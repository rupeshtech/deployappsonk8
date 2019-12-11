# Deploy apps on AKS - goazure Meetup

## Assignment-4: Create Deployments

Steps:

### 4.1 Update DeploymentDefinition file

Open DeploymentDefinition.yaml file and update "yourmeetupname"

### 4.2 Create Deployment

run below command

```sh
kubectl apply -f .\4.Createdeployment\DeploymentDefinition.yaml
kubectl get deployments
```

### 4.3 Apply port forwarding

```sh
kubectl port-forward deployment/myapp-deployment 3001:80
```

### 4.4 browse the application

open browser and browse localhost:3001

### 4.5 Browse kubernetes dashboard

browse Kubernetes dashboard and see deployment and no of pods.

### 4.6 Upscale number of pods

Go to Deployment definiton file and change replica to 10

run below command

```sh
kubectl apply -f .\4.Createdeployment\DeploymentDefinition.yaml
```

### 4.7 Browse kubernetes dashboard

browse Kubernetes dashboard and see deployment and no of pods.
