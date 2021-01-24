# Provision an EKS Cluster

This repo is a companion repo to the [Provision an EKS Cluster learn guide](https://learn.hashicorp.com/terraform/kubernetes/provision-eks-cluster), containing
Terraform configuration files to provision an EKS cluster on AWS.

### Pre-requisites
- Download `brew install awscli` on macOS
- aws configure
- Run `brew install terraform`
- `terraform init`
- `terraform apply`, takes around 20-30 minutes
- if nodes are not created and it failes to create nodegroup. You can manually create the nodegroups.
- Copy kubeconfig with `aws eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)`