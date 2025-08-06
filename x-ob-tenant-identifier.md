---
id: x-ob-tenant-identifier
title: Passing the X-OB-Tenant-Identifier HTTP Header
---
# Passing the X-OB-Tenant-Identifier HTTP Header

**Effective Date:** January 2025

Starting January 2025, all API requests must include the `X-OB-Tenant-Identifier` HTTP header. This ensures tenant-specific routing and processing.

---

### 📌 Header Requirement

| Header Name              | Required | Description                                 |
|--------------------------|----------|---------------------------------------------|
| `X-OB-Tenant-Identifier` | Yes      | Unique identifier for the requesting tenant. Example: `tenant12345` |

---

### 💻 Examples

#### Java (Apache HttpClient)
```java
request.addHeader("X-OB-Tenant-Identifier", "tenant12345");
```

#### Python (requests)
```python
headers = { "X-OB-Tenant-Identifier": "tenant12345" }
requests.get(url, headers=headers)
```

#### JavaScript (Axios)
```javascript
axios.get(url, {
  headers: {
    'X-OB-Tenant-Identifier': 'tenant12345'
  }
});
```

#### cURL
```bash
curl -X GET "https://api.yourservice.com/resource" \
  -H "X-OB-Tenant-Identifier: tenant12345"
```

#### Go (net/http)
```go
req.Header.Add("X-OB-Tenant-Identifier", "tenant12345")
```

---

### ❓FAQ

**Q: What happens if the header is missing?**  
A: The API will return a `400 Bad Request` with the message:
```json
{
  "error": "Missing required header: X-OB-Tenant-Identifier"
}
```

**Q: Where do I get the tenant identifier?**  
A: Log into OneBill → Config → Settings → Business Profile → Tenant ID.

**Q: Is it required for all endpoints?**  
A: Yes, this header is **mandatory** for all API endpoints.