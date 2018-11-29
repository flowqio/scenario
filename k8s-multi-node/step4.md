## Step4  使用Dashboard 

4.1 在master节点查看dashbaord token

```ba
sh /data/share/k8s/showToken.sh
```

`sh /data/share/k8s/showToken.sh`{{execute}}

4.3 在master节点启动kubectl proxy

```bas
sh /data/share/k8s/startProxy.sh
```



`sh /data/share/k8s/startProxy.sh`{{execute}}



4.4 通过URL  http://<id>-8001-<env id>.env.flowq.io/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/进行访问

```bash
#example : 
#http://01d43df4f5ef558d-8001-env1.env.flowq.io/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/
```

`sh /data/share/k8s/showToken.sh`{{execute}} 