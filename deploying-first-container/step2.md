## Step2 docker 查看一个Container



通过docker ps 命令可以查看所有正在运行的container ,包括container的名字,启动时间,运行时间.

这个命令返回的name/ID可以被用于docker 其他命令

比如查看container详细信息,  "docker inspect <friendly-name|container-id>" 

查看container 日志, "docker logs <friendly-name|container-id>" 将显示container的标准输出、错误日志.



2.1 查看Container 

我们在Step1 运行了一个redis镜像,现在我们使用docker ps命令来查看container

`docker ps`{{execute}}


`curl www.google.com`{{execute}}