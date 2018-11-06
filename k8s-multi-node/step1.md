## Step1 K8S基本操作:

环境介绍:

* 主机名: master , k8s 管理节点
* 主机名: node1, k8s 工作节点
* 主机名: node2, k8s 工作节点

​    

1.1 首先选择master  , 初始化kubeadm

`hostname`{{execute}}

如果是master则继续，如果是node1,node2请切换主机

执行kubeadm init,该命令需要花费一定时间在后台远程下载系统所需要的image 

执行下面的命令:

 ```bash

   #旧版本 kubeadm init --apiserver-advertise-address $(hostname -i)
   #新版本
   cp /data/share/k8s/kubeadm.sh . && chmod 775 ./kubeadm.sh
   #(如果/data/share 目录为空的话请稍后再试或者联系管理员steven@flowq.io)
 ```

`cp /data/share/k8s/kubeadm.sh `{{execute}}

`chmod 775 ./kubeadm.sh`{{execute}}

`./kubeadm.sh`{{execute}}

新的脚本kubeadm.sh会创建/data/work/join.sh 直接切换到node1,node2执行即可.



1.2 为kubernetes 配置网络(请省略1.2 直接到第step2 添加节点)

kubernetes可以使用多种cni网络,在这里我们使用的是weave

执行下面的命令:

```bash

  kubectl apply -n kube-system -f /data/share/k8s/weave/net.yaml

```



1.3 查看kubernetes 节点、集群信息

`kubectl get nodes`{{execute}} 

可以发现master节点已经注册到K8S集群

`kubectl cluster-info`{{execute}}

