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

<img width="1591" height="912" alt="openid copy" src="https://github.com/user-attachments/assets/07dfe211-4539-462b-ac2e-4ca9c0eaa914" />



---

## Step 3: Authenticate User

- Click **Send Request**
- Log in using your test user
- After login, you will be redirected back

<img width="1343" height="915" alt="open id pro copy" src="https://github.com/user-attachments/assets/864c5b11-0cae-404f-9e53-2da8b91c94ce" />


---

## Step 4: Capture Authorization Code

You will see a temporary code like:

<img width="1105" height="371" alt="authorization copy" src="https://github.com/user-attachments/assets/807cc0b2-e564-4d8b-b128-3cd92e96fd57" />

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

<img width="1571" height="907" alt="exchange token copy" src="https://github.com/user-attachments/assets/1722bb91-3419-4e40-9460-fe16a27a9316" />


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
  

