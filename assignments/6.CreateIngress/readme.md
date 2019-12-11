# Deploy apps on AKS - goazure Meetup

## Assignment-6: Create Ingress

Steps:

### 6.1 Update IngressDefinition file

Open IngressDefinition.yaml file and update <yourmeetupname>

### 6.2 Create ingress

Run below command

```sh
kubectl apply -f .\6.CreateIngress\IngressDefinition.yaml
kubectl get ing
```

### 6.3 Update host file

host file is located in windows at "C:\Windows\System32\drivers\etc\hosts"

```sh
104.40.159.19 <yourmeetupname>.meetupdemo.goazure.com
```

### 6.4 browse the application

Open browser and browse <yourmeetupname>.meetupdemo.goazure.com