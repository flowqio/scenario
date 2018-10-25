## Step4 访问Redis-续

如果Jck想运行多个Redis 实例,就会出现端口被占用的情况


任务
通过查询问题, Jack发现可以使用-p 6379 ,注意不是"-p 6379:3379" 将container 6379端口导出为一个随机端口 `docker run -d --name redisDynamic -p 6379 redis:latest`{{execute}}

接着可以通过 `docker port redisDynamic 6379`{{execute}} 查看端口

Jack当然也可以痛殴之前学习的ps命令,查看所有的container的端口  ```docker ps```{{execute}}