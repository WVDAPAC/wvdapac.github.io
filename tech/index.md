---
layout: default
title: Technical Resources
nav_order: 3
has_children: yes
---

![WVD APAC](/images/wvdlogo.jpg "Windows Virtual Desktop")  
# Technical Enablement & Resources

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


