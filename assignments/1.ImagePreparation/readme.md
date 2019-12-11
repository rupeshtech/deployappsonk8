# Deploy apps on AKS - goazure Meetup

## Assignment-1: Prepare Image

In this assignment you have to prepare image. You can also create your own image

### 1.1 Login to Azure

Run following steps

```sh
az login --service-principal --username 255a5fbe-7b77-4b6a-ac18-f3fdb780d84a --password "goazuremeetup@123" --tenant "4da5a05e-4afa-4737-939d-cec520c9244b"
 ```

### 1.2 Pull Image

```sh
az acr login -n goazuremeetup
docker pull goazuremeetup.azurecr.io/demoapp:v1
```

### 1.3 Create container

```sh
docker container run -d -p 3227:80 --name demoapplinux goazuremeetup.azurecr.io/demoapp:v1
```

### 1.4 Browse Application

open browser and browse localhost:3227
ENTER your name and Click Save

### 1.5 Create another Image

```sh
docker container commit demoapplinux "yourmeetupname":v1
```

```sh
docker container run -d -p 3228:80 --name "yourmeetupname" "yourmeetupname":v1
```

open browser and browse localhost:3228

### 1.6 Tag Image

Image needs to be tagges to specific format (acrname.azurecr.io/yourmeetupname:version) if it is to be pushed to Azure container registry

```sh
docker tag "yourmeetupname":v1 goazuremeetup.azurecr.io/"yourmeetupname":v1
```

### 1.7 Push Image

```sh
docker push goazuremeetup.azurecr.io/"yourmeetupname":v1
```
