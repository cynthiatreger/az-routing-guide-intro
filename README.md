# Onboarding Guide to Routing in Azure - Intro

## Background & Objective

Coming from the OnPrem world, in this set of articles I will try to share some of my basic but key learnings that helped me a lot in the first months of my Azure networking journey. 

This guide has been inspired by many conversations with customers and colleagues and aims at providing a better understanding of how the routing in Azure is done. The focus will be on private routing in hub & spoke topologies* and will be no breaking news for people already familiar with cloud networking! 

(\* The impact of vWAN on VNET communications is not discussed here, but could become a second guide like this one!)

Along with the point of view shared in these repos, please find some other useful and brilliant resources introducing Cloud Networking :
- Jose Moreno’s recent post highlights the [differences between Cloud and On-Prem Networking](https://blog.cloudtrooper.net/2023/01/21/azure-networking-is-not-like-your-on-onprem-network/)
- John Savill’s latest (v2) [masterclass on Azure Networtking](https://youtu.be/9DuTWSvsLXM)

## Guide Presentation

I have been thinking of many ways to present the following information and have finally decided to propose a **step by step approach**, starting from basic VNET peering connectivity (Part1).

We will build up from there on the impact of adding a **virtual network gateway (Expressroute or VPN)** in an Azure environment and use the examples to clarify some of the **terminology**. 

(Part2? 3?) After that we will see **how traditional On-Prem routing interoperates with Azure routing** when deploying an NVA (a router, firewall, SDWAN hub or IPSec concentrator) and how this can sometimes lead to more complex designs. 

And finally we will address a few **ways to take away some of that complexity** (Part 3? 4?).

Feel free to jump to any section that could be an interest to you!

The pre-requisites are general understanding of Azure Virtual Networks ([VNETs](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)) and of native (non-cloud) networking.





