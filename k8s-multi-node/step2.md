## Step2 把工作节点加入到K8S集群

在step1 我们已经使用kubeadm 创建了一个集群，现在需要把node1, node2添加到集群。

2.1 切换node1,使用kubeadm join 添加节点

请把step1的 kubeadm join **信息复制到终端

```bash
#执行/data/work/join.sh,将node加入集群
```



`/data/work/join.sh`{{execute}}



正常情况下稍后工作节点node1就会加入到集群

* node2 重复执行上面的步骤即可。

2.2 返回master 查看节点、服务状态

`kubectl get nodes `{{execute}}

`kubectl get svc`{{execute}}

