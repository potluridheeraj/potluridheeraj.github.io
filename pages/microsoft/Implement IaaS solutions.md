---
title: Implement IaaS solutions
keywords: Microsoft, Az-204
permalink: Implement_IaaS_solutions
folder: microsoft
sidebar: az-204_sidebar
---
## Implement IaaS solutions
### **Provision VMs**
#### test
Quickstart: Create a Windows virtual machine in the Azure portal  
[Tutorial: Create and Manage Windows VMs with Azure PowerShell](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/tutorial-manage-vm?WT.mc_id=thomasmaurer-blog-thmaure)    
How to connect and sign on to an Azure virtual machine running Windows  
Quick steps: Create and use an SSH public-private key pair for Linux VMs in Azure          


{% include note.html content="A resource group must be created before a virtual machine" %}

```powershell
New-AzResourceGroup -ResourceGroupName "myResourceGroupVM" -Location "EastUS"
```

Create the VM with New-AzVM.    
(Windows)
```powershell
New-AzVm `
    -ResourceGroupName "myResourceGroupVM" `
    -Name "myVM" `
    -Location "EastUS" `
    -VirtualNetworkName "myVnet" `
    -SubnetName "mySubnet" `
    -SecurityGroupName "myNetworkSecurityGroup" `
    -PublicIpAddressName "myPublicIpAddress" `
    -Credential $cred
```
(Linux)
```shell
az vm create \
  --resource-group myResourceGroup \
  --name myVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --ssh-key-values mysshkey.pub
```

Return the public IP address of the VM
```powershell
Get-AzPublicIpAddress `
   -ResourceGroupName "myResourceGroupVM"  | Select IpAddress
```
    
Use the Get-AzVMImagePublisher command to return a list of image publishers.    
Use the Get-AzVMImageOffer to return a list of image offers.   
If you are using PowerShell and have the Azure PowerShell module installed you may also connect using the Get-AzRemoteDesktopFile cmdlet, as shown below.  
```powershell
Get-AzRemoteDesktopFile -ResourceGroupName "RgName" -Name "VmName" -Launch
```


```powershell
```
```powershell
``````powershell
``````powershell
``````powershell
``````powershell
``````powershell
``````powershell
``````powershell
```
```powershell
```
```powershell
```
```powershell
```
```powershell
```
```powershell
```
```powershell
```
```powershell
```
```powershell
```
## Getting Started

 pre-requisites:
 - [Vm ware](https://www.vmware.com/) or [Virtualbox](https://www.virtualbox.org/) 
 - [Vagrant](https://www.vagrantup.com/docs/installation/)
