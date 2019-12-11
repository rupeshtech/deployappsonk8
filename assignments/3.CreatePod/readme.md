# Deploy apps on AKS - goazure Meetup

## Assignment-3: Creat POD

Steps:

### 3.1  Run below command

```sh
kubectl apply -f .\3.CreatePod\PodDefinition.yaml
kubectl get pods
```

### 3.2 Apply port forwarding

```sh
kubectl port-forward pod/myapp-pod 3001:80
```

### 3.3 Browse the application
 
Open browser and browse localhost:3001

### 3.4 Delete pod

```sh
kubectl delete pod myapp-pod
```

### 3.5 Update PodDefinition file

Open PodDefinition.yaml and change the image name to your image
you can comment line no 10 and uncomment line no 13,14,15 in PodDefinition.yaml

### 3.6 Reapply podDefinition file

Run below command

```sh
kubectl apply -f .\3.CreatePod\PodDefinition.yaml
```

### 3.7 Apply port forwarding

```sh
kubectl port-forward pod/myapp-pod 3001:80
```

### 3.8 Browse application and Kubernetes dashboard

open browser and browse the application localhost:3001

go to kubernetes dashboard or open browser and browse 127.0.o.1:8001

### 3.9 CleanUp

```sh
kubectl get pods
kubectl delete pod myapp-pod
```
