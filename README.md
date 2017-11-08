# azure-arm-simple-two-vm
Born from a need for quick HOL VMs for customer visits

# What's in here
## [linux-win.template.json](linux-win.template.json)
- Azure ARM template for deploying two VMs
- Windows Server 2016 Datacenter
- Ubuntu 16.04
- Single virtual network for both
- NSGs for each, 3389 for Windows, 22 for Ubuntu
- Auto-shutdown rules for 7p UTC

## [deployer.ps1](deployer.ps1)
- Powershell deployment script
- Takes an array of prefixes
- Those prefixes become the root of the resource names
- Intended usage: `deployer.ps1 -prefixes user,initials,or,some,other,id
- Each item in the list will create a new deployment + resource group