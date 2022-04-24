- Relate
	- #Syncthing #版本管理 #团队协作 #软件工程 [[Github]] [[GitBook]]
- 资料
	- [轮子那点事儿(2)：获取GitHub Followers, Stars, Forks的API的制作 | Lazy_V's Blog](http://blog.zhangkexuan.cn/2020/11/05/api-fanscount-github/)
- 书籍
	- [[Pro Git]]
	- [[Git权威指南]]
- 笔记
	-
- FAQ
	- 更新gitignore
	  id:: 6263c594-fcfc-4a1c-b6ee-9210514976ff
		- id:: 6263c594-da57-46b5-9ca8-8dacca80f281
		  ```
		  git rm -r --cached .
		  git add .
		  git commit -m "update .gitignore"
		  ```
	- git push Github失败，提示443
	  collapsed:: true
		- SSL_connect: SSL_ERROR_SYSCALL in connection to github.com:443
		- git config --global --unset http.proxy
		- git config --global http.sslVerify "false"
	- GIT实现本地配置文件修改后不提交远程仓库
	  id:: 6263c594-8634-415a-bb19-9b78ad82d25b
		- [GIT实现本地配置文件修改后不提交远程仓库 - 思无 - 博客园](https://www.cnblogs.com/lovelyli/p/13359421.html)
		- git关闭跟踪文件修改提交
			- git update-index --assume-unchanged "/root/tem/java/web/application-dev.yml"
		- git打开跟踪文件修改提交
			- git update-index --no-assume-unchanged "/root/tem/java/web/application-dev.yml"
	- 使用另一个本地仓库作为远程仓库
		- [你的github-通过坚果云管理您的代码 | 坚果云博客](http://jianguoyun.blog.techweb.com.cn/archives/80.html)
		- 初始化远程仓库
			- git init –bare
		-
-
-
-