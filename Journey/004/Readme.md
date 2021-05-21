# Azure Virtual Machines 

## Introduction

Learn how to deploy a Windows Virtual Machine via the Azure Portal.

## Use Case

Learn about Virtual Machines in Azure and create some. 

## Cloud Research

* Which VM workload option is best to run a network appliance on?

  A compute optimised VM should be used to run a network appliance. These VMs have a high CPU to memory ratio. There are 6 VM sizes and you can filter them in the portal by "Family". General purpose, Compute optimised , memory optimised, storage optimised, GPU, High performance computes.
  
* Is an ARM template a JSON file?
  
  JSON is Javascript Object Notation that is human readable to store and transmit data objects. ARM templates are written in JSON they are used to automate deployment of resources in Azure. It is a form on Infrastructure as Code as is declarative - meaning you can state what you want deployed without having to write the steps out. 
  
* What is Azure Backup?
  
  Its a backup as a service, that protects physical and virtual machines on prem or in the cloud. 

  Usage : 

  * Files and folders on Windows OS - physical or virtual, local or cloud.
  * Application aware snapshots
  * Server workloads - SQL, SP, Exchange
  * Support for Azure VMs - Win and Linux
  * Client machines - Linux and Win 10

* What are some advantages of using Azure Backup?

  * Pay for what you use
  * Auto allocation 
  * Local redundant storage - data exisits in same region or geo redundant 
  * Data transfer in and out , unlimited
  * Data encryption 
  * Long term rentention - no length of time  , limit
  
* What is availability?
  
  Percentage of time a service is available for use

* What is an availability set?
  
  To avoid a single point of failure MS recommend deploying at least 2 instances of a each VM, this feature is called an availability set. 

  It is a logical feature used to ensure groups of VMs are deployed so there isnt a single point of failure and not all upgraded at the same time. VMs in an availability set should be the same. MS provide 99.95% connectivity SLA for these. There must be at least two instances of the VM deployed in the set. 

  Availability sets are created in the Azure portal under the disaster recovery section. 

* What is a fault domain?
  
  When you put a VM in a Availability set , Azure spreads them across Fault domains and Update domains. 

  A fault domain is a logical group of hardware in Azure that shares a set of hardward components, that share a single point of failure. You can picture it as a rack within an on prem DC. The first two VMs in an AV set will put put in two different racks. 

* What is an update domain?
  
  An update domain is a logical group of hardware that can undergo maintenance or be rebooted at the same time. 

## Try yourself

I followed this guide on Microsoft Learn to create a VM in the Azure Portal \
https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-virtual-machines/3-create-a-vm
