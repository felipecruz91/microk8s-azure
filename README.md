# microk8s-azure

Creates an Ubuntu VM in Azure with the latest version of Microk8s installed.

## Configure parameters file

First of all, set the `adminUsername`, `adminPassword`, and `virtualMachineSize` in the [parameters file](https://github.com/felipecruz91/microk8s-azure/blob/master/azuredeploy.parameters.json).

## Deploy infrastructure

```cli
az login

az account list --output table

az account set --subscription "Visual Studio Professional"

az group create -l westeurope -n MyResourceGroup

az deployment group validate --resource-group <resource-group-name> --template-file <path-to-template> --parameters <path-to-parameters-file>

az deployment group create --resource-group <resource-group-name> --template-file <path-to-template> --parameters <path-to-parameters-file>
```
