---
id: proxy-information
title: Proxy Information
---
# Proxy Information

OneBill supports a Channel Management module to let a business expand through channel partners. When a user wants to manage data under a partner, the proxy information is passed as part of the header.

This enables users to perform operations **as a channel partner**, using a single login created at the **provider level**. This avoids the need for different logins per partner.

---

### 📌 Required Header

| Header                | Required | Description                           |
|------------------------|----------|---------------------------------------|
| `proxy_accountNumber` | Yes      | Partner's account number to act on behalf of. |