# 🔐 IAM Project #1: Azure AD Conditional Access

## 📘 Overview

This project demonstrates how to configure Identity and Access Management (IAM) in **Microsoft Azure Active Directory** using **Conditional Access Policies**. The goal was to simulate real-world identity controls such as Multi-Factor Authentication (MFA) and access restrictions based on group membership and device compliance.

---

## 🎯 Objectives

- Set up Azure Active Directory and create test users
- Enforce Multi-Factor Authentication (MFA) for all users
- Create a Security Group and assign users
- Configure Conditional Access Policies to:
  - Require MFA
  - Block access from unmanaged devices

---

## 🛠️ Tools Used

- **Microsoft Azure Portal**
- **Azure Active Directory**
- **Conditional Access**
- **Microsoft Authenticator App**
- **Private/Incognito Browsers for Testing**

---

## 🪜 Steps Performed

### ✅ 1. Azure Account Creation
- Signed up for a free Azure account at [azure.microsoft.com/free](https://azure.microsoft.com/free)
- Accessed the portal at [portal.azure.com](https://portal.azure.com)

### ✅ 2. User & Group Creation
- Created three test users:
  - `admin.user@tenant.onmicrosoft.com`
  - `sales.user@tenant.onmicrosoft.com`
  - `guest.user@tenant.onmicrosoft.com`
- Created a **Security Group** named `SalesDept`
- Added `sales.user` to the group

### ✅ 3. Conditional Access Policies

#### 🔒 Require MFA for All Users
- Assigned to **All Users**
- Applied to **All Cloud Apps**
- Grant control: **Require MFA**

#### 🚫 Block Unmanaged Devices for SalesDept
- Assigned to `SalesDept` group
- Condition: All platforms
- Grant control: **Block Access**
- Applied to selected apps like **Microsoft 365**

---

## 🧪 Testing

### 👤 `guest.user` Login Test
- Signed in via [portal.office.com](https://portal.office.com)
- Prompted for MFA and successfully authenticated via **Microsoft Authenticator**

📸 _[MFA prompt]_

---

### 👤 `sales.user` Login Test
- Signed in from an **unmanaged device** (Incognito browser)
- Triggered Conditional Access Policy

📸 _[screenshot of access blocked message]_

---

## 📚 Lessons Learned

- Conditional Access is a powerful tool to enforce granular IAM controls
- Azure AD security can be easily tested using private browsing and test users
- Microsoft Authenticator setup is smooth and highly secure for MFA
- Policies should be clearly documented to avoid locking out admins

---

## 📁 Screenshots

> 📷 Place images in a `/screenshots` folder inside this project  
markdown
![MFA Prompt](https://raw.githubusercontent.com/markwhyce-svg/iam-project-series/main/project1-conditional-access/screenshots/mfa-prompt.jpg)
![Access Blocked](screenshots/access-blocked.png)  
![Policy Settings](screenshots/conditional-policy.png)
