# microk8s-azure

Creates an Ubuntu VM in Azure with the latest version of Microk8s installed.

## Deploy infrastructure

```cli
az login

az account list --output table

az account set --subscription "Visual Studio Professional"

az group create -l westeurope -n MyResourceGroup

az deployment group validate --resource-group <resource-group-name> --template-file <path-to-template> --parameters <path-to-parameters-file>

az deployment group create --resource-group <resource-group-name> --template-file <path-to-template> --parameters <path-to-parameters-file>
```
