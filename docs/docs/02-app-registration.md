## Application Registration (OIDC Client Setup)

##  Objective
Register a web application in Auth0 to enable authentication using OpenID Connect.

---

## Step 1: Create Application

Navigate to:

Applications → Applications → Create Application

Fill in:
- Name: IAM-Test-App
- Type: Regular Web Application

Click Create.

---

## Step 2: Configure Application Settings

Locate the following:

### Allowed Callback URLs

<img width="1088" height="625" alt="CALLBACK" src="https://github.com/user-attachments/assets/6025a527-a950-40c8-b280-60ca1b8ef8d9" />

This is where Auth0 redirects users after login.

---

##  Step 3: Capture Credentials

From the Settings tab, copy:

- Client ID
- Client Secret

⚠️ Important:
- Treat Client Secret like a password
- Never expose it in frontend code

---
<img width="1873" height="902" alt="TEST APP copy" src="https://github.com/user-attachments/assets/a159e451-8889-4b38-acde-d904489a5329" />



---

## Why This Matters

Applications must be registered so the Identity Provider can:
- Identify the application
- Control access
- Enforce security policies

---

## Outcome

- Application successfully registered
- Redirect URI configured
- Credentials generated for authentication flow
