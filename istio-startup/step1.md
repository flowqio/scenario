## Step1 最小化安装istio基本操作:



我们已经构建了一个基于minikube的环境,可以直接使用kubectl 最小化安装

1.1 查看k8s集群信息 

`kubectl cluster-info`{{execute}}

该命令会返回当前k8s集群信息,如果没有报错我们可以进行下一步安装

扩展操作,获取详细的k8s集群信息: 
​	`kubectl cluster-info dump `{{execute}}

1.2 解压istio-1.0.2-linux.tar.gz 

`cd /data/work`{{execute}}

`tar -zxvf /data/share/istio/istio-1.0.2-linux.tar.gz`{{execute}}

 `cd istio-1.0.2`{{execute}}

1.3 安装所需的Customer Resource Definition 定义文件配置文件

`kubectl apply -f install/kubernetes/helm/istio/templates/crds.yaml`{{execute}}

```b
error: unable to recognize "install/kubernetes/istio-demo.yaml": no matches for admissionregistratio
n.k8s.io/, Kind=MutatingWebhookConfiguration
#忽略上面的错误
```



1.4 安装不需要TLS的istio-demo

`kubectl apply -f install/kubernetes/istio-demo.yaml`{{execute}} 

可以通过istio-system namespace 查看istio pods 安装情况

`kubectl get pods -n istio-system`{{execute}}






