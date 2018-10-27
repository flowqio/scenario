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

   kubeadm init --apiserver-advertise-address $(hostname -i)

 ```


需要注意init结束后输出的kubeadm join **信息, 后面添加工作节点时需要使用

kubeadm join <master ip:port> --token <自动生成的token> --discovery-token-ca-cert-hash sha256:<ca证书的sha256 base64编码>

例如

kubeadm join 10.0.0.5:6443 --token yw2jb0.7rzg82yadmh5pvjw --discovery-token-ca-cert-hash sha256:cbedccbacd05b6da9c93eae180b5a3bbe8ef3abc20996796bdf9ef26656178bb



1.2 为kubernetes 配置网络

kubernetes可以使用多种cni网络,在这里我们使用的是weave

执行下面的命令:

```bash

  kubectl apply -n kube-system -f "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 |tr -d '\n')"

```



1.3 查看kubernetes 节点、集群信息

`kubectl get nodes`{{execute}} 

可以发现master节点已经注册到K8S集群

`kubectl cluster-info`{{execute}}

