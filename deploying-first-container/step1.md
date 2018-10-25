## Step1 运行一个容器(Container):

所有的Container都需要加载Docker镜像(docker image), 首先第一步我们要确认运行redis所需要的镜像名字. 这个镜像包含了所有redis需要的执行文件、库、系统环境,而且不会依赖于其他环境.

Jane 可以从registry.hub.docker.com/ 寻找到自己的需要的镜像, 也可以使用docker search <name>. 本例子就是使用 "docker search redis" 查找包含redis的镜像.



1.1 查看本地存储的docker镜像

`docker images`{{execute}}

该命令会返回当前docker主机本地所有的image


1.2 搜索 redis 镜像

docker search <name>

Jack 可以通过使用serach 命令, 查找到官方的Redis Docker镜像. 


`docker search redis`{{execute}}

1.2 运行 redis 镜像
因为Redis是后台NoSQL服务,所以Jack 可以在后台运行该服务.
`docker run -d redis`{{execute}}

默认的Docker会下载最新（latest)版本镜像, 如果想使用特定的版本可以通过tag参数, 在本例子, 运行 docker run -d redis:3.2 就会使用 version 3.2.

如果Jack是第一次使用redis 镜像,docker会自动从hub.docker.com下载镜像到本地



