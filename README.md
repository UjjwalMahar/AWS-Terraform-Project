#  **AWS-Terraform-Project** 

---

# Infrastructure Deployment Steps with Terraform

This repository contains the necessary instructions and Terraform code to deploy an infrastructure stack on a cloud provider using Terraform. The following steps will guide you through the process of creating a VPC, internet gateway, custom route table, subnet, security group, network interface, elastic IP, and an Ubuntu server with Apache2 installed and enabled.

## Prerequisites

Before starting the deployment process, make sure you have the following prerequisites:

- Terraform installed on your local machine. You can download it from the official Terraform website.
- An account with the chosen cloud provider.
- Appropriate access and permissions to create the required resources.
- Basic knowledge of Terraform and the cloud provider's infrastructure and networking concepts.

## Deployment Steps

Follow the steps below to deploy the infrastructure stack using Terraform:

### 1. Set Up Terraform and add AWS provider

1. Clone or download this repository to your local machine.
2. Install the necessary Terraform providers by running `terraform init` within the repository's directory.
3. Add your AWS access key , secret key and also the region. 

### 2. Create VPC

1. Open the `main.tf` file.
2. Configure the desired VPC settings, such as CIDR block, name, and other parameters.

### 3. Create Internet Gateway

1. Within the same `main.tf` file, configure the internet gateway settings.
2. Associate the internet gateway with the previously created VPC.

### 4. Create Custom Route Table

1. In the `main.tf` file, configure the custom route table settings.
2. Associate the route table with the VPC.

### 5. Create a Subnet

1. Configure the subnet settings in the `main.tf` file.
2. Associate the subnet with the VPC.

### 6. Create Security Group to Allow Port 22, 80, 443

1. Configure the security group settings in the `main.tf` file.
2. Allow inbound traffic on ports 22(SSH), 80(HTTP), and 443(HTTPS).

### 7. Create a Network Interface in the Subnet

1. Configure the network interface settings in the `main.tf` file.
2. Associate the network interface with the previously created subnet.

### 8. Assign an Elastic IP to the Network Interface

1. Configure the elastic IP settings in the `main.tf` file.
2. Associate the elastic IP with the network interface.

### 9. Create Ubuntu Server and Install/Enable Apache2

1. Configure the Ubuntu server settings in the `main.tf` file.
2. Run `terraform apply` to create the Ubuntu server and install Apache2.

## Conclusion

Congratulations! You have successfully deployed an infrastructure stack on AWS using Terraform. The stack includes a VPC, internet gateway, custom route table, subnet, security group, network interface, elastic IP, and an Ubuntu server with Apache2 installed and enabled. You can now access the Ubuntu server over the internet using the elastic IP and start hosting your websites or applications.

*Please refer to the Terraform documentation and guides provided by your cloud provider for more detailed information on each step and additional customization options.*

