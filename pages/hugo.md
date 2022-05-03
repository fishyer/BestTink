- 资料
	- [Hugo 从入门到会用 - olOwOlo](https://olowolo.com/post/hugo-quick-start/)
	- [为 obsidian 中的文件批量添加 front matter - 习吾学](https://xwlearn.com/howto-add-frontmatter-in-batch-for-files-in-obsidian/)
		- 找到这个博主的仓库了，fork了 [fishyer/xwlearn: My Blog](https://github.com/fishyer/xwlearn)
	- [Front Matter | Hugo](https://gohugo.io/content-management/front-matter/)
	  collapsed:: true
		- ```yaml
		  ---
		  title: "文章标题"
		  description: "文章的描述信息"
		  tags: [ "标签1", "标签2", "标签3" ]
		  categories: [ "分类1", "分类2" ]
		  keywords: [ "Hugo", "keyword" ]
		  date: 2012-04-06
		  lastmod: 2015-12-23
		  # CJKLanguage: Chinese, Japanese, Korean
		  isCJKLanguage: true
		  
		  # 如果draft为true，除非使用 --buildDrafts 参数，否则不会发布文章
		  draft: false
		  
		  # 设置文章的过期时间，如果是已过期的文章则不会发布，除非使用 --buildExpired 参数
		  expiryDate: 2020-01-01
		  
		  # 设置文章的发布时间，如果是未来的时间则不会发布，除非使用 --buildFuture 参数
		  publishDate: 2020-01-01
		  
		  # 排序你的文章
		  weight: 40
		  
		  # 使用这两个参数将会重置permalink，默认使用文件名
		  url: 
		  slug: 
		  
		  # 别名将通过重定向实现
		  aliases:
		    - 别名1
		    - /posts/my-original-url/
		    - /2010/01/01/another-url.html
		  
		  # type 与 layout 参数将会改变 Hugo 寻找该文章模板的顺序，将在下一节细述
		  type: review
		  layout: reviewarticle
		  
		  # 三个比较复杂的参数
		  taxonomies:
		  linkTitle: 
		  outputs:
		  # 实验性的参数
		  markup: "md"
		  
		  # 你还可以自定义任何参数，这些参数可以在模板中使用
		  include_toc: true
		  show_comments: false
		  ---
		  ```
	- [Hugo框架中文文档 前言设定 Front Matter - Andbible](https://www.andbible.com/post/hugo-content-management-front-matter/)
	- [olOwOlo/hugo-theme-even: 🚀 A super concise theme for Hugo https://hugo-theme-even.netlify.app](https://github.com/olOwOlo/hugo-theme-even)
	-
- 笔记
	- 给已有的blog添加front-matter属性
	  collapsed:: true
		- python获取文件名
			- [Python3 os.path() 模块 | 菜鸟教程](https://www.runoob.com/python3/python3-os-path.html)
		- python正则替换
- 常用命令
	- 安装hugo
		- brew install hugo
	- 查看版本：
		- hugo version
	- 新建一篇文章：
		- hugo new post/my-first-blog.md
	- 生成静态文件：
		- hugo -t even
	- 启动服务器：
		- hugo server
		- hugo server --disableFastRender
		- hugo server --minify --theme hugo-book
	- 正常启动服务后，在浏览器打开 http://localhost:1313/ 看到我们的网站。
- 文件夹说明
	- archetypes 使用hugu new post生成新文章的模板，可以自定义里面的值
	- content 存放网站内容
	- data 存储Hugo在生成您的网站时可以使用的配置文件
	- layouts 以.html文件的形式存储模板，指定如何将内容的视图呈现到静态网站中
	- static 存储所有静态内容：图像，CSS，JavaScript等，当Hugo构建您的站点时，静态目录中的所有资产都将按原样复制
	- themes 存放主题
	- config.toml 配置文件
-
-
-