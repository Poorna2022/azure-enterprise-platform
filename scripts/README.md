
# Scripts

## Overview

The `scripts` directory contains automation scripts that simplify deployment, maintenance, validation, troubleshooting, and operational tasks across the Azure Enterprise Landing Zone.

These scripts are intentionally separated from Terraform to ensure operational activities remain reusable without modifying infrastructure code.

---

## Directory Structure

```
scripts/
│
├── bootstrap/
├── validation/
├── deployment/
├── cleanup/
├── monitoring/
├── networking/
├── security/
├── utilities/
└── README.md
```

---

## Folder Description

### bootstrap/

Initial environment setup.

Examples:

- Install Terraform
- Install Azure CLI
- Install PowerShell Modules
- Authenticate Azure
- Configure backend storage

---

### deployment/

Deployment helper scripts.

Examples:

- Deploy Management Groups
- Deploy Landing Zones
- Deploy Policies
- Deploy Networking
- Deploy Monitoring

---

### validation/

Infrastructure validation scripts.

Examples:

- Resource validation
- Tag validation
- Naming validation
- Policy compliance
- State verification

---

### cleanup/

Environment cleanup scripts.

Examples:

- Remove test resources
- Delete orphaned resources
- Destroy development environments

---

### monitoring/

Monitoring automation.

Examples:

- Configure alerts
- Enable diagnostics
- Export dashboards
- Configure Log Analytics

---

### networking/

Networking utilities.

Examples:

- DNS validation
- Connectivity testing
- NSG rule checks
- Route verification

---

### security/

Security automation.

Examples:

- RBAC validation
- Key Vault access checks
- Defender onboarding
- Policy verification

---

### utilities/

General helper scripts.

Examples:

- Generate documentation
- Convert YAML
- Merge configuration
- Inventory resources

---

# Supported Languages

Scripts may be written using:

- PowerShell
- Bash
- Python
- Azure CLI

---

# Script Naming Convention

Use descriptive names.

Examples:

```
deploy-hub-network.ps1

validate-tags.ps1

cleanup-dev-environment.ps1

configure-alerts.sh

generate-inventory.py
```

---

# Best Practices

✔ Scripts should be idempotent

✔ Add comments

✔ Validate input

✔ Support logging

✔ Return exit codes

✔ Avoid hardcoded values

✔ Use parameters whenever possible

---

# Logging

Scripts should support logging.

Example:

```
logs/

deploy.log

validation.log

cleanup.log
```

---

# Error Handling

Recommended:

- Try/Catch
- Exit Codes
- Verbose Output
- Validation Checks

---

# Security Guidelines

Never store:

- Passwords
- Secrets
- Tokens
- Certificates
- Keys

Retrieve secrets from Azure Key Vault whenever required.

---

# Usage Example

PowerShell

```powershell
.\deploy-hub-network.ps1 `
    -Environment prod `
    -Location eastus
```

Azure CLI

```bash
./deploy-monitoring.sh prod eastus
```

Python

```bash
python generate_inventory.py
```

---

# Recommended Tools

- Azure CLI
- PowerShell 7+
- Python 3.x
- Terraform CLI
- jq
- yq

---

# CI/CD Integration

Scripts are designed to execute from:

- Azure DevOps
- GitHub Actions
- Jenkins
- Local Developer Machine

---

# Contributing

Before adding scripts:

- Add documentation
- Test locally
- Validate idempotency
- Follow naming standards
