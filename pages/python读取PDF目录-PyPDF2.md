- "from PyPDF2 import PdfFileReader
# 每个PDF书签的索引格式
# {'/Title': '书签名', '/Page': '指向的目标页数', '/Type': '类型'} 
pdf_path="/Users/yutianran/Downloads/MyObsidian/06-Book/论语今读.pdf"
md_path="/Users/yutianran/Downloads/MyObsidian/论语今读-content.md"

pdf = PdfFileReader(pdf_path)
bookmarks = pdf.getOutlines()

def get_pagenum(page, bookmarks,level):
    for i in bookmarks:
        if isinstance(i,list):
            get_pagenum(page, i,level+1)
        else:
            page_num=pdf.getDestinationPageNumber(i)
            prefix="  "*level
            line=f"{prefix}- {i['/Title']}-{page_num}"
            page.append(line)
    return page
# 收集
page= []
get_pagenum(page, bookmarks,0)
# 整理
directory_str= ''
for i in page:
    directory_str=directory_str+i+"\n"
    print(i)
# 输出
with open(md_path, 'w', encoding='utf-8') as f:
    f.write(directory_str)

"
- python读取PDF标注-PyMuPDF
  "from typing import List, Tuple
  
  import fitz  # install with 'pip install pymupdf'
  import pandas as pd
  
  def _parse_highlight(annot: fitz.Annot, wordlist: List[Tuple[float, float, float, float, str, int, int, int]]) -> str:
      points = annot.vertices
      quad_count = int(len(points) / 4)
      sentences = []
      for i in range(quad_count):
          # where the highlighted part is
          r = fitz.Quad(points[i * 4 : i * 4 + 4]).rect
  
          words = [w for w in wordlist if fitz.Rect(w[:4]).intersects(r)]
          sentences.append(" ".join(w[4] for w in words))
      sentence = " ".join(sentences)
      return sentence
  
  
  def handle_page(page):
      wordlist = page.getText("words")  # list of words on page
      wordlist.sort(key=lambda w: (w[3], w[0]))  # ascending y, then x
  
      highlights = []
      annot = page.firstAnnot
      while annot:
          if annot.type[0] == 8:
              highlights.append(_parse_highlight(annot, wordlist))
          annot = annot.next
      return highlights
  
  
  path="/Users/yutianran/Downloads/MyObsidian/06-Book/论语今读.pdf"
  doc = fitz.open(path)
  highlights = []
  for page in doc:
      highlights += handle_page(page)
  
  #print(highlights)
  highlighted_text = [",".join(i.split(" ")) for i in highlights] # adds a comma in place of spaces
# print(highlighted_text)
for i in highlighted_text:
    print(i)
# df = pd.DataFrame(highlights)
# print(df.head())
"