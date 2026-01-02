# Starlight API Utilities

**Developer:** Dominex

**Description:**
Starlight API utilities provide HTTP methods like GET, POST, PUT, PATCH, DELETE, HEAD, and OPTIONS for the Starlight Programming Language. Supports headers, auth, JSON body, query parameters, and timeouts.

**Installation:**
`npm install starlight-api`

**Usage:**

## Basic GET Request
`
import api from "starlight-api";

const response = await api.get("https://example.com/data");
console.log(response.data);
`

## POST Request with JSON
`
const payload = { name: "Starlight", version: "1.0.0" };

const response = await api.post("https://example.com/api", payload, {
    headers: { "Custom-Header": "Value" }
});
console.log(response.data);
`

## Custom Headers and Auth
`
const response = await api.get("https://example.com/secure", {
    headers: { "X-Token": "abc123" },
    auth: { username: "user", password: "pass" }
});
`

**Options:**

- `method` - HTTP method (GET, POST, etc.)
- `url` - Request URL
- `headers` - Custom HTTP headers
- `body` - Request body (object or string)
- `auth` - Basic auth: { username, password }
- `params` - Query parameters object
- `timeout` - Request timeout in ms (default 15000)


## All Methods:

- `api.request(options)`
- `api.get(url, options)`
- `api.post(url, body, options)`
- `api.put(url, body, options)`
- `api.patch(url, body, options)`
- `api.delete(url, options)`
- `api.head(url, options)`
- `api.options(url, options)`


**Notes:**
- JSON responses are automatically parsed.
- Timeout defaults to 15 seconds.
- Handles both HTTP and HTTPS protocols.
- Returns object: { ok, status, statusText, headers, data, raw }.

https://starlight-learn-lang.pages.dev/
