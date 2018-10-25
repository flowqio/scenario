## Step2 使用K8S运行一个应用

 kubernets创建应用有多种方法,可以使用run , create,apply

2.1 使用run运行一个nginx application

`kubectl run --image=nginx nginx-app --port=80`{{execute}}



2.2 使用exec 访问一个pod

线获取这个pods的名字nginx-app-xxx
 
`kubectl get pods `{{execute}}

kubectl exec nginx-app-xxx ls