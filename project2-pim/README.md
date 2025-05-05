# 🛡️ IAM Project #2: Microsoft Entra – Privileged Identity Management (PIM)

## 📘 Overview

This project demonstrates how to implement **Just-in-Time (JIT)** access to privileged roles using **Microsoft Entra Privileged Identity Management (PIM)**.  
The objective is to reduce standing admin rights, enable time-bound role elevation, and audit all privileged activity — key best practices in Identity and Access Management (IAM).

**Tenant Domain**: `markwhyce.onmicrosoft.com`  
**License Used**: Microsoft Entra ID P2 (Trial)

---

## 🎯 Objectives

- Enable Privileged Identity Management (PIM) in Microsoft Entra ID
- Assign privileged roles as **eligible** (not permanently active)
- Elevate roles temporarily using Just-in-Time access
- Audit role activations and privileged operations

---

## 🛠️ Tools Used

- Microsoft Entra Portal
- Microsoft Entra PIM (formerly Azure AD PIM)
- Audit Logs
- Just-in-Time Access Control

---

## 🪜 Steps Performed

---

### ✅ 1. Enabled PIM in the Tenant

- Navigated to **Microsoft Entra > Privileged Identity Management**
- Clicked **Consent** to activate role management via PIM

📸 `screenshots/pim-enable-consent.png`

---

### ✅ 2. Assigned an Eligible Role

- Assigned the **Security Administrator** role to myself as **Eligible**
- Role Assignment Type: `Eligible`  
- This ensures that elevation must be manually activated with approval and justification

📸 `screenshots/pim-eligible-role-assignment.png`

---

### ✅ 3. Activated the Role (Just-in-Time)

- Used **My roles** → Clicked **Activate**
- Provided justification: `Testing PIM for IAM project`
- Set a 1-hour access duration
- Role status changed from Eligible → Active

📸 `screenshots/pim-role-activation.png`

---

### ✅ 4. Reviewed Audit Logs

- Opened **PIM > Audit History**
- Verified role activation event was logged for my user
- Confirmed timestamp, role type, and justification were captured

📸 `screenshots/pim-audit-log.png`

---

## 📚 Lessons Learned

- Privileged Identity Management (PIM) reduces the attack surface by eliminating standing admin rights.
- Eligible roles with Just-in-Time activation provide tighter control over sensitive permissions.
- Audit trails in PIM allow full visibility into who elevated access, when, and why.
- Microsoft Entra ID P2 provides a robust solution for enforcing least privilege and zero trust principles in the cloud.

---

## 📁 Screenshots

| Filename                        | Description                              |
|----------------------------------|------------------------------------------|
| `pim-enable-consent.png`         | PIM consent and enablement screen         |
| `pim-eligible-role-assignment.png` | Eligible role assignment for Security Admin |
| `pim-role-activation.png`        | Just-in-Time role elevation screen        |
| `pim-audit-log.png`              | Audit trail showing role activation       |

---

## 👨‍💻 Author

**Michael Akintuyosi**  
Student | Computing and Security Technology  
Drexel University  
GitHub: [markwhyce-svg](https://github.com/markwhyce-svg)  
LinkedIn: [Michael Akintuyosi](https://www.linkedin.com/in/michael-akintuyosi-025317183/)

---

> Part of my hands-on IAM series exploring Microsoft Entra capabilities for secure identity lifecycle and access control.
