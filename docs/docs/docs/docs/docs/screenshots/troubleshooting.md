# troubleshooting.md

# Troubleshooting Guide

## Objective
Document common issues encountered during the IAM lab and how they were resolved.

---

## Issue 1: Redirect URI Mismatch

### Error
unauthorized_client

### Cause
Callback URL in request does not match Auth0 settings

### Fix
Ensure this matches exactly:
https://oidcdebugger.com/debug

---

## Issue 2: Invalid Grant

### Error
invalid_grant

### Cause
- Authorization code expired
- Code already used

### Fix
Restart login flow and use a fresh code

---

## Issue 3: Missing Scope

### Error
only access token was given which cannot be decoded in jwt cause its an encrypted token

### Cause
Scope not set properly

### Fix
Use:
openid profile email

---

##  Lesson Learned

Most IAM issues are caused by:
- Misconfiguration
- Mismatched URLs
- Expired tokens

Attention to detail is critical in identity systems.

---

##  Outcome

- Issues identified and resolved
- Stronger understanding of authentication flow
