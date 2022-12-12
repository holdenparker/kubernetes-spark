
Install Docker Desktop
https://www.docker.com/

Enable Kubernetes in settings

Following this example:
https://towardsdatascience.com/ignite-the-spark-68f3f988f642

Deploy infrastructure to kubernetes cluster
```
kubectl create -f ./k8s/deploy.yaml
```

Open access to Jupyter
```
kubectl port-forward -n sie-555 deployment/sie-555-deployment 8888:8888
```