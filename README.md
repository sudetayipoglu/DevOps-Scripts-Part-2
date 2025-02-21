📌 **Introduction**
<br><br>
This repository contains essential DevOps &amp; Cloud Engineering scripts for automation, infrastructure as code and monitoring. These scripts demonstrate best practices in DevOps and cloud automation, making this repository a valuable asset for any Cloud Engineer or DevOps professional.
# DevOps-Scripts-Part-2
🔹 **Infrastructure as Code (IaC)**
<br><br>
**Terraform Script - AWS EC2 Instance Deployment**
```yaml
# Define the AWS provider and region
provider "aws" {
  region = "us-east-1"
}

# Create an EC2 instance with the specified AMI and instance type
resource "aws_instance" "web" {
  ami           = "ami-12345678"  # Replace with the correct AMI ID
  instance_type = "t2.micro"       # Define instance size

  # Assign a name tag for identification
  tags = {
    Name = "WebServer"
  }
}
```
✅ **Usage:**
```yaml
terraform init   # Initialize Terraform
terraform apply  # Apply the configuration and create resources
```
🔹 **Security & Compliance**
<br><br>
**Linux Security Check (Bash Script)**
```yaml
#!/bin/bash
# Check the number of failed login attempts
echo "Checking failed login attempts..."
grep "Failed password" /var/log/auth.log | wc -l

# Check the permissions of the sudoers file
echo "Checking sudoers file permissions..."
ls -l /etc/sudoers
```
✅ **Usage:**
```yaml
chmod +x security-check.sh
./security-check.sh
```

