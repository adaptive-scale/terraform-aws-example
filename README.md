# Provision an EKS Cluster


### Pre-requisites
- Download `brew install awscli` on macOS
- aws configure
- Run `brew install terraform`
- Download kubectl

### Provision a cluster
- `terraform init`
- `terraform apply`, takes around 20-30 minutes
- if nodes are not created and it failes to create nodegroup. You can manually create the nodegroups.
- Copy kubeconfig with `aws eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)`
- Run `kubectl get nodes` to see the nodes in the cluster
