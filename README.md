# Onboarding Guide to Routing in Azure - Intro & Structure

## Background & Objective

Coming from a galaxy far, far away: "***the On-Prem***", I will try to share in this set of articles some of my basic but key learnings that helped me a lot in the first months of my Azure Cloud Networking journey. 

This guide has been inspired by many conversations with customers and colleagues and aims at providing a better understanding of how the routing in Azure is done. The focus will be on private routing in hub & spoke topologies* and will be no breaking news for people already familiar with cloud networking! 

(\* The impact of vWAN on VNET communications is not discussed here, but could become a second guide like this one!)

Along with the point of view shared in these repos, please find some other useful and brilliant resources introducing Cloud Networking :
- Jose Moreno’s recent post highlights the [differences between Cloud and On-Prem Networking](https://blog.cloudtrooper.net/2023/01/21/azure-networking-is-not-like-your-on-onprem-network/)
- John Savill’s latest (v2) [masterclass on Azure Networtking](https://youtu.be/9DuTWSvsLXM)

The pre-requisites are general understanding of Azure Virtual Networks ([VNETs](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)) and of native (non-cloud) networking.

## Guide Structure

I have been thinking of many ways to present the information and have finally decided to propose a **step by step approach**, starting from basic VNET peering connectivity and building up from there on the impact of adding a **virtual network gateway (Expressroute or VPN)** (Episode #1).

Episode #2 will be about clarifying some of the Azure routing elements and the used terminology.

In Episode #3, things will finally start unfolding as we will see **how traditional On-Prem routing interoperates with Azure routing** when deploying NVAs (routers, firewalls, SDWAN hubs or IPSec concentrators) and how this can sometimes lead to more complex designs. 

And finally Episode #4 will address a few **ways to take away some of that complexity**.

Feel free to jump to any section that could be an interest to you!

- [EPISODE #1: DISCOVERY/REMINDER OF AZURE VNET CONNECTIVITY & IMPACT OF VIRTUAL NETWORK GATEWAYS](https://github.com/cynthiatreger/az-routing-guide-part1-vnet-peering-and-virtual-network-gateways)

- [EPISODE #2: ~~VM ROUTING~~ NIC ROUTING ](https://github.com/cynthiatreger/az-routing-guide-part1-vnet-peering-and-virtual-network-gateways)

- EPISODE #3: NVA ROUTING

- EPIDODE #4: NVA ROUTING v2 WITH VXLAN & ROUTE SERVER



