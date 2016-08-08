title: Nginx 初识
date: 2016-08-03 23:07:30
tags: hexo
---

#### 结识
    
搭建本博客使用的就是本款强大的可扩展的`Nginx`web/proxy服务器。在了记录一下nginx相关的信息方便后面查找使用，加深一下自己对nginx的理解，毕竟作为自己不经常使用。

Nginx的安装步骤就不在这里提了，毕竟网上优秀的文章很多，在这里主要记一下相关的使用方法。

#### 使用


nginx启动、重启、关闭

```

	# 启动
	nginx    

	# 关闭
	ps -ef | grep nginx   	# 查询nginx主进程号
	kill -QUIT 进程号      	# 从容停止
	kill -TERM 进程号 		# 快速停止
	kill -9 进程号  			# 强制停止
	# 如果ngixn.conf配置了pid文件路径，如果没有，则在logs目录下
	kill -信号类型 '/usr/local/nginx/logs/nginx.pid'

	# 重启 更改配置后需要重启
	kill -HUD 主进程号或进程号文件路径  # 方法1
	nginx -s reload   

```

