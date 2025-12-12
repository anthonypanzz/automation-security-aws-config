# Automatically Blocking Port 22 From Public Exposure

This project implements a fully automated compliance workflow that enforces a **“No Public SSH”** policy by preventing Security Groups from exposing **port 22 (SSH)** to the internet.

Using **AWS Config**, the workflow continuously monitors for violations and automatically remediates them—no manual intervention required.

---

## 🔧 What I Built

- ✔️ Enabled **AWS Config** to continuously monitor EC2 Security Groups  
- ✔️ Applied the managed rule **`restricted-ssh`** to detect non-compliant configurations  
- ✔️ Created a **custom IAM remediation role** to allow automated enforcement  
- ✔️ Configured an **AWS-CloseSecurityGroup** remediation action  
- ✔️ Tested the workflow by creating a non-compliant Security Group and observed AWS Config automatically remediate it  

---

## ⭐ Why This Matters

This automation ensures that the **“No Public SSH”** security policy isn’t just written in documentation—it’s **actively enforced 24/7 across the environment**.

- No configuration drift  
- No exposed ports  
- No manual cleanup  

---

## Key Takeaway

Cloud security isn’t just about defining policies; it’s about **building mechanisms that guarantee those policies are followed**.  
**AWS Config + automated remediation** provides a powerful foundation for ensuring continuous compliance and eliminating risky exposure.

---
