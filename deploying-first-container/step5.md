## Step5 持久化数据
过了一段时间Jack的Redis存储了一些数据，但是当他删除并重新创建container的时候出现了数据丢失,原因就是container是非持久化的, Jack需要一个数据持久化的方案,避免这样情况的出现.

Containers 是被设计成无状态的. 我们可以通过绑定外部卷(volumes)的方式为它增加持久化能力, 可以使用 -v <host-dir>:<container-dir> 参数. 当一个目录/卷被加载, 这个目录里面的文件可以被容器进行读写，这个功能允许你实现container的数据持久化.

Task
Jack 通过文档知道了官方Redis镜像会将数据存储在/data目录.为了实现数据持久化,Jack需要将docker host(本地目录) /opt/docker/data/redis 映射到cotnainer的/data目录.

完整的命令:

  `docker run -d --name redisMapped -v /opt/docker/data/redis:/data redis`{{execute}}

