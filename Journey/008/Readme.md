
![placeholder image](tflogo.png)

# Terraform Getting Started Azure Part 2 - Build Infrastructure

## Introduction

Terraform is used heavily for deploying Infrastructure as Code at my place of work . I have followed various tutorials online but wanted to go through the offical HashiCorp getting started tutorial. 

## Prerequisite

Terraform installed (see day 1) , VSCode installed and Azure Cli. 

## Use Case

Learn Terraform so I can deploy IaC. 

## Deploy a Resource group in Azure

- Had to update Terraform using Choco 
- Logged into Azure - Az login from terminal 
- Created a folder locally , created a main.tf file
- Used code from tutorial to create Resource Group

```
# configure the Azure provider
terraform {
  required_providers {
    azurerm = {
      source = "hashicorp/azurerm"
      version = ">= 2.26"
    }
  }

}

# specify provider
provider "azurerm" {
  features {}
}

# resource block 
resource "azurerm_resource_group" "rg" {
  name     = "myTFResourceGroup"
  location = "uksouth"
}

```

- Run terraform plan ,  terminal shows plan - 1 to add , 0 to change, 0 to destory
- Run terraform apply , confirmed changes by typing yes
- Comfirmed changes by checking Azure Portal 
- Inspect State , terraform writes to terraform.tfstate, so it can manage or destroy resources later. The file conains all th data in the config. For large projects state would be storage remotely to enable collab. 

### Notes on code to deploy Resource Group
\
Resource blocks are used  to define infrastructure  , the above is a block  to create a resource group. This block has two labels 1. the resource type in this case a resource group "azurerm_resource_group" 2. the label for the block . "rg"


