# OIDC Authorization Code Flow

##  Objective
Simulate a real authentication flow and retrieve an authorization code.

---

## Step 1: Open OIDC Debugger

Go to:
https://oidcdebugger.com

---

## Step 2: Configure Request

Fill in the following:

- Authorize URI:
  https://YOUR_DOMAIN.auth0.com/authorize

- Client ID:
  (from Auth0)

- Redirect URI:
  https://oidcdebugger.com/debug

- Scope:
  openid profile email

- Response Type:
  code

---

<img width="1591" height="912" alt="openid" src="https://github.com/user-attachments/assets/5efe495f-0d38-448b-9b09-eba947bdc6c5" />


---

## Step 3: Authenticate User

- Click **Send Request**
- Log in using your test user
- After login, you will be redirected back

<img width="1343" height="915" alt="open id pro" src="https://github.com/user-attachments/assets/d344481f-7df3-41a4-8d8c-455a7cae0d7c" />

---

## Step 4: Capture Authorization Code

You will see a temporary code like:

<img width="1541" height="915" alt="openid connect success" src="https://github.com/user-attachments/assets/0a3f1810-b049-4704-9d0a-3f2cd959b83b" />


This code is:
- Short-lived
- Single-use
- Required for token exchange

---

## Step 5: Exchange Code for Token

## Use Postman (easiest) for exchange code for token
Open Postman
Set method to POST
URL:https://YOUR_DOMAIN.auth0.com/oauth/token
Go to Body → x-www-form-urlencoded and add:
KEY	VALUE:
- grant_type = authorization_code
- code = (your code)
- client_id
- client_secret
- redirect_uri

Hit Send

---

<img width="1571" height="907" alt="exchange token" src="https://github.com/user-attachments/assets/531da2ea-d18d-479a-ada8-dd4383a64b3b" />

---

## Outcome

- Successfully completed authentication flow
- Retrieved access token and ID token (JWT)

---

## Key Insight

This flow ensures:
- Secure authentication
- No credentials exposed to the application
- Tokens are issued only after verification
  
