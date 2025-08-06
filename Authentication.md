---
id: authentication
title: Authentication
---

# Authentication

OneBill uses **OAuth** for authenticating a user to access the API. An access token must be generated in order to utilize the OneBill REST web services.

---

### 🔐 Original Request URL (POST)

```bash
https://www....com/oauth/token?grant_type=password&client_id=<TenantID>&client_secret=<client_secret>&username=<username>&password=<hashed_password>&scope=trust
```

---

### 📌 Request Parameter Descriptions

| Parameter        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `client_id`      | Check your welcome pack email notification for the Tenant ID or contact your OneBill onboarding executive. |
| `client_secret`  | Available in Business Profile section of the application.                  |
| `username`       | Username for a particular tenant.                                           |
| `hashed_password`| Password encoded using `ShaPasswordEncoder256`.                             |
