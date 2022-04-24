alias:: Logseq入门简介

- 基础教程
	- 极简版
		- [Logseq小白系列教程入门篇一 - 知乎](https://zhuanlan.zhihu.com/p/343854552)
		- [Logseq小白系列教程入门篇二 - 知乎](https://zhuanlan.zhihu.com/p/405764984)
	- 文字版
		- [Logseq 中文文档](https://logseq-documents-cn.fishyer.com/#/page/Contents)
			- 来源于[Logseq 中文文档 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/1787)
			- 我怕他删库了，所以自己备份到自己服务器，重新部署了一份
	- 视频版
		- 来源自Obsidan群的 #及时春雨
		- [Logseq从入门到精通-15集视频-bilibili](https://www.bilibili.com/video/BV1144y14764)
- 为什么推荐Logseq做笔记
  collapsed:: true
	- 1-它有大纲、MarkDown、双链等功能，还是本地的，免费的，开源的，编辑体验也超爽
	- 2-它的自动聚合功能超爽，可以帮我们发现笔记之间的潜在链接，让以前的笔记不至于石沉大海
		- 案例效果，来源于[双链笔记软件推荐：Logseq 和它的五种用法 - 少数派](https://sspai.com/post/69503)
		  collapsed:: true
			- ![](https://photo.fishyer.com/img/202204212126602.png)
- 新手建议
  collapsed:: true
	- 1-就当一个普通的[[大纲]]软件来用就行了，Tab键变成下级节点，Shift+Tab变成上级节点
	- 2-就当一个普通的[[MarkDown]]软件就行了，## 二级标题，### 三级标题，更多语法看[这里](https://cubox.pro/share/bWpE42)
	- 3-就当一个普通的[[双链]]笔记软件来用 就行了，`[[]]`就是另一条笔记联系起来，可以当标签来用
	- 4-多用`/`命令，里面有很多快捷输入的方法，不用自己记语法
	- 不建议新手去玩的功能
		- 别名
			- 比如给一个页面取多个标题，方便在不同地方引用它
				- ```
				  alias:: title1 title2
				  ```
		- 嵌入
			- 比如嵌入一个页面
				- ```
				  {{embed [[SubPage]]}}
				  ```
		- 高级Query
			- 不过简单的Query语法可以了解一下，
				- 查找所有属性为public，值为false的笔记
					- ```
					  {{query (property public false)}}
					  ```
- 高级搜索
  collapsed:: true
	- 不建议新手去折腾高级搜索
	-
- 插件
  collapsed:: true
	- 不建议新手去折腾插件，因为Logseq本身提供的功能已经足以满足我们的大多数笔记场景
	- 不过这几个插件强烈建议安装一下
		- 只建议安装我现在依然启用的那几个
			- ![](https://photo.fishyer.com/img/202204231748406.png)
	-
- Obsidian与Logseq的对比
  collapsed:: true
	- Obsidian的劣势
		- 1.Obsidan更偏向Markdown，对于大纲的支持不是特别好，适合写长文，但不是很适合整理思路
		- 2.Obsidian的所见即所得，没有Logseq用起来爽
		- 3.Obsidian的潜在链接不是很方便查看时编辑，无法直接在当前page编辑它的潜在链接的那个block，点击潜在链接的block，会自动跳转到那个block所在的page，有点麻烦
		- 4.Obsidian没有Logseq的导出html功能，不方便用来建站
		- 5.Obsidian的块引用没有Logseq方便，是基于##标题的
	- Obsidian的优势
		- 1.Obsidian的插件更加丰富
		- 2.Obsidian的流畅度更好一点，毕竟它不算严格的块编辑器，节点主要是page级别，底层的数据库的压力不是特别大，这点在移动端时会比较明显
		- 3.Obsidian的潜在链接比较方便快速关联，目前Logseq还没有这方面的快捷方式，可能需要借助PopClip
		- 4.Obsidian可直接查看文件夹体系，管理附件会比较方便
		- 5.如果舍得花钱的话，Obsidan官方有同步和发布功能，Logseq暂时还没有
- 个人使用Logseq的一些心得
	- 不建议用Logseq做PDF阅读，推荐[[Zotero]]，因为Logseq不方便管理书架
	- 不建议用Logseg做任务管理，推荐[[滴答清单]]，因为滴答清单收集任务和日程提醒更方便
	- 不建议用Logseq做写作分享，推荐[[MWeb]]，因为大纲很适合自己整理思路，保持简洁，但不是特别便于分享，并且它也没有直接发布到各种自媒体平台的插件
- FAQ-我自己整理的在日常使用Logseq的过程中遇到的一些问题
	- DONE 目前Logseq还没有一键收藏别人分享的Logseq页面功能，复制粘贴时，会发现只能复制一个节点
		- 好在可以借助Cubox的收藏，实现网页快照保存，以免别人的博客挂了导致链接失效
	- TODO 准备发布文章时，如何将Logseq的大纲形式转换为标准MarkDown形式？
		- 自己刚准备用sed来做下批量替换时，突然发现网上已经有大神写好了脚本
		  collapsed:: true
			- [logseq转换为标准markdown脚本](https://xutuan.vercel.app/#/page/logseq%E8%BD%AC%E6%8D%A2%E4%B8%BA%E6%A0%87%E5%87%86markdown%E8%84%9A%E6%9C%AC)
		- 脚本
		  collapsed:: true
			- ```
			  # convert logseq to md
			  for file in *.md **/*.md **/**/*.md 
			  do
			  	# filepath="$file"
			  	file_name=$(basename "$file")
			  	echo "PROCESSING $file..."
			  	queryb='#+BEGIN_QUERY'
			  	querye='#+END_QUERY'
			  	sed -i 's/##########/\t\t\t\t\t\t\t-/' $file
			  	sed -i 's/#########/\t\t\t\t\t\t-/' $file
			  	sed -i 's/########/\t\t\t\t\t-/' $file
			  	sed -i 's/#######/\t\t\t\t-/' $file
			  	sed -i 's/######/\t\t\t-/' $file
			  	sed -i 's/#####/\t\t-/' $file
			  	sed -i 's/####/\t-/' $file
			  	sed -i 's/###/-/' $file
			  	# sed -i 's/##//' $file
			  	sed -i 's/:PROPERTIES:/<!--/' $file
			  	sed -i 's/:END:/-->\n/' $file
			  	sed -i 's/{{{embed /#relink-embed <!--/' $file
			  	sed -i 's/((/#relink-block [[/' $file
			  	sed -i 's/))/]]/' $file
			  	sed -i 's/{{{/#relink <!--/' $file
			  	sed -i 's/}}}/-->/' $file
			  	sed -i 's/{{/#relink <!--/' $file
			  	sed -i 's/}}/-->/' $file
			  	sed -i "s/$queryb/<!--$queryb/" $file
			  	sed -i "s/$querye/$query-->\n\n/" $file
			  done
			  ```
		- 步骤
		  collapsed:: true
			- 代码保存为`convertlogseq.sh`
			- 将需要转换的markdown文件与脚本放在同一个文件夹下
			- cmd-cd进入待处理的文件夹路径
			- 运行 > `convertlogseq.sh`
		- 哈哈，感觉配合MWeb的发布前脚本配置，完美
	- TODO 如何发布Logseq为博客？
	  :LOGBOOK:
	  CLOCK: [2022-04-23 Sat 18:20:56]--[2022-04-23 Sat 18:20:56] =>  00:00:00
	  :END:
		- DONE 1-本地导出为html，上传到github，借助vercal的部署服务，借助CloudFlare做重定向
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:44:26]--[2022-04-23 Sat 18:44:27] =>  00:00:01
		  :END:
		- DOING 2-直接用Github Action在远程导出html，提交即自动发布，后续步骤同1
		  id:: 6263d353-e761-406e-8b15-4a4f0528adb9
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:55:16]
		  :END:
			- 参考资料
				- [Logseq Publish · Actions · GitHub Marketplace](https://github.com/marketplace/actions/logseq-publish)
				- [配置 Logseq 自动发布相关流程](https://logseq.abosen.top/#/page/%E9%85%8D%E7%BD%AE%20logseq%20%E8%87%AA%E5%8A%A8%E5%8F%91%E5%B8%83%E7%9B%B8%E5%85%B3%E6%B5%81%E7%A8%8B)
	- TODO logseq没有像WorkFlowy那样的@标签，感觉制作一些人名标签时不是很方便
	  :LOGBOOK:
	  CLOCK: [2022-04-23 Sat 18:44:15]--[2022-04-23 Sat 18:44:16] =>  00:00:01
	  :END:
	- TODO logseq的block有方便的移动方式么？
	- TODO logseq的图片自动上传插件 ImageUploader好像在0.6.6以后又不行了
	- TODO logseq的默认日志文件名称，修改了配置文件，但好像只能修改显示效果，不会修改实际文件名
	- WAITING 一次导入太多Markdown文件到Logseq库里面，导致卡顿怎么办
		- 无解，不过现在好像优化了很多，现在好像不怎么卡了
	- TODO logseq导入的zotero标注，都找不到anotations，只有一些元数据
	- DONE 如何获取笔记的URL Schema，以方便和其它工具联动
	  collapsed:: true
	  :LOGBOOK:
	  CLOCK: [2022-04-23 Sat 18:06:08]--[2022-04-23 Sat 18:06:09] =>  00:00:01
	  :END:
		- 右上角，Copy page URL
		- ```
		  logseq://graph/MyLogseq?page=Contents
		  ```
	- DOING 在外部点击logseq的url，会新建一个窗口，而不是复用原来的窗口，据说已有PR，但尚未正式发布
	  :LOGBOOK:
	  CLOCK: [2022-04-23 Sat 18:07:23]
	  :END:
	- DONE 如何定制首页
	  :LOGBOOK:
	  CLOCK: [2022-04-23 Sat 18:07:30]--[2022-04-23 Sat 18:07:30] =>  00:00:00
	  :END:
		- 比如你想让你的overview页面作为博客首页,还是打开config.edn这个文件, 然后输入如下内容
			- ```
			  :default-home {:page "overview":sidebar "Contents" }
			  ```
	- DONE 如何自定义主题
	  :LOGBOOK:
	  CLOCK: [2022-04-23 Sat 18:19:37]--[2022-04-23 Sat 18:19:38] =>  00:00:01
	  :END:
		- 修改logseq/config.edn，即可
		- 可以配置Github仓库里面的的远程文件做主题，[Logseq主题](https://gist.github.com/3e82a313a58b816a7ddf6de25a607977)
			- 使用[[jsdelivr]]给github文件做cdn加速
	- DONE 如何添加页面别名，方便在不同的引用地方使用不同的名称
	  :LOGBOOK:
	  CLOCK: [2022-04-23 Sat 18:17:47]--[2022-04-23 Sat 18:17:48] =>  00:00:01
	  :END:
		- [term/alias](https://docs.logseq.com/#/page/term%2Falias )
		- ```
		  alias:: title1 title2
		  ```
- 网上的公开Logseq数字花园案例
  collapsed:: true
	- [abosen-README](https://logseq.abosen.top/#/page/README)
	- [xutuan-logseq使用经验分享](https://xutuan.vercel.app/#/page/logseq%E4%BD%BF%E7%94%A8%E7%BB%8F%E9%AA%8C%E5%88%86%E4%BA%AB)
	- [zhangxueshan246-Logseq](https://zhangxueshan246.github.io/#/)
	- [tothegarden-All journals](https://tothegarden.vercel.app/all-journals)
- 书签
	- [Logseq中文文档-起步](https://logseq-documents-cn.fishyer.com/#/page/%E8%B5%B7%E6%AD%A5)
	- [Quicker + zotero/Mdnotes 实现Logseq打开外部PDF并注释 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/1446)
	- [如何发布logseq成为博客 - 知乎](https://zhuanlan.zhihu.com/p/344165645)
	- [OKR + GTD + Note => Logseq · 构建我的被动收入](https://www.bmpi.dev/self/okr-gtd-note-logseq/)
	- [logseq/awesome-logseq: Awesome Logseq resources created by the community <3](https://github.com/logseq/awesome-logseq)
	- [Logseq使用教程之七：Telegram+IFTTT+Quicker实现Logseq速记 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/3369)
	- [logseq使用经验分享](https://xutuan.vercel.app/#/page/logseq%E4%BD%BF%E7%94%A8%E7%BB%8F%E9%AA%8C%E5%88%86%E4%BA%AB)
	-
- {{embed [[欢迎加入]]}}
-