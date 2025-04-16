# 📜 Custom IAM Policy: Full Access to Specific S3 Bucket

This custom IAM policy grants **full access** (`s3:*`) to a **specific S3 bucket** and all its objects.  
It is useful when you want a user or group to access only one bucket and nothing else.

---

## ✅ Use Case

> Give full access to the S3 bucket `my-bucket-name`, without giving access to any other AWS resources.

---

## 🧾 JSON Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:*",
      "Resource": "arn:aws:s3:::my-bucket-name/*"
    }
  ]
}
