# Token Analysis (JWT Breakdown)

## Objective
Decode and analyse the ID Token returned from Auth0.

---

## Step 1: Copy the Token

After token exchange, copy the ID Token (JWT).

---

## Step 2: Decode Token

Go to:
https://jwt.io

Paste the token into the decoder.

---

<img width="1657" height="902" alt="jwt io copy" src="https://github.com/user-attachments/assets/fddc8b11-d67e-406d-8096-ae126ba875a0" />


## Sample Payload
  "nickname": "",
  
  "name": "@gmail.com",
  
  "picture": "https://s.gravatar.com/avatar/b11301036dcd73d64772d2b856fc02bc?s=480&r=pg&d=https%3A%2F%2Fcdn.auth0.com%2Favatars%2Fss.png",
  
  "updated_at": "2026-04-22T10:56:25.565Z",
  
  "email": "@gmail.com",
  
  "email_verified": 
  
  "iss": "https://dev-kjq1iuqp5sh8qgl3.us.auth0.com/",
  
  "aud": "bQCrRSYzoo3YF4mdfY2",
  
  "sub": "auth0|69e771c8c61be620e134da5f",
  
  "iat": 1776856311,
  
  "exp": 1776892311,
  
  "sid": "OYngEodMKzLiDPeUc",
  
  "nonce": "51vs4aufkdi"


## Understanding Key Claims
sub (Subject):

Unique user ID

Never changes even if email changes

iss (Issuer):

Identity Provider URL

Confirms token origin

iat (Issued At):

Time token was created

exp (Expiration):

Token expiry time

Critical for security


## Why Tokens Expire

Short-lived tokens:

Reduce risk if stolen

Enforce re-authentication

Improve overall security posture

## Outcome
Token successfully decoded

Identity data validated

Understanding of authentication payload achieved
