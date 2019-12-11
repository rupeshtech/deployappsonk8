# Deploy apps on AKS - goazure Meetup

## Assignment-2: Connect to Cluster

### 2.1 GetContext

```sh
$rgName="goazure"
$aksName="goazure"
az aks get-credentials --resource-group $rgName --name $aksName
```

### 2.2 Open kubernetes dashboard

Open another terminal (and never close it) and run following command

```sh
az aks browse --resource-group goazure --name goazure
```

### 2.3 Create Namespace

```sh
kubectl config get-contexts
kubectl config use-context $aksName
kubectl get namespaces
$mynamespace="<yourmeetupname>"
kubectl create namespace $mynamespace
```

### 2.4 Set default namespace

```sh
kubectl config set-context --current --namespace=$mynamespace
```

go to kubenetes dashboard and see if u namespace is created [example link]
