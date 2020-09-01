---
layout: default
title: Technical Resources
nav_order: 3
---
# Technical Content for Consultants & Engineers

> DISCLAIMER  
> The collated set of guidance on this page is here for your convenience. Please note that best efforts are taken
> to keep the information and guidance on this page up to date but there is potential for it to become outdated 
> or inaccurate. Please always refer to a Microsoft corporate managed website for the most up to date, reliable information.

## Introduction
Development of WVD capabilities is progressing at a rapid pace. For technical consultant teams, keeping across the latest guidance, features and configuration options is important to ensure your customers are getting the best value for their money while also ensuring business & non-functional requirements are also met.

To be good with WVD, you need knowledge in multiple areas including Azure, M365, Windows Server, Active Directory Domain Services, Azure Active Directory and more. Find links below covering material you should be familiar with.

## Service History & Context
The original WVD service in Azure has been Generally Available since 2019. While this version of WVD worked great, it was cumbersome to deploy and manage. This version was referred to as the "Fall 2019 update" but is now referred to as "WVD Classic"

The current WVD service is a fully native Azure resource which makes deployment and management much simpler, allowing use of ARM templates, Azure RBAC, Azure PowerShell and all the other Azure services you're familiar with. It was referred to as the "Spring 2020 update" but is now just known as "WVD" or in comparison to the original, as "ARM-based WVD".

Guidance from here on is to deploy any new WVD environment using ARM based WVD and to migrate away from or decommission any "original" WVD deployment as soon as feasible. See the Migration section for more detail.

### Whats new in ARM WVD? 

| Title                            |  Content  |  Link                                                    |
| -------------------------------- | --------- |--------------------------------------------------------- |
| Overview of the changes with the new WVD | Video (7 mins) | [Windows Virtual Desktop updates for admins (2020)](https://www.youtube.com/watch?v=zmsTD9Hd-xY) |
| Azure Friday WVD Overview  | Video (25 mins) | [Enabling secure remote work using Windows Virtual Desktop](https://www.youtube.com/watch?v=dL1LpGpGRIo) |
  


  

## WVD Requirements

At the highest level, WVD deployments need:
- an Active Directory domain in sync with an Azure Active Directory domain
- an Azure subscription with connectivity to the synchronized Active Directory domain
- M365 licensing for the intended end-users  

More detail about requirements and a sample / reference architecture can be found here:  
[WVD Requirements Overview](https://docs.microsoft.com/en-us/azure/virtual-desktop/overview#requirements)   


## Customer Environment Requirements

| Title                            |  Content  |  Link                                                    |
| -------------------------------- | --------- |--------------------------------------------------------- |
| Client-side network requirements | Webpage   | [Client connect networking](https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/network-guidance) |
| Session host sizing guidelines   | Webpage  | [VM Sizing Guidelines](https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/virtual-machine-recs) |
| Customer experience estimator tool | Web tool | [Customer experience estimator](https://azure.microsoft.com/en-us/services/virtual-desktop/assessment/) |


## Architecture

### Reference Architectures

| Title                            |  Content  |  Link                                                    |
| -------------------------------- | --------- |--------------------------------------------------------- |
| WVD at Enterprise Scale | Website   | [Architecture Reference](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/wvd/windows-virtual-desktop#architecture/) |
| Multiple Active Directory Forests | Webpage   | [Architecture Reference](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/wvd/multi-forest) |
| Multiple Forests with Azure AD DS | Webpage  | [Architecture Reference](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/wvd/multi-forest-azure-managed) |



### Azure Landing Zones
The WVD session host VMs deployed in Azure won't exist in isolation and likely won't be the only workload your customer ever has in Azure. You should be familiar with recommended practices regarding the initial setup and deployment of shared resources within an Azure environment to ensure your customer's business requirements are met and they are well positioned to adopt additional Azure workloads in the future.

These concepts are well covered in the Ready pillar of the Cloud Adoption Framework for Azure:  
[Cloud Adoption Framework For Azure: Ready](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/)


You'll also want to ensure the Azure environment is configured securely. See the security section for more info.


### Azure WVD Resources
Workspaces, Host Pools and App Groups all constitute resources in a WVD deployment.  
Read more about them here: [WVD ARM Resources](https://docs.microsoft.com/en-us/azure/virtual-desktop/environment-setup)


## Image Management
While you can absolutely deploy WVD session hosts using standard VM images from the Azure gallery, more often than not, customized images are preferred preconfigured with the exact set of applications and settings that a customer requires. See the Image Management section for more.


## Azure Active Directory
When logging into the WVD service, users get authenticated against Azure AD first and their allocated licenses checked there to confirm they are permitted to access the service. Knowledge of how to leverage Azure AD authentication options and security features like password hash authentication, seamless single sign-on, multifactor authentication (MFA), conditional access and more will provide your customers users a better experience while keeping them secure.  


## Active Directory Domain Services
As the session host VMs are required to be Domain-Joined, knowledge of Active Directory capabilities and related features such as Group Policy, DNS, etc is very handy.  


## Endpoint Management
How will you be performing OS updates? Installing the latest applications? Changing settings?

## Profile Management
FSLogix Content
Storage options

## Migration

| Title                            |  Content  |  Link                                                    |
| -------------------------------- | --------- |--------------------------------------------------------- |
| Microsoft Mechanics: VDI Migration | Video (14 mins)   | [How to Migrate VDI to WVD](https://www.youtube.com/watch?v=rkKaWT-tN54) |
| Christiaan Brinkhoff: VDI Migration | Video (51 mins) | [Accelerate VDI Migration to WVD](https://www.youtube.com/watch?v=T9oJFsHcnLM&feature=youtu.be&t=86) |

## Automation

