# Onboarding Guide to Routing in Azure - Intro & Structure

- [Episode #1: Azure VNET connectivity reminder, impact of Virtual Network Gateways, propagation options for On-Prem routes](https://github.com/cynthiatreger/az-routing-guide-part1-vnet-peering-and-virtual-network-gateways)

- [Episode #2: ~~VM Routing~~ NIC Routing ](https://github.com/cynthiatreger/az-routing-guide-ep2-nic-routing)

- [Episode #3: NVA Routing Fundamentals](https://github.com/cynthiatreger/az-routing-guide-ep3-nva-routing-fundamentals)

- [Epsidode #4: Chained NVAs and BGP](https://github.com/cynthiatreger/az-routing-guide-ep4-chained-nvas-bgp)

- [Episode #5: NVA Routing 2.0 with IPSEC/VxLAN & Azure Route Server](https://github.com/cynthiatreger/az-routing-guide-ep4-nva-routing-2-0)
##
## Background & Objective

Coming from the On-Prem, I will try to share in this set of articles some of my basic but key learnings that helped me a lot in the first months of my Azure Cloud Networking journey. 

This guide has been inspired by many conversations with customers and colleagues and aims at providing a better understanding of the routing mechanisms in Azure and how they translate from On-Prem networking. 

The focus will be on private routing in hub & spoke topologies*. For clarity, network security and resiliency best practices as well as internet breakout considerations have been left out of this guide.

The pre-requisites are general understanding of Azure Virtual Networks ([VNETs](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)) and of native (non-cloud) networking.

Along with the point of view shared in these repos, please check out the following recent and insightful resources on Azure Networking :
- Jose Moreno’s recent post highlights the [differences between Cloud and On-Prem Networking](https://blog.cloudtrooper.net/2023/01/21/azure-networking-is-not-like-your-on-onprem-network/)
- John Savill’s latest (v2) [masterclass on Azure Networtking](https://youtu.be/9DuTWSvsLXM)

\* *The impact of vWAN on VNET and branch communications is not discussed here, and would require an entire series on its own :slightly_smiling_face:. However, in a vWAN tiered VNET design, the upper Spoke and transit VNETs would still follow some of the principles described in this guide.*

## Guide Structure

I have been thinking of many ways to present the information and have finally decided to propose a **step by step approach**, starting from basic VNET peering connectivity and building up from there on the impact of adding a **virtual network gateway (Expressroute or VPN)** and how to influence the propagation of On-Prem routes ([Episode #1](https://github.com/cynthiatreger/az-routing-guide-ep1-vnet-peering-and-virtual-network-gateways)).

[Episode #2](https://github.com/cynthiatreger/az-routing-guide-ep2-nic-routing) will be about clarifying some of the Azure routing elements and the used terminology.

In [Episode #3](https://github.com/cynthiatreger/az-routing-guide-ep3-nva-routing-fundamentals) and [Episode #4](https://github.com/cynthiatreger/az-routing-guide-ep4-chained-nvas-bgp), things will finally start unfolding as we will see **how traditional On-Prem routing interoperates with Azure routing** when deploying NVAs (routers, firewalls, SDWAN hubs or IPSec concentrators) and running BGP, and how this can sometimes lead to more complex designs. 

And finally [Episode #5](https://github.com/cynthiatreger/az-routing-guide-ep4-nva-routing-2-0) will address a few **ways to take away some of that complexity**.

Feel free to jump to any section that could be an interest to you!



