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

<img width="1919" height="945" alt="Screenshot 2026-08-04 084721" src="https://github.com/user-attachments/assets/d6b4b74a-fe47-4c52-bff3-2b3b51172e84" />

2. Log in:
   - Click **Sign in using root user email**
   - Enter the registered email address
   - Enter the AWS password
   - Complete the verification process

<img width="1919" height="941" alt="Screenshot 2026-08-04 084748" src="https://github.com/user-attachments/assets/03ca12e7-4c47-45eb-86a8-e535d67cb8df" />

3. Type **S3** in the search box.

<img width="1919" height="938" alt="Screenshot 2026-08-04 084803" src="https://github.com/user-attachments/assets/4f933454-1f79-430b-a5ba-8bbd984e5917" />

5. Click **Amazon S3**.
6. Click **Create bucket**.

<img width="1919" height="944" alt="Screenshot 2026-08-04 084844" src="https://github.com/user-attachments/assets/4ea1edd8-df60-4a28-af68-10b2a3df2247" />

7. Enter the following details:

   | Parameter    | Value                      |
   |--------------|-----------------------------|
   | Bucket type  | General purpose            |
   | Bucket name  | `student-cloud-storage-001` |
   | AWS Region   | Asia Pacific (Mumbai)      |

<img width="1919" height="943" alt="Screenshot 2026-08-04 085039" src="https://github.com/user-attachments/assets/77258614-fcdb-404e-a907-e71166572af1" />

9. Leave the remaining settings unchanged.
11. Click **Create bucket**.

<img width="1918" height="943" alt="Screenshot 2026-08-04 085054" src="https://github.com/user-attachments/assets/2acbf073-822b-426c-acda-7bf65d5a09e6" />

12. Click **Upload**.
13. Upload the following files:
    - PDF file
    - Word document
    - Image file

<img width="1919" height="948" alt="Screenshot 2026-08-04 085217" src="https://github.com/user-attachments/assets/aef13495-58dc-47df-8252-89845d1f9d41" />
    
**Example bucket structure:**
```
student-cloud-storage-001
│
├── Cloud.pdf
├── Assignment.docx
├── Image.jpg
└── Notes.pdf
```
<img width="1917" height="949" alt="Screenshot 2026-08-04 085230" src="https://github.com/user-attachments/assets/fa3422e1-2aca-4da6-9fb1-b770e8b76999" />

---

## Part B — Launching an Amazon EC2 Instance

1. Type **EC2** in the AWS search bar.

<img width="1919" height="942" alt="Screenshot 2026-08-04 085303" src="https://github.com/user-attachments/assets/83a8a44a-07a0-4f20-82e4-0e9906be5289" />

2. Open the **EC2 Dashboard**.

<img width="1918" height="937" alt="Screenshot 2026-08-04 085320" src="https://github.com/user-attachments/assets/3eaed767-2520-4860-8768-bf5f59c45a83" />

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

<img width="1918" height="959" alt="Screenshot 2026-08-04 085617" src="https://github.com/user-attachments/assets/787fde8e-a597-46a7-ae53-02fc2d414ef3" />

12. Wait until the status changes:

<img width="1919" height="390" alt="Screenshot 2026-08-04 085716" src="https://github.com/user-attachments/assets/de219366-bcca-47d8-8bfc-d707480500f1" />


    ```
    Pending → Running
    ```

### Connecting to the EC2 Instance
1. Open **EC2**.
2. Select the instance.

<img width="1918" height="943" alt="Screenshot 2026-08-04 085852" src="https://github.com/user-attachments/assets/071680fe-763a-47d3-8ab4-8a3aa91f0258" />

3. Click **Connect**.

<img width="1919" height="936" alt="Screenshot 2026-08-04 085907" src="https://github.com/user-attachments/assets/c9718a5c-47b6-4aad-b4ea-9b204d3b30ef" />

4. Select **EC2 Instance Connect**.
5. Click **Connect**.

<img width="1919" height="936" alt="Screenshot 2026-08-04 085907" src="https://github.com/user-attachments/assets/dc72dc6a-b553-4b9d-afd8-b3d181928b45" />

6. Execute the following command:

   ```bash
   echo "Hello AWS"
   ```

   **Output:**
   ```
   Hello AWS
   ```

<img width="1919" height="424" alt="Screenshot 2026-08-04 085956" src="https://github.com/user-attachments/assets/89ec4ccd-469d-494b-a1ac-46d443fffb72" />


### Stopping the EC2 Instance
1. Open **EC2**.
2. Select **Instances**.
3. Select the running instance.
4. Click **Instance state**.

<img width="1919" height="941" alt="Screenshot 2026-08-04 090038" src="https://github.com/user-attachments/assets/073c5fb4-e689-42e6-b853-3d3bcb6671ab" />

5. Click **Stop instance**.

   **Status flow:**
   ```
   Running → Stopping → Stopped
   ```
<img width="1904" height="903" alt="Screenshot 2026-08-04 090059" src="https://github.com/user-attachments/assets/8096aac6-fb26-4f36-bda2-3f18761618a0" />


### Logging Out of AWS
1. Click the profile icon in the upper-right corner.
2. Select **Sign out**.

---

## Result
The Amazon S3 bucket was created successfully, files were uploaded, an EC2 instance was launched, and the virtual machine was connected successfully.
