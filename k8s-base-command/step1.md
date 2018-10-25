## Step1 K8S基本操作:


kubectl 是k8s自带的命令客户端

1.1 查看k8s集群信息 

`kubectl cluster-info`{{execute}}

该命令会返回当前k8s集群信息

扩展操作,获取详细的k8s集群信息: 
	`kubectl cluster-info dump `{{execute}}


1.2 查看k8s资源信息

kubectl get <参数>是一个非常重要的操作可以查询各类k8s资源


`kubectl get nodes`{{execute}}

`kubectl get pods`{{execute}}




