## Step4  使用Dashboard 

4.1 使用kubectl创建pod

```ba
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/recommended/kubernetes-dashboard.yaml
```



4.2 创建dashboard所需要的角色

```bash
kubectl apply -f /data/share/k8s/dashboard-admin.yaml
```



4.3 启动kubectl proxy

```bas
sh /data/share/k8s/startProxy.sh
```



`sh /data/share/k8s/startProxy.sh`{{execute}}



4.4 查看Token

```bash
sh /data/share/k8s/showToken.sh
```

`sh /data/share/k8s/showToken.sh` {{execute}}

