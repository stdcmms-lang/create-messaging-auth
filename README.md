# Messaging Auth — Implementation Test

Implement the **auth and current-user HTTP API** described in [`auth-interface.md`](auth-interface.md). This is a timed exercise: use AI to help you finish the implementation in the time window. Any tech stack is fine.

## What to build

Your server should expose the endpoints, request/response shapes, error codes, and behaviors defined in `auth-interface.md` (registration, login, refresh, logout, password reset, email verification, MFA, profile updates, devices/sessions, and blocked users).

## Quick check

With your server running (`http://127.0.0.1:3000`), run the preliminary functional suite:

```bash
node auth-functional-test.mjs
```

These tests cover core flows; passing them does not guarantee a complete solution. Read the spec for edge cases and concurrency rules.

## How you will be evaluated

| Dimension | What we look for |
|-----------|------------------|
| **Functional correctness** | Behavior matches `auth-interface.md` (status codes, response shapes, flows, idempotency, token rotation, anti-enumeration, etc.). Your implementation should cover **edge cases** and resist **race conditions** |
| **Scalability** | Sensible data model and API design for low latency and high throughput. |
| **Security** | Safe auth practices (token handling, replay protection, input validation, redirect allow-list rules, no leakage of secrets in responses). |
