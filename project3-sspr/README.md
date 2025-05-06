# 🔐 IAM Project #3: Self-Service Password Reset (SSPR) & Lockout

## 📘 Overview

This project explores how to configure and test **Self-Service Password Reset (SSPR)** in Microsoft Entra ID. It includes enabling SSPR for users, setting up authentication methods, performing password reset simulations, and reviewing account lockout configurations to support account recovery and reduce help desk dependency.

---

## 🎯 Objectives

- Enable SSPR for users in Microsoft Entra ID
- Configure authentication methods (email, phone, security questions)
- Register recovery methods as a test user
- Simulate password reset using the SSPR portal
- Review and understand account lockout thresholds and settings

---

## 🪜 Steps Performed

---

### ✅ 1. Enabled SSPR in Entra ID

- Navigated to **Microsoft Entra ID → Protection → Password reset**
- Set **Self-service password reset** to:
  - ✅ Selected: **A group of users** (recommended) OR **All**
- Chose group from the tenant to enable SSPR

📸![Enable SSPR](screenshots/sspr-enable-settings.png)

---

### ✅ 2. Configured Authentication Methods

- Set users to register **at least one method** for SSPR
- Allowed methods:
  - ✅ Mobile phone
  - ✅ Email
  - ✅ Microsoft Authenticator app (if desired)
- Disabled security questions for better security (optional)

📸![Authentication Methods Config](screenshots/sspr-authentication-methods.png)

---

### ✅ 3. Registered Recovery Info as Test User

- Logged in as a test user (e.g., `tjones@markwhyce.onmicrosoft.com`)
- Went to [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup)
- Registered phone number and/or email for password recovery

📸![User Registration](screenshots/sspr-user-registration.png)

---

### ✅ 4. Simulated a Password Reset

- Opened a private browser session
- Visited: [https://aka.ms/sspr](https://aka.ms/sspr)
- Entered user email
- Received verification via registered method
- Reset the password successfully

📸![SSPR Reset Flow](screenshots/sspr-password-reset-flow.png)

---

### ✅ 5. Reviewed Lockout Settings

- Navigated to **Microsoft Entra → Protection → Authentication methods**
- Explored **Account lockout settings**
  - Threshold: 10 failed attempts
  - Duration: 60 seconds (example)
- Verified protections against brute-force attacks

📸![Lockout Settings](screenshots/sspr-lockout-settings.png)

---

## 📚 Lessons Learned

- SSPR empowers users to reset passwords without IT support, reducing helpdesk tickets.
- Recovery method registration is critical and should be enforced at first login.
- Properly configuring lockout settings protects accounts from password spray and brute force.

---
