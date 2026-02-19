**How to Use the Authentication Skill**

Use this guide to get the **best results** from the Authentication Skill and avoid insecure or incomplete setups.

---

## What This Skill Is For

Use this skill to design:

* User registration & login
* Token-based authentication
* Session management
* Logout & token invalidation
* User identity & profile handling

This skill is **security-first** and intended for **production systems**.

---

## ⚠️ IMPORTANT: Reference the Skill File

**You MUST reference `authentication/SKILL.md` when implementing authentication features.**

When prompting an AI assistant or planning your implementation:

```
Use @authentication/SKILL.md to implement authentication for my application.
```

The SKILL.md file contains:
* Complete security guidelines and best practices
* Detailed implementation requirements for all auth components
* Token management and session handling specifications
* Security requirements and attack prevention measures
* Compliance and testing requirements

**Do not implement authentication without consulting SKILL.md** - it ensures you follow production-grade security standards.

---

## Step 1: Describe Your App (Required)

Always start with this:

```
Application type: (Web / Mobile / API)
Frontend:
Backend:
Database:
Security level: (Basic / Production / High)
```

Example:

```
Application type: Web (SPA)
Frontend: Next.js
Backend: Node.js
Database: PostgreSQL
Security level: Production
```

---

## Step 2: List What You Need

```
Required:
- Registration
- Login
- Access & refresh tokens
- Logout

Optional:
- Email verification
- Password reset
- 2FA
```

If unsure, say:

```
Use secure defaults
```

---

## Step 3: Use This Prompt Template

```
Use the Authentication Skill.

Design a secure authentication system for my app.

[App details]
[Required / Optional features]

Explain the auth flow, token handling, session management, and logout.
Do not include code.
```

---

## Safe Defaults (If You Don’t Know)

* Access token: **15 minutes**
* Refresh token: **14 days**
* Token storage (web): **httpOnly cookies**
* Password hashing: **bcrypt / argon2**
* Login limit: **5 attempts / 15 minutes**

---

## Simple Auth Flow

```
Login → Issue tokens → Access API
Refresh → New access token
Logout → Invalidate tokens
```

---

## What Not to Do

* Don’t store passwords or tokens in plain text
* Don’t expose detailed login errors
* Don’t skip logout or token invalidation

---
