---
description: This set of Bicep templates demonstrates how to set up an AI Studio Hub with managed vnet enabled. To access the vnet, a VM and Bastion jumphost is set up. 
page_type: sample
products:
- azure
- azure-resource-manager
urlFragment: ai-networking
languages:
- bicep
- json
---
# Azure Machine Learning end-to-end secure setup

This set of templates demonstrates how to set up AI Studio hub end-to-end in a secure set up.

This reference implementation includes the Workspace, a compute cluster, compute instance and attached private AKS cluster. It  includes the configuration of associated resources including Azure Key Vault, Azure Storage, and Azure Container Registry in a network-isolated setup.

## Resources

| Provider and type | Description |
| - | - |
| `Microsoft.Resources/resourceGroups` | The resource group all resources get deployed into |
| `Microsoft.Insights/components` | An Azure Application Insights instance associated to the Azure Machine Learning workspace |
| `Microsoft.KeyVault/vaults` | An Azure Key Vault instance associated to the Azure Machine Learning workspace |
| `Microsoft.Storage/storageAccounts` | An Azure Storage instance associated to the Azure Machine Learning workspace |
| `Microsoft.ContainerRegistry/registries` | An Azure Container Registry instance associated to the Azure Machine Learning workspace |
| `Microsoft.MachineLearningServices/workspaces` | An Azure Machine Learning workspace instance |
| `Microsoft.MachineLearningServices workspaces/computes` | Azure Machine Learning workspace compute types: cluster and compute instance |
| `Microsoft.Network/privateDnsZones` | Private DNS zones for Azure Machine Learning and the dependent resources |
| `Microsoft.Network/networkSecurityGroups` | A Network Security Group pre-configured for use with Azure Machine Learning |
| `Microsoft.ContainerService/managedClusters` | An Azure Kubernetes Services cluster for inferencing |
| `Microsoft.Compute/virtualMachines` | A Data Science Virtual Machine `jumpbox` to access the workspace over the private link endpoint |
| `Microsoft.Network/virtualNetworks` | A virtual network to deploy all resources in |
