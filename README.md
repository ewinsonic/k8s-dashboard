# kubernetes-dashboard use


## Create 
```
kubectl create -f kubernetes-dashboard.yaml
kubectl create -f admin-user.yaml
kubectl create -f admin-role.yaml
```

## Get Token
```
kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
```

### Then Use Token to Login, node Port is on 30005
