---
navigation:
  order: 30
---

# 4.3 Errors

| Status | Meaning | What the device does |
|---|---|---|
| 400 | Malformed request | Stop sending, and log it |
| 401 | Invalid token | Re-authenticate |
| 409 | Version mismatch (conflict) | Replace with the response's `body`, and show a conflict |
| 413 | Body over 1 MB | Tell the user, and do not send |
| 429 | Too many requests | Wait the seconds named in `Retry-After`, then resend |
| 5xx | Server failure | Resend with exponential backoff (up to 5 times) |
