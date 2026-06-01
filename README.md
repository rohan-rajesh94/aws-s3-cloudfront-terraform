# AWS S3 + CloudFront Static Website using Terraform

This project demonstrates Infrastructure as Code (IaC) using Terraform to provision an Amazon S3 bucket, upload a static website, and serve it globally through an Amazon CloudFront distribution.

## Architecture

User → CloudFront → S3 Bucket → index.html

## How long did you spend on the exercise?

I spent approximately **5-6 hours** completing this exercise, including:

* Setting up Terraform and AWS CLI
* Creating and testing Terraform configurations
* Deploying AWS resources
* Troubleshooting CloudFront and S3 access issues
* Configuring static website hosting
* Validating the final deployment

### Feedback

This exercise provided practical experience with Infrastructure as Code (IaC) using Terraform. It helped me understand how AWS S3 and CloudFront work together to deliver static website content and gave me hands-on exposure to troubleshooting cloud infrastructure issues.

---

## Detailed Steps to Execute the Terraform Code

### Prerequisites

* AWS Account
* Terraform installed
* AWS CLI installed and configured

### 1. Clone the Repository

```bash
git clone <repository-url>
cd terraform-s3-cloudfront
```

### 2. Configure AWS Credentials

```bash
aws configure
```

Provide:

* AWS Access Key ID
* AWS Secret Access Key
* Default Region (us-east-1)
* Output Format (json)

### 3. Initialize Terraform

```bash
terraform init
```

### 4. Validate Configuration

```bash
terraform validate
```

### 5. Review Execution Plan

```bash
terraform plan
```

### 6. Deploy Infrastructure

```bash
terraform apply
```

Type:

```text
yes
```

when prompted.

### 7. Verify Deployment

Terraform will output:

* S3 Bucket Name
* CloudFront Distribution URL

Open the CloudFront URL in a browser to verify that the website is being served successfully.

### 8. Destroy Resources (Optional)

```bash
terraform destroy
```

---

## Security Considerations

The following security practices were considered while creating the infrastructure:

* AWS credentials were never hardcoded in Terraform files.
* Sensitive files such as Terraform state files were excluded from version control using `.gitignore`.
* CloudFront was used in front of S3 to improve performance and reduce direct access to the storage layer.
* Principle of least privilege was considered when configuring resource access.
* Resource configuration was managed through Terraform to ensure consistency and repeatability.
* Public access was enabled only for demonstration purposes to serve the static website.
* In a production environment, CloudFront Origin Access Control (OAC) should be used to keep the S3 bucket private and prevent direct public access.
* Infrastructure changes are version controlled through Git, allowing traceability and change tracking.

## Technologies Used

* Terraform
* AWS S3
* AWS CloudFront
* AWS CLI
* Git & GitHub

## Outputs
S3 Bucket Name
CloudFront Distribution URL

* S3 Bucket Name
* CloudFront Distribution URL
