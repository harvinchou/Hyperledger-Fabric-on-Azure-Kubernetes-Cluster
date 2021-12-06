# Introduction 
This repo uses Hyperledger Fabric (HLF) Deployer to automate the deployment and configuration of the blockchain environment. HLF Deployer uses Azure Resource Manager template (ARM template) to deploy related resources such as orderer and peer in the Hyperledger Fabric network. This is to standardize and accelerate the deployment of Hyperledger Fabric in Azure China.


# Hyperledger Fabric (HLF) 2.x on Azure Kubernetes Service (AKS)
Forked from:
> Hyperledger fabric developer network on few clicks. This offer is meant to provide Hyperledger Fabric as a Service using ARM Templates to spin off resources inside an AKS cluster. https://github.com/krypc-code/Hyperledger-Fabric-on-Azure-Kubernetes-Cluster


# HLF on Azure China
Please refer to https://docs.microsoft.com/en-us/azure/china/ for the matters needing attention when deploying to Azure China using HLF Deployer.

This repo has made the following customizations for Azure China:
- The certificate to connect to an Azure Database for PostgreSQL server in China is located at https://dl.cacerts.digicert.com/DigiCertGlobalRootCA.crt.pem
- The endpoints to change in Azure China https://docs.microsoft.com/en-us/azure/china/resources-developer-guide#check-endpoints-in-azure
- Microsoft.CustomProviders is not supported in Azure China.
- Access to the internet sites may be blocked in China https://en.wikipedia.org/wiki/Internet_censorship_in_China


# Getting Started
1. **Architecture**
2. **Prerequisites**

## **Azure Linux VM**
<!--- Indent entire section -->
<div style="margin-left: 1.5em;">

### Git

Install the latest version of [git](https://git-scm.com/downloads) if it is not already installed.

```shell
$ sudo apt-get install git
```

### cURL

Install the latest version of [cURL](https://curl.haxx.se/download.html) if it is not already installed.

```shell
$ sudo apt-get install curl
```

### Docker

Install the latest version of [Docker](https://docs.docker.com/get-docker/) if it is not already installed. 

```shell
sudo apt-get -y install docker-compose
```

Once installed, confirm that the latest versions of both Docker and Docker Compose executables were installed.

```shell
$ docker --version
Docker version 19.03.12, build 48a66213fe
$ docker-compose --version
docker-compose version 1.27.2, build 18f557f9
```

Make sure the Docker daemon is running.

```shell
sudo systemctl start docker
```

Optional: If you want the Docker daemon to start when the system starts, use the following:

```shell
sudo systemctl enable docker
```

Add your user to the Docker group.

```shell
sudo usermod -a -G docker <username>
```

#### Go

Optional: Install the latest version of [Go](https://golang.org/doc/install) if it is not already installed
(only required if you will be writing Go chaincode or SDK applications).

#### JQ

Optional: Install the latest version of [jq](https://stedolan.github.io/jq/download/) if it is not already installed
(only required for the tutorials related to channel configuration transactions).

</div>


## Docs 🛠
- [Install HLF Deployer : ](docs/HLFDeployer.md)

- [Deploying Orderer Nodes : ](docs/DeployOrdererNodes.md)

- [Deploying Peer Nodes : ](docs/DeployPeerNodes.md)

- [Generating Profiles : The admin,msp and connection profiles for orderer and peer.](docs/GeneratingProfiles.md)

- [Creating Consortium : Creation of multiple organisations and their crypto materials.](docs/CreatingConsortium.md)

- [Setup Fabric Cli Go : Command line interface for interacting with the blockchain system.](docs/FabricGoCli.md)

- [Channel Operations : Creation of channels and basic operations on them.](docs/ChannelOperations.md)

- [Deploy External Chaincode : Executing chaincode on an external container. This an advanced feature.](docs/ExternalChaincode.md)



