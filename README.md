# Task 3: Infrastructure as Code (IaC) with Terraform

## Project Overview

This project demonstrates Infrastructure as Code (IaC) using Terraform and Docker. Terraform is used to provision an Nginx Docker container, verify the deployed resources, inspect Terraform state, and destroy the infrastructure when it is no longer needed.

## Tools Used

- Terraform
- Docker Desktop
- Docker provider for Terraform
- Nginx
- Git and GitHub
- Windows 11 and Git Bash

## Project Structure

```text
elevate-labs-task-3-terraform/
├── main.tf
├── .gitignore
├── README.md
└── screenshots/
```

## How It Works

The Terraform configuration in `main.tf` defines the Docker provider, downloads the `nginx:alpine` image, and creates a container named `terraform-nginx-task3`.

Port `8080` on the local computer is mapped to port `80` inside the container.

## Execution Steps

Initialize the Terraform project:

```bash
terraform init
```

Format and validate the configuration:

```bash
terraform fmt
terraform validate
```

Preview the infrastructure changes:

```bash
terraform plan
```

Create the Docker resources:

```bash
terraform apply
```

Inspect the running container and Terraform state:

```bash
docker ps
terraform state list
```

Open `http://localhost:8080` in a browser to verify the Nginx welcome page.

Destroy the resources when finished:

```bash
terraform destroy
```

Confirm the destruction by checking Docker:

```bash
docker ps -a
```

## Screenshots and Execution Evidence

Execution screenshots are included in the `screenshots/` folder to demonstrate the Terraform workflow.

- Terraform initialization
- Terraform plan
- Successful Terraform apply
- Terraform state inspection
- Running Nginx container
- Successful Terraform destroy

## Key Learnings

- Understanding Infrastructure as Code (IaC)
- Using Terraform providers and resources
- Executing `terraform init`, `plan`, `apply`, and `destroy`
- Understanding Terraform state
- Provisioning and managing Docker containers through Terraform

## Conclusion

Successfully used Terraform to provision and manage a local Docker container. Verified the deployment, inspected Terraform state, and destroyed the provisioned resources.

This project demonstrates the basic infrastructure lifecycle using Infrastructure as Code.

