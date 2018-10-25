## Docker - 部署你的第一个容器

+ 难度: 入门  
+ 预计花费时间: 10 分钟

    在这个入门的实验里面,你将要扮演一个开发者Jack, 他当前非常需要一个可靠的Key-Value Store存储服务, 在讨论后他确定选择redis作为自己的KV Store存储后端.

     Jack 不太熟悉redis的安装配置,但是他听说Docker可以简化redis的部署使用,以及他可以在很短的时间里面用到redis. 这个练习就是帮助Jack完成自己的任务:在Docker里部署一个redis container.

### Docker 是什么?
+ Docker describes  "an open platform for developers and sysadmins to build, ship, and run distributed applications".
+ Docker 可以让你运行容器(containers), 每一个容器就像独立的sandbox运行程序和它依赖的操作系统, 是一种比传统VM虚拟化更加轻量的方式,同一个机器上可以运行多个容器.
  
+ [Docker wikipedia] (https://en.wikipedia.org/wiki/Docker_(software\))

   