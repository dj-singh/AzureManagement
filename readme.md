# Azure Management scripts
This repository stores some PowerShell scripts for managing Microsoft Azure. Often, it's helpful to use little scripts to manage Azure subscriptions, to get or to deploy resources and to automate specific tasks. I plan to extend this collection from time to time. 

## Install the Azure PowerShell Az module
As prerequesits, you need to have the Azure PowerShell Az module installed on your computer.
The new Azure PowerShell Az module is available since December 2018 and, as the documentation says, offers shorter commands, improved stability, and cross-platform support since it's running on the .NET Standard library which means it runs on PowerShell 5.x and PowerShell 6.x (PS 6.x can run on Linux, macOS, and Windows). I see, "Az" is shorter than "AzureRM"… ;) Anyway, Az also offers feature parity and an easy migration path from AzureRM, see more at [Introducing the new Azure PowerShell Az module](https://docs.microsoft.com/en-us/powershell/azure/new-azureps-module-az?view=azps-1.3.0).

## Connect to Azure
(Un)install or update the PowerShell module, as described at [Working with the new Azure PowerShell Az module](https://blog.atwork.at/post/2019/02/26/The-new-Azure-PowerShell-Az-module) or at [docs.microsoft.com](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-1.3.0). Once installed, use the Connect-AzAccount command and sign-in with your credentials:
```powershell
Connect-AzAccount
```
## See subscriptions
When working with multiple subscriptions, get a list of all subscriptions as here:
```powershell
Get-AzSubscription
```

## Select a subscription
Select the desired Azure subscription by name: 
```powershell
Set-AzContext -Subscription '<subscriptionname>'
```

## Run your scripts
After that, run your PowerShell Az scripts, as for example [get-subscription-inventory.ps1](https://github.com/tonipohl/AzureManagement/blob/master/get-subscription-inventory.ps1).

Happy PowerShell-ing!
