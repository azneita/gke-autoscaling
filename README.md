# gke-autoscaling
See https://blog.azneita.org/2022/08/11/google-kubernetes-engine-autoscaling/

## Additional GCP permissions required
To be able to create role and rolebinding objects, the following permissions are required
- container.roles.create	
- container.roleBindings.create

## How to use?
```
kubectl apply -f 01-horizontalpodautoscaler.yaml
kubectl apply -f 02-serviceaccount.yaml
kubectl apply -f 03-role.yaml
kubectl apply -f 04-rolebinding.yaml
kubectl apply -f 05-scale-up-cronjob.yaml
kubectl apply -f 06-scale-down-cronjob.yaml
