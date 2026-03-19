---
icon: circle-info
---

# CDN API

## CDN Cache Clearing API

#### Authentication

To authenticate your API requests, include your token in the `Authorization` header using the **Bearer** scheme:

```
Authorization: Bearer YOUR_API_TOKEN
```

> ⚠️ **Important:** Keep your token secure and **never share it publicly**. You can regenerate your token at any time from the dashboard.

***

#### Endpoint

#### `POST /api/v1/cdn/clear-cache`

Clears the cache for a specified CDN domain.

**Request Body**

```json
{
  "domain": "example.1of1cdn.com"
}
```

* **domain** (string, required): The CDN domain for which the cache should be cleared.

**Response**

* **Success (200 OK)**

```
"Cache cleared"
```

***

#### Usage Examples

#### cURL

```bash
curl -X POST https://shield.1of1servers.com/api/v1/cdn/clear-cache \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "domain": "example.1of1cdn.com"
  }'
```

***

#### JavaScript (Fetch)

```js
const response = await fetch('https://shield.1of1servers.com/api/v1/cdn/clear-cache', {
  method: 'POST',
  headers: {
    'Authorization': 'Bearer YOUR_API_TOKEN',
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    domain: 'example.1of1cdn.com'
  })
});

const result = await response.text();
console.log(result);
```

***

#### JavaScript (Axios)

```js
import axios from 'axios';

const response = await axios.post(
  'https://shield.1of1servers.com/api/v1/cdn/clear-cache',
  {
    domain: 'example.1of1cdn.com'
  },
  {
    headers: {
      'Authorization': 'Bearer YOUR_API_TOKEN',
      'Content-Type': 'application/json'
    }
  }
);

const result = response.data;
console.log(result);
```
