```bash
eval $(minikube docker-env)
```
or
```powershell
& minikube -p minikube docker-env --shell powershell | Invoke-Expression
```

Deploy images


```bash
kubectl apply -f .
```


