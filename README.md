
# ☁️ AWS Infrastructure with Terraform

This project demonstrates how to **provision, manage, and maintain AWS infrastructure** using **Terraform**.  
The setup is fully modular, enabling clean, reusable code for multiple environments.  
The infrastructure lifecycle (create, update, destroy) is managed entirely via CLI commands, ensuring **automation**, **scalability**, and **reliability**.

---

## 🚀 Highlights
- ⚡ **Provisioned AWS Resources**: EC2 instances, S3 buckets, IAM roles & policies  
- 📦 **Modular Terraform Setup**: Reusable modules for networking, compute, and storage  
- 🖥️ **Infrastructure Lifecycle Management** via Terraform CLI (`plan`, `apply`, `destroy`)  
- 🔒 **Secure Access Management** using IAM roles  
- 🌍 **Scalable Infrastructure** with state management and variables  

---

## 🏗️ Tech Stack
- **Infrastructure as Code (IaC):** Terraform (v1.x)  
- **Cloud Provider:** Amazon Web Services (AWS)  
- **Services Used:**  
  - **EC2** – Compute instances  
  - **S3** – Storage & remote Terraform state backend  
  - **IAM** – User roles, groups, and permissions  

---

## 📂 Project Structure
```

aws-infra-terraform/
│── main.tf               # Root Terraform configuration
│── variables.tf          # Input variables
│── outputs.tf            # Outputs after apply
│── provider.tf           # AWS provider setup
│── modules/              # Modularized infrastructure code
│   ├── ec2/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   ├── s3/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   └── iam/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
│── terraform.tfvars      # Environment-specific variables
│── README.md             # Project documentation

````

---

## ⚙️ How It Works

### 1️⃣ Initialize Terraform
Before provisioning resources, initialize Terraform to download the required AWS provider and set up backend state management.
```bash
terraform init
````

### 2️⃣ Plan Infrastructure

Preview the infrastructure changes before applying:

```bash
terraform plan
```

### 3️⃣ Apply Infrastructure

Provision AWS resources (EC2, S3, IAM) automatically:

```bash
terraform apply
```

### 4️⃣ Destroy Infrastructure

Tear down all resources safely:

```bash
terraform destroy
```

---

## 🔑 Security Considerations

* **AWS Credentials**: Stored securely using environment variables or AWS CLI profiles.
* **Remote State**: Terraform state is stored in an **S3 bucket** for team collaboration.
* **IAM Roles**: Followed the principle of least privilege when creating IAM roles & policies.

---

## 📸 Demo

🔗 [View Project](https://your-project-link.com)

---

## 📚 Best Practices Followed

* ✅ Modular code for **reusability**
* ✅ Separate environments (dev, staging, prod) via `terraform.tfvars`
* ✅ Remote state management with **S3 + DynamoDB lock**
* ✅ Tags added to resources for **cost tracking & organization**

---

## 🧑‍💻 Author

**Hiralal Singh (Charon)**
Founder of **Successor** | Cloud & DevOps Enthusiast

---

