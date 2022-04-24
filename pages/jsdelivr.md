- task
	- DONE 能否配合Github用来做图床
	  :LOGBOOK:
	  CLOCK: [2022-04-18 Mon 05:10:17]--[2022-04-18 Mon 05:10:17] =>  00:00:00
	  :END:
	- DONE 能否使用photo.fishyer.com代替cdn.jsdelivr.net/gh/fishyer/photo@main，这一长串？
	  collapsed:: true
		- [[CloudFlare]]如何使用重定向？
			- 资料
				- [使用 Cloudflare 的 Page Rules 页面规则进行 URL 转发和域名重定向的图文教程 - 灯芯](https://iyideng.cc/blog/cloudflare-url-forwarding-and-domain-name-redirection.html)
				- 示意图
				  collapsed:: true
					- ![Replaced by Image Uploder](https://photo.fishyer.com/img/202204180555426.png){:height 412, :width 646}
			- photo.fishyer.com/*
			- 转发 URL - 状态代码: 301 - 永久重定向
			- https://cdn.jsdelivr.net/gh/fishyer/photo@main/$1
- cdn链接格式
	- // load any GitHub release, commit, or branch
	- // note: we recommend using npm for projects that support it
	- https://cdn.jsdelivr.net/gh/user/repo@version/file
	- // load jQuery v3.2.1
	- https://cdn.jsdelivr.net/gh/jquery/jquery@3.2.1/dist/jquery.min.js
	- // use a version range instead of a specific version
	- https://cdn.jsdelivr.net/gh/jquery/jquery@3.2/dist/jquery.min.js
	- https://cdn.jsdelivr.net/gh/jquery/jquery@3/dist/jquery.min.js
	- // omit the version completely to get the latest one
	- // you should NOT use this in production
	- https://cdn.jsdelivr.net/gh/jquery/jquery/dist/jquery.min.js
	- // add ".min" to any JS/CSS file to get a minified version
	- // if one doesn't exist, we'll generate it for you
	- https://cdn.jsdelivr.net/gh/jquery/jquery@3.2.1/src/core.min.js
	- // add / at the end to get a directory listing
	- https://cdn.jsdelivr.net/gh/jquery/jquery/
- 资料
	- [jsDelivr - A free, fast, and reliable CDN for open source](https://www.jsdelivr.com/?docs=gh)
	- [GitHub+jsdelivr+PicGo 搭建图床 - 知乎](https://zhuanlan.zhihu.com/p/345163512)
	- [fishyer/photo: 图床](https://github.com/fishyer/photo)
- 示例
	- https://
	- cdn.jsdelivr.net/gh/fishyer/photo@main/img/202202121857752.png
	- photo.fishyer.com/img/202202121857752.png
	- 测试一下
		- ![](https://photo.fishyer.com/img/202204180551727.png)
	- 配置示意图
	  collapsed:: true
		- ![](https://cdn.jsdelivr.net/gh/fishyer/photo@main/img/202204180507954.png)
- [[配置host，加速github访问速度]]
-