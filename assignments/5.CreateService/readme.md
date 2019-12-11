# Deploy apps on AKS - goazure Meetup

## Assignment-5: Create Service

Steps:

### 5.1 Create Service

run below command

```sh
kubectl apply -f .\5.CreateService\ServiceDefinition.yaml
kubectl get svc
```

### 5.2. Apply port forwarding

```sh
kubectl port-forward service/myapp-svc 3001:80
```

### 5.3. browse the application localhost:3001

Open browser and browse localhost:3001
