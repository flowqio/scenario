## Step2 安装Bookinfo 实例

 上一节我们使用安装了不带TLS的istio, 并且已经通过nodeport配置,可以正常使用istio以及相关组件的服务,本节将接着安装bookinfo示例

2.1 使用kubectl 安装booinfo 

`kubectl apply -f samples/bookinfo/platform/kube/bookinfo.yaml`{{execute}}

查看booinfo pods 运行状态

`kubectl get po`



2.2 使用istioctl 定义网关

`istioctl create -f samples/bookinfo/networking/bookinfo.gateway.yaml`

