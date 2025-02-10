## Azure Terraform Boilerplate
A minimal, production-ready Terraform configuration for Azure resource deployment.

### Features

Basic Azure resources setup (Resource Group, Storage Account)
Environment-based deployments (DEV, TEST, PROD)
Secure default configurations
State file backend configuration
Proper naming conventions and tagging

### Repository Structure

├── main.tf                # Main resource configurations
├── variables.tf           # Variable definitions
├── versions.tf            # Provider configurations
├── outputs.tf            # Output definitions
├── environments/
│   ├── dev/
│   │   ├── backend.tfvars # Dev backend configuration
│   │   └── terraform.tfvars # Dev variables
│   └── test/
│       ├── backend.tfvars # Test backend configuration
│       └── terraform.tfvars # Test variables

### Setup

1. Login to Azure
| _az login_

2. Initialize Terraform with the appropriate backend configuration
| _terraform init -backend-config=environments/dev/backend.tfvars_

3. Plan your changes
| _terraform plan -var-file=environments/dev/terraform.tfvars_

4. Apply the changes
| _terraform apply -var-file=environments/dev/terraform.tfvars_


