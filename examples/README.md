
# Examples

## Overview

The `examples` directory provides complete reference implementations demonstrating how to consume the reusable Terraform modules contained within this repository.

These examples accelerate onboarding, simplify learning, and act as tested deployment references.

---

## Directory Structure

```
examples/
│
├── hub-network/
├── spoke-network/
├── virtual-machine/
├── key-vault/
├── storage-account/
├── app-service/
├── aks/
├── private-endpoint/
├── complete-landing-zone/
└── README.md
```

---

# Purpose

Each example demonstrates:

- Required inputs
- Optional inputs
- Outputs
- Best practices
- Recommended architecture

---

# Example Categories

## Hub Network

Shows deployment of:

- Virtual Network
- Firewall
- Bastion
- VPN Gateway
- Route Tables

---

## Spoke Network

Shows:

- Spoke VNet
- NSGs
- Peering
- Subnets

---

## Virtual Machine

Deploy:

- Windows VM
- Linux VM
- Managed Identity
- Diagnostics
- Extensions

---

## Key Vault

Example includes:

- Secrets
- RBAC
- Private Endpoint
- Soft Delete
- Purge Protection

---

## Storage Account

Demonstrates:

- Private Endpoint
- Firewall
- Lifecycle Policies
- Encryption

---

## App Service

Deploy:

- App Service Plan
- Web App
- Managed Identity
- Private Endpoint

---

## AKS

Deploy:

- AKS Cluster
- Node Pools
- Azure CNI
- Azure Monitor
- Managed Identity

---

## Private Endpoint

Example resources:

- Storage
- SQL
- Key Vault
- Cosmos DB

---

## Complete Landing Zone

Full enterprise deployment including:

- Management Groups
- Policies
- Networking
- Monitoring
- Security
- Shared Services
- Identity

---

# Running an Example

```
cd examples/virtual-machine
```

```
terraform init
```

```
terraform plan
```

```
terraform apply
```

---

# Example Structure

```
virtual-machine/

main.tf

variables.tf

outputs.tf

terraform.tfvars

README.md
```

---

# Best Practices

Examples should:

- Be minimal
- Be readable
- Demonstrate production patterns
- Avoid unnecessary complexity
- Use reusable modules only

---

# Learning Path

Recommended order:

1. Storage Account

2. Virtual Network

3. Key Vault

4. Virtual Machine

5. Private Endpoint

6. App Service

7. AKS

8. Complete Landing Zone

---

# Notes

Examples are reference implementations.

Production deployments should use:

```
terraform/environments/
```

instead of directly deploying from examples.

---

# Contribution Guidelines

Every new module should include:

- At least one working example
- Documentation
- Variables
- Outputs
