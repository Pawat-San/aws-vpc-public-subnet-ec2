# Step by Step: Create VPC + Public Subnet + EC2

## 1. Create VPC
- Go to AWS Console → VPC → Create VPC
- VPC CIDR: 10.0.0.0/16

## 2. Create Subnet
- Public subnet CIDR: 10.0.1.0/24
- Attach to VPC

## 3. Create Internet Gateway
- Create IGW → Attach to VPC

## 4. Update Route Table
- Go to Route Tables
- Add route `0.0.0.0/0` → Target: Internet Gateway

## 5. Launch EC2 Instance
- AMI: Amazon Linux 2
- Subnet: Public Subnet
- Assign public IP: Yes
- Security Group: Allow SSH (22) + HTTP (80)

## 6. Test Connectivity
- SSH into EC2 using public IP
- Try `ping google.com` or run a web server
