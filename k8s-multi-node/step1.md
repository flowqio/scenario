## Step1 K8S基本操作:

环境介绍:

* 主机名: master , k8s 管理节点
* 主机名: node1, k8s 工作节点
* 主机名: node2, k8s 工作节点

​    

1.1 首先选择master  , 初始化kubeadm, *请不要使用kubeadm init执行

命令说明:

 ```bash

   
   #如果发现/data/share 目录为空的话请稍后再试或者联系管理员steven@flowq.io)
   
   
 ```

请执行集群创建命令:

`bash /data/share/k8s/kubeadm.sh  `{{execute}}

执行后需要花费一定时间在后台远程下载系统所需要的image ,

稍后会自动创建/data/work/join.sh, 直接切换到node1,node2执行即可.



1.2 ~~为kubernetes 配置网络(请省略1.2 直接到第step2 添加节点)~~

~~kubernetes可以使用多种cni网络,在这里我们使用的是weave~~

~~执行下面的命令: kubectl apply -n kube-system -f /data/share/k8s/weave/net.yaml~~



1.3 查看kubernetes 节点、集群信息

`kubectl get nodes`{{execute}} 

可以发现master节点已经注册到K8S集群

`kubectl cluster-info`{{execute}}

