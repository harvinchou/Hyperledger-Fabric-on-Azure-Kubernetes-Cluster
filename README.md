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
1.	...

## Docs 🛠
- [Installation Guide : For customization of microsoft arm template for user defined organisation details.](docs/InstallationGuide.md)

- [Generating Profiles : The admin,msp and connection profiles for orderer and peer.](docs/CreatingProfiles.md)

- [Fabric CA Operations : Step if you wish to create a custom user for fabric ca.](docs/CA.md)
 
      - [Installation Guide](docs/InstallationGuide.md)