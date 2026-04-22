# Environment Setup (Auth0 IAM Lab)

Objective
Set up an Identity Provider (IdP) using Auth0 and create a test user for authentication.

---

Step 1: Create an Auth0 Account

Go to:
https://auth0.com

- Sign up for a free account
- Choose a tenant name (this becomes your domain)
- Select your region

---

Step 2: Create a Test User

Navigate to:

User Management → Users → Create User

Fill in:
- Email: iam-test@example.com
- Password: (choose a secure password)
- Connection: Username-Password-Authentication

---

<img width="1447" height="751" alt="create user" src="https://github.com/user-attachments/assets/c073c9f7-616e-4cef-ac5e-0edcc278f7be" />


---
 Step 3: Add User Attributes

You can enrich identity data by adding metadata.

Example:
- Department: Engineering

This is useful for:
- Role-based access control (RBAC)
- Conditional access policies

<img width="1065" height="835" alt="user metadata" src="https://github.com/user-attachments/assets/03396ba9-79e6-412e-9dcf-d75f00f17826" />

---

At this stage:
- Auth0 tenant is configured
- A test identity exists
- Ready to integrate with an application

---

## 💡 Key Insight

Identity Providers like Auth0 act as a central authentication authority, removing the need to store passwords inside applications.

