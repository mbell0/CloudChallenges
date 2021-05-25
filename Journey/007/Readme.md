
![placeholder image](tflogo.png)

# Terraform Getting Started Azure Part 1

## Introduction

Terraform is used heavily for deploying Infrastructure as Code at my place of work . I have followed various tutorials online but wanted to go through the offical HashiCorp getting started tutorial. 

## Prerequisite

Terraform installed (see day 1) , VSCode installed and exts installed. 

## Use Case

Learn Terraform so I can deploy IaC. 

## Research

- Terraform is an Infrastructure of code tool made by HashiCorp. It is used for building, changing and managing infrastructure in a safe and repeatable way. It is written in HCL (HashiCorp Language) .
- You can use it to deploy resources rather than working in the Azure Portal.
- Terraform workflow - Scope confrim resources that need creating, Author create the config file , Intialise the directory by running terraform init (will download correct plug ins for provider), Plan and apply the changes , terraform plan , terraform apply. 
- Advantages of TF 
  - Platform agnostic can be used with AWS, GCP and others 
  - State management 
    - TF creates a state file when initialised its used to create plans and change the infra. 
    - Operator confidence 
      - Easily repeatable operations and planning to ensure actions do not cause disruption. 

## Provision a NGINX server using Docker 

I followed this tutorial on the Terraform Webiste .

[Provision NGINX Server]([link](https://learn.hashicorp.com/tutorials/terraform/install-cli?in=terraform/azure-get-started))

An NGINX Server is open source software used for web serving, caching, load balancing and more. 

Docker is OS level virtualisation to deliver software in containers. 