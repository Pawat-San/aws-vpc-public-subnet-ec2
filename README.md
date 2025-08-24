# AWS VPC + Public Subnet + EC2

This project demonstrates how to create a simple AWS Virtual Private Cloud (VPC) with:
- **VPC** (10.0.0.0/16)
- **Public Subnet** (10.0.1.0/24)
- **Internet Gateway**
- **EC2 Instance** with public access (via SSH / HTTP)

---

## 📌 Architecture Diagram
![VPC Diagram](diagram.png)

---

## 📖 Documentation
For detailed step-by-step instructions, see:  
👉 [docs/steps.md](docs/steps.md)

---

## 🚀 How to Use
1. Open AWS Management Console.
2. Follow the steps described in `docs/steps.md`.
3. Launch an EC2 instance and test connectivity via public IP.

---

## 💡 Notes
- Security Group: open port **22 (SSH)** and **80 (HTTP)**.
- Don’t forget to **terminate resources** after testing to avoid charges.

---

## 👤 Author
Created by [Pawat-San](https://github.com/Pawat-San)
