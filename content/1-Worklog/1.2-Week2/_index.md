---
title: "Week 2 Worklog"
date: 2026-06-22
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Understand core networking concepts on AWS using Amazon Virtual Private Cloud (VPC).
* Practice building isolated network infrastructure, configuring Route Tables, Internet Gateways, and security firewall layers.

### Tasks to be implemented this week:

| Day | Tasks | Start Date | End Date | Resource Links |
| :---: | :--- | :---: | :---: | :--- |
| **Mon** | - Learn Amazon VPC overview and IP address planning using CIDR Notation <br> - Differentiate Public Subnet and Private Subnet concepts | 22/06/2026 | 22/06/2026 | Amazon VPC Guide |
| **Tue** | - Study operational mechanics of Internet Gateway (IGW) and Route Tables <br> - Research secure Internet connectivity solutions for Private Subnets using NAT Gateways | 23/06/2026 | 23/06/2026 | VPC Networking Guide |
| **Wed** | - Differentiate Security Groups (Stateful) and Network ACLs (Stateless) firewalls <br> - **Hands-on:** Provision custom VPC, Public Subnet, and Private Subnet | 24/06/2026 | 24/06/2026 | Security Best Practices |
| **Thu** | - **Hands-on:** Create & attach Internet Gateway to VPC, configure Public Route Table, provision NAT Gateway for Private Subnet | 25/06/2026 | 25/06/2026 | VPC Hands-on Lab |
| **Fri** | - **Hands-on:** Launch EC2 instances in Public & Private Subnets, test Internet outbound access via NAT Gateway, configure SG & NACL | 26/06/2026 | 26/06/2026 | VPC Lab Testing |

### Week 2 Achievements:

* Gained deep insight into building secure VPC cloud networks for web applications.
* Successfully built a standard VPC architecture featuring Public Subnet (Web/Load Balancer) and Private Subnet (Backend/Database).
* Configured NAT Gateway enabling Private Subnet resources to fetch software updates without exposure to inbound traffic.
* Correctly configured Security Groups and Network ACLs to ensure network access security.