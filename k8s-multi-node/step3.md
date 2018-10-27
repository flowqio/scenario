## Step3  测试K8S集群

在step1，step2 我们完成了K8S多节点集群的创建，现在我们运行一个基本的应用来测试我们的K8S集群。

3.1 在master节点，使用kubectl部署

`kubectl apply -f https://raw.githubusercontent.com/kubernetes/website/master/content/en/examples/application/nginx-app.yaml` {{execute }}

查看K8S部署情况

`kubectl get deploy`{{execute}}

`kubectl get svc`{{execute}}

并使用curl访问cluster ip , 如果返回nginx欢迎页,说明已经K8S集群已经成功创建。