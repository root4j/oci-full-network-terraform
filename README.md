# OCI Full Network Terraform IaC
This Terraform code deploys a networking scheme in OCI to manage Kubernetes and other required deployments. It consists of five subnets, which are divided into the following categories.

- *SUBNET_PUBLIC:* This network is for public purposes, in case it is necessary to deploy a resource that can be used from any point (for example, a VPN).
- *SUBNET_PRIVATE:* This network is for private purposes, in case it is necessary to deploy a resource that can be used internally (for example, a database).
- *SUBNET_API:* This is a public network used for an OKE (Oracle Kubernetes Engine) deployment. This network must be assigned to the Kubernetes API.
- *SUBNET_NODE:* This is a private network used for an OKE (Oracle Kubernetes Engine) deployment. This network should be assigned to the nodes. It's good practice to keep Kubernetes nodes on private networks.
- *SUBNET_SVC:* This is a public network used for an OKE (Oracle Kubernetes Engine) deployment. Esta red se debe asignar a los servicios que se requieran adiconales como por (ejemplo balanceadores de carga).

## Tools
[![Tools](https://skillicons.dev/icons?i=github,terraform&theme=dark)](https://registry.terraform.io/providers/oracle/oci/latest/docs)

## Execute Terraform Template
[![Deploy to Oracle Cloud](https://oci-resourcemanager-plugin.plugins.oci.oraclecloud.com/latest/deploy-to-oracle-cloud.svg)](https://cloud.oracle.com/resourcemanager/stacks/create?zipUrl=https://github.com/oci-ht/oci-network-terraform/archive/refs/tags/1.0.zip)