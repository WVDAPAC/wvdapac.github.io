---
layout: default
title: Architecture
nav_order: 1
parent: Technical Resources
---

![WVD APAC](/images/wvdlogo.jpg "Windows Virtual Desktop")  
## Tech Resources: Architecture

### Reference Architectures

| Title                            |  Content  |  Link                                                    |
| -------------------------------- | --------- |--------------------------------------------------------- |
| WVD at Enterprise Scale | Website   | [Architecture Reference](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/wvd/windows-virtual-desktop#architecture/) |
| Multiple Active Directory Forests | Webpage   | [Architecture Reference](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/wvd/multi-forest) |
| Multiple Forests with Azure AD DS | Webpage  | [Architecture Reference](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/wvd/multi-forest-azure-managed) |
| WVD Resources & Relationships | LinkedIn Article | [WVD Resources & Relationships](https://www.linkedin.com/pulse/wvd-windows-virtual-desktop-resources-relationships-peter-smallbone/?trackingId=UVa5n22cSmeQ5i8aUx9cTw%3D%3D) |


### Azure Landing Zones
The WVD session host VMs deployed in Azure won't exist in isolation and likely won't be the only workload your customer ever has in Azure. You should be familiar with recommended practices regarding the initial setup and deployment of shared resources within an Azure environment to ensure your customer's business requirements are met and they are well positioned to adopt additional Azure workloads in the future.

These concepts are well covered in the Ready pillar of the Cloud Adoption Framework for Azure:  
[Cloud Adoption Framework For Azure: Ready](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/)


You'll also want to ensure the Azure environment is configured securely. See the security section for more info.


### Azure WVD Resources
Workspaces, Host Pools and App Groups all constitute resources in a WVD deployment.  
Read more about them here: [WVD ARM Resources](https://docs.microsoft.com/en-us/azure/virtual-desktop/environment-setup)
