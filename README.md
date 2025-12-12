# Automatically Blocking Port 22 From Public Exposure

This project implements a fully automated compliance workflow that enforces a **“No Public SSH”** policy by preventing Security Groups from exposing **port 22 (SSH)** to the internet.

Using **AWS Config**, the workflow continuously monitors for violations and automatically remediates them—no manual intervention required.

---

## 🔧 What I Built

- ✔️ Enabled **AWS Config** to continuously monitor EC2 Security Groups  


- ✔️ Applied the managed rule **`restricted-ssh`** to detect non-compliant configurations  
<img width="1878" height="613" alt="Screenshot 2025-12-10 222653" src="https://github.com/user-attachments/assets/df4156d6-353e-43f1-abee-229ee37bca99" />

---

- ✔️ Created a **custom IAM remediation role** to allow automated enforcement

<img width="1916" height="877" alt="Screenshot 2025-12-11 060212" src="https://github.com/user-attachments/assets/894b0812-e14b-42b5-a320-d68c9f89b9de" />
<img width="1906" height="887" alt="Screenshot 2025-12-10 221940" src="https://github.com/user-attachments/assets/4a543bef-ae1c-4e0f-a1c6-2d026608ec33" />

   --- 

- ✔️ Configured an **AWS-CloseSecurityGroup** remediation action  
<img width="1908" height="864" alt="Screenshot 2025-12-10 223104" src="https://github.com/user-attachments/assets/996c6bfa-d5f6-4503-9a9e-07e27980f985" />
<img width="1894" height="686" alt="Screenshot 2025-12-10 223048" src="https://github.com/user-attachments/assets/d2bdd14d-b25d-4837-9b52-33e33aa137bf" />


---

- ✔️ Tested the workflow by creating a non-compliant Security Group and observed AWS Config automatically remediate it  

<img width="1601" height="246" alt="Screenshot 2025-12-11 053455" src="https://github.com/user-attachments/assets/509080fa-296d-4a97-b240-1717c38d6f66" />
<img width="1484" height="350" alt="Screenshot 2025-12-11 055637" src="https://github.com/user-attachments/assets/b2778df4-9592-414b-9611-4b560f24affb" />
<img width="1609" height="270" alt="Screenshot 2025-12-11 055705" src="https://github.com/user-attachments/assets/8ae6ffc9-1b7b-4a7b-94b1-2b4cd2d17650" />


---

## ⭐ Why This Matters

This automation ensures that the **“No Public SSH”** security policy isn’t just written in documentation, it’s **actively enforced 24/7 across the environment**.

- No configuration drift  
- No exposed ports  
- No manual cleanup  

---

## Key Takeaway

Cloud security isn’t just about defining policies; it’s about **building mechanisms that guarantee those policies are followed**.  
**AWS Config + automated remediation** provides a powerful foundation for ensuring continuous compliance and eliminating risky exposure.

---
