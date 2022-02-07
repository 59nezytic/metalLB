* Tool for Using LoadBalancer at Kubernetes (kubeadm)

```
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.9.3/manifests/namespace.yaml
```

```
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.9.3/manifests/metallb.yaml
```

```
kubectl create secret generic -n metallb-system memberlist --from-literal=secretkey="$(openssl rand -base64 128)"
```

* Change your floating IP at <metalLB_cm.yaml>

```
kubectl create -f metalLB/metalLB_cm.yaml
```
