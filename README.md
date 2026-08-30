# AZ-104 Lab – 18 - Production Azure Infrastructure

## Project Overview

This project documents the design and implementation of a production-style Azure infrastructure as part of my hands-on AZ-104 Administrator training.

The environment was designed to demonstrate key Azure administration concepts including:

* Azure RBAC and least-privilege access
* Azure Storage configuration and security
* Blob containers
* Storage lifecycle management
* Storage redundancy
* Virtual networking
* Network segmentation using subnets
* Network Security Groups (NSGs)
* Virtual Machine deployment
* Azure monitoring and insights
* Cost-conscious resource management

---

# Architecture

![Azure Production Architecture](./architecture/azure-production-architecture.png)

The environment uses a three-tier network design consisting of separate Web, Application, and Database subnets.

```text
Internet
   |
   v
Web Subnet
   |
   v
Application Subnet
   |
   v
Database Subnet
```

Network Security Groups were used to control and restrict traffic between the different network tiers.

---

# Technologies Used

* Microsoft Azure
* Azure Virtual Networks
* Azure Subnets
* Network Security Groups (NSGs)
* Azure Storage Accounts
* Azure Blob Storage
* Azure RBAC
* Azure Virtual Machines
* Azure Monitor
* Azure Storage Insights

---

# Azure Storage Configuration

A production-style Azure Storage Account was configured to demonstrate secure and cost-conscious storage management.

The storage environment included multiple containers for separating different types of data:

* `web-content`
* `app-data`
* `backups`

Storage security was configured to support secure access and prevent unnecessary anonymous access.

Additional configuration included:

* Secure transfer
* TLS security configuration
* Private container access
* Lifecycle management
* Locally Redundant Storage (LRS)

---

# Storage Lifecycle Management

Azure Storage Lifecycle Management was configured to demonstrate automated storage optimisation.

Lifecycle policies can automatically move older data to more cost-effective storage tiers based on defined conditions.

This demonstrates how Azure administrators can help manage storage costs while maintaining appropriate data availability.

---

# Identity and Access Management

Azure Role-Based Access Control (RBAC) was configured using the principle of least privilege.

Rather than assigning unnecessary administrative permissions, access was designed around the permissions required for specific responsibilities.

Key concepts demonstrated:

* Role-Based Access Control
* Least-privilege access
* Resource-level permissions
* Controlled administrative access

---

# Production Virtual Network

A production Virtual Network was created to provide network isolation and segmentation.

## Virtual Network

**VNet:** `vnet-prod`

The network was divided into three separate subnets:

| Subnet     | Purpose          |
| ---------- | ---------------- |
| `snet-web` | Web tier         |
| `snet-app` | Application tier |
| `snet-db`  | Database tier    |

This structure demonstrates a common three-tier application architecture.

---

# Network Security Groups

Network Security Groups were created and associated with the appropriate subnets.

The environment included:

* `nsg-web`
* `nsg-app`
* `nsg-db`

The NSGs were used to control network traffic between the different tiers.

The intended traffic flow was designed as:

```text
Internet
   ↓
Web Tier
   ↓
Application Tier
   ↓
Database Tier
```

This approach helps reduce unnecessary network exposure and supports network segmentation.

---

# Virtual Machine Deployment

A small Azure Virtual Machine was deployed in the Web subnet as part of the practical lab environment.

The VM was used as a short-lived resource to demonstrate:

* Azure VM deployment
* VNet integration
* Subnet placement
* NSG association
* Basic production infrastructure design

The VM was intentionally treated as a temporary resource to help keep the lab environment cost-conscious.

---

# Monitoring and Observability

Azure monitoring capabilities were reviewed using Azure Storage monitoring and Insights.

The monitoring environment provides visibility into areas such as:

* Storage activity
* Transactions
* Capacity
* Availability
* Performance metrics

Monitoring is an important part of Azure administration because it helps administrators identify potential issues and understand resource behaviour.

---

# Cost Optimisation

Cost awareness was considered throughout the implementation of this lab.

The following decisions helped keep the environment cost-conscious:

* Standard storage configuration
* Locally Redundant Storage (LRS)
* Minimal test data
* Avoiding unnecessary services
* Using a short-lived Virtual Machine
* Avoiding unnecessary additional monitoring resources

This project demonstrates that cloud infrastructure should be designed with both technical requirements and cost management in mind.

---

# Screenshots

## Azure Storage

![Storage Account](screenshots/01-storage-account.png)

## Storage Containers

![Storage Containers](screenshots/02-storage-containers.png)

## Storage Security

![Storage Security](screenshots/03-storage-security.png)

## Storage Lifecycle Management

![Storage Lifecycle](screenshots/04-storage-lifecycle.png)

## Storage Redundancy

![Storage Redundancy](screenshots/05-storage-redundancy.png)

## RBAC and Least Privilege

![RBAC](screenshots/06-rbac-least-privilege.png)

## Production Virtual Network

![VNet](screenshots/07-production-vnet.png)

## Network Subnets

![Subnets](screenshots/08-subnets.png)

## NSG Associations

![NSG Associations](screenshots/09-nsg-associations.png)

## Network Security Rules

![NSG Rules](screenshots/10-nsg-rules.png)

## Virtual Machine

![VM Overview](screenshots/11-vm-overview.png)

## VM Networking

![VM Networking](screenshots/12-vm-networking.png)

## Storage Monitoring

![Storage Monitoring](screenshots/13-storage-monitoring.png)

---

# Key Skills Demonstrated

Through this project, I gained practical experience with:

* Azure resource management
* Azure Storage administration
* Storage security
* Lifecycle management
* Azure RBAC
* Least-privilege access
* Virtual networking
* Subnet design
* Network Security Groups
* VM deployment
* Azure monitoring
* Cost-conscious cloud administration

---

# Conclusion

This project represents a hands-on production-style Azure infrastructure deployment completed as part of my AZ-104 Administrator learning journey.

The lab combined identity management, storage, networking, security, compute, monitoring, and cost management into a single Azure environment.

The goal was not simply to create Azure resources, but to understand how these services work together in a structured and secure infrastructure design.
## Project Evidence

### Resource Management

![Resource Group](screenshots/01-resource-management/01-resource-group.png)

![Resource Group Resources](screenshots/01-resource-management/02-resource-group-resources.png)

![Resource Tags](screenshots/01-resource-management/03-resource-tags.png)

### Networking

![Virtual Network](screenshots/02-networking/01-virtual-network.png)

![Subnets](screenshots/02-networking/02-subnets.png)

![Network Security Group](screenshots/02-networking/03-network-security-group.png)

### Security

![Security Configuration](screenshots/03-security/01-nsg-security-rules.png)

### Monitoring

![Azure Insights](screenshots/04-monitoring/01-azure-insights.png)

### Governance & Cost Management

![Azure Policy](screenshots/05-governance-cost/01-azure-policy.png)

![Cost Management](screenshots/05-governance-cost/02-cost-management.png)
