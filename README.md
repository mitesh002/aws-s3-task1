# 🌩️ Cloud Computing Internship – Task 1: AWS S3 Cloud Storage Setup

## ✅ Task Objective
Create and configure cloud storage using **Amazon S3**.  
Deliverables include:
- A bucket with uploaded example files
- Configured access permissions

---

## 🪣 Bucket Details
- **Bucket Name**: `elitecloudtask1mitesh`
- **Region**: `ap-south-1` (Mumbai)
- **Bucket Access Settings**: "Block all public access" disabled
- **Bucket Policy**: Public read access enabled for all objects

---

## 📁 Files Uploaded
| File Name      | Description          | Access Level |
|----------------|----------------------|--------------|
| `natural.jpg`  | Sample image file    | Public       |
| `cloud_task.pdf`  | Sample pdf file     | Private      |

---

## 🌐 Public Access Demo
- **Public URL for `natural.jpg`**:  
  [https://elitecloudtask1mitesh.s3.ap-south-1.amazonaws.com/natural.jpg](https://elitecloudtask1mitesh.s3.ap-south-1.amazonaws.com/natural.jpg)

---

## 🔐 Access Control
- **Object Ownership**: Bucket Owner Enforced (ACLs ignored)
- **Public Access via**: S3 Bucket Policy
- **Private Objects**: Remain inaccessible without proper IAM or signed URLs

### Bucket Policy Used:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadForAllObjects",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::elitecloudtask1mitesh/*"
    }
  ]
}
