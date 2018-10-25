## Step3 访问Redis

Jack通过 docker run 已经成功运行了Redis, 每个continer是一个沙箱，需要通过导出服务端口才能被外部应用访问.


Jack知道Redis默认的服务端口为6379. 他需要学习通过docker如何导出Redis服务端口.


通过查看文档, Jack 发现可以通过 -p <host-port>:<container-port> 参数. 

`docker run -d --name redisHostPort -p 6379:6379 redis:latest`{{execute}}


默认的端口被导出映射到 0.0.0.0,如果你想映射到127.0.0.1,可以通过如下参数实现: -p 127.0.0.1:6379:6379
