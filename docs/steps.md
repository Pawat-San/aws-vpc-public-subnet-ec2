# Step by Step: Create VPC + Public Subnet + EC2

## 1. Create VPC
- Go to AWS Console → VPC → Create VPC
- Name: `my-vpc`
- CIDR Block: `10.0.0.0/16`

## 2. Create Subnet
- Name: `public-subnet-1`
- VPC: `my-vpc`
- CIDR Block: `10.0.1.0/24`
- Availability Zone: select one (e.g., ap-southeast-1a)

## 3. Create Internet Gateway
- Name: `my-igw`
- Attach to `my-vpc`

## 4. Update Route Table
- Select the route table for `my-vpc`
- Add route:  
  - Destination: `0.0.0.0/0`  
  - Target: Internet Gateway (`my-igw`)
- Associate route table with `public-subnet-1`

## 5. Launch EC2 Instance
- AMI: Amazon Linux 2
- Instance type: t2.micro (Free Tier)
- Network: `my-vpc`
- Subnet: `public-subnet-1`
- Auto-assign Public IP: **Enable**
- Security Group:  
  - Allow **SSH (22)** from your IP  
  - Allow **HTTP (80)** from Anywhere  

## 6. Test Connectivity
- Copy the public IP of the instance
- SSH into instance:
  ```bash
  ssh -i mykey.pem ec2-user@<Public-IP>
