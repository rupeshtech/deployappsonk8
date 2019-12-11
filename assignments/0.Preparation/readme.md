# Deploy apps on AKS - goazure Meetup

## Assignment-0: Preparation

### Step 0.1: Download & Install VS Code (optional)

[Download Link](https://code.visualstudio.com/download)

### Step 0.2: Download & Install Docker

[Windows Direct download exe](https://goazurestrg.blob.core.windows.net/meetup/Docker_for_Windows_Installer.exe)
[Thru Docker Website](https://www.docker.com/products/docker-desktop)

--- for windows----

[if you get error "Hyper-V and Containers features are not enabled" then go to "Turn Windows features on-off" ('Windows-onderdelen') and check "Hyper-V"](https://goazurestrg.blob.core.windows.net/meetup/HyperVNotEnable.PNG)

[Enable HyperV](https://goazurestrg.blob.core.windows.net/meetup/EnableHyperV.jpg)

--------------------------

### Step 0.3: Test Docker

```sh
docker version
```

### Step 0.4: Download & Install VS Azure Cli

 This will install Az command and Modules

[Download Link](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)

### Step 0.5: Test az

```sh
az --help
```

see the subgroups and focus on account,acr and aks
run following command

```sh
az account --help
az aks --help
```

### Step 0.6: Download & Install KubeCtl

#### on Windows

 a. install
[Direct Downloadlink](https://storage.googleapis.com/kubernetes-release/release/v1.16.0/bin/windows/amd64/kubectl.exe)

Thru Curl, run below command

```sh
curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.16.0/bin/windows/amd64/kubectl.exe
```

thru az

```sh
az aks install-cli
```

b. Add the binary in to your PATH

Please add "C:\Users\urname\.azure-kubectl" to your search PATH so the `kubectl.exe` can be found. Following are two options

    Run set PATH=%PATH%; "C:\Users\username\.azure-kubectl" or $env:path += "C:\Users\urname\.azure-kubectl" for PowerShell. This is good for the current command session. for ex:
    set PATH=%PATH%; C:\Users\rkumar\.azure-kubectl

    Update system PATH environment variable by following "Control Panel->System->Advanced->Environment Variables", and re-open the command window. You only need to do it once

#### on macOS

Using hmebrew

```sh
brew install kubectl
```

or

```sh
brew install kubernetes-cli
```

or using Macports on macOS
If you are on macOS and using Macports package manager, you can install kubectl with Macports.

```sh
sudo port selfupdate
sudo port install kubectl
```

or using  curl

```sh
curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.16.0/bin/darwin/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```

### Step 0.7: Test KubeCtl Version

```sh
kubectl version
```
