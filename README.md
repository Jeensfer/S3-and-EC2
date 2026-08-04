# Experiment No. 2 — Cloud Storage Creation (S3) and Launching an EC2 Instance in AWS

## Aim
To create an Amazon S3 bucket for cloud storage and launch a virtual machine using Amazon EC2 in the AWS Management Console.

## Objectives
After completing this experiment, students will be able to:
- Understand AWS Cloud Storage (Amazon S3)
- Create and manage S3 buckets
- Upload and organize files in cloud storage
- Launch an EC2 virtual server
- Connect to an EC2 instance
- Understand cloud computing infrastructure services

## Software Requirements
- Laptop/Desktop
- Internet connection
- AWS Academy Learner Account / AWS Free Tier Account
- Modern web browser (Chrome/Edge)

## Theory

### Amazon S3 (Simple Storage Service)
Amazon S3 is an object storage service provided by AWS that stores unlimited amounts of data with high durability and availability.

**Features:**
- Unlimited storage
- 99.999999999% (11 nines) durability
- High availability
- Secure storage
- Versioning
- Lifecycle management
- Encryption

---

## Part A — Creating an Amazon S3 Bucket

1. Open the AWS console: [https://aws.amazon.com/console/](https://aws.amazon.com/console/)
2. Log in:
   - Click **Sign in using root user email**
   - Enter the registered email address
   - Enter the AWS password
   - Complete the verification process
3. Type **S3** in the search box.
4. Click **Amazon S3**.
5. Click **Create bucket**.
6. Enter the following details:

   | Parameter    | Value                      |
   |--------------|-----------------------------|
   | Bucket type  | General purpose            |
   | Bucket name  | `student-cloud-storage-001` |
   | AWS Region   | Asia Pacific (Mumbai)      |

7. Leave the remaining settings unchanged.
8. Click **Create bucket**.
9. Click **Upload**.
10. Upload the following files:
    - PDF file
    - Word document
    - Image file

**Example bucket structure:**
```
student-cloud-storage-001
│
├── Cloud.pdf
├── Assignment.docx
├── Image.jpg
└── Notes.pdf
```

---

## Part B — Launching an Amazon EC2 Instance

1. Type **EC2** in the AWS search bar.
2. Open the **EC2 Dashboard**.
3. Click **Launch instance**.
4. Enter the instance name: `CloudLabVM`
5. Select the operating system:
   - Amazon Linux 2023
   - Ubuntu Server
6. Select the instance type: `t3.micro`
7. Create a key pair:

   | Parameter      | Value        |
   |----------------|--------------|
   | Key pair name  | `CloudLabKey`|
   | Key pair type  | RSA          |
   | File format    | `.pem`       |

8. Download the `CloudLabKey.pem` file.
9. Configure network settings:
   - ✅ Allow SSH traffic (Port 22)
   - ✅ Allow HTTP traffic (Port 80)
   - ✅ Allow HTTPS traffic (Port 443)
10. Set the storage size: `8 GiB`
11. Click **Launch instance**.
12. Wait until the status changes:

    ```
    Pending → Running
    ```

### Connecting to the EC2 Instance
1. Open **EC2**.
2. Select the instance.
3. Click **Connect**.
4. Select **EC2 Instance Connect**.
5. Click **Connect**.
6. Execute the following command:

   ```bash
   echo "Hello AWS"
   ```

   **Output:**
   ```
   Hello AWS
   ```

### Stopping the EC2 Instance
1. Open **EC2**.
2. Select **Instances**.
3. Select the running instance.
4. Click **Instance state**.
5. Click **Stop instance**.

   **Status flow:**
   ```
   Running → Stopping → Stopped
   ```

### Logging Out of AWS
1. Click the profile icon in the upper-right corner.
2. Select **Sign out**.

---

## Result
The Amazon S3 bucket was created successfully, files were uploaded, an EC2 instance was launched, and the virtual machine was connected successfully.
