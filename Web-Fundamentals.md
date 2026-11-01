# Day 11 — Web Application Fundamentals

## Web application architecture
A browser (client) sends a request to a web server. The server routes it to application code, may access a database, and returns a response for the browser to display.

**Flow:** User action → HTTP request → server/application → database or service → HTTP response → browser.

## HTTP and HTTPS
HTTP transfers web resources. HTTPS is HTTP protected by TLS, providing encryption in transit, integrity and server authentication when certificates are validated. HTTPS does not itself fix insecure application logic.

## HTTP request
A request includes a method, path, headers and sometimes a body.

```http
GET /products HTTP/1.1
Host: example.test
Accept: text/html
```

Common methods: GET (retrieve), POST (submit/create or trigger an operation), PUT (replace), PATCH (partially update), DELETE (request deletion).

## HTTP response
A response contains a status code, headers and optional body.

| Code | Meaning |
|---|---|
| 200 | OK |
| 201 | Created |
| 301/302 | Redirect |
| 400 | Bad Request |
| 401 | Authentication required/failed |
| 403 | Forbidden |
| 404 | Not Found |
| 429 | Too Many Requests |
| 500 | Internal Server Error |

## Cookies and sessions
Cookies are small data items stored by the browser and sent with matching requests. Session cookies often contain an opaque session identifier. Use Secure, HttpOnly and appropriate SameSite attributes. Do not store plaintext passwords in cookies.

A session associates multiple requests with a user or client state. Use unpredictable identifiers, rotate after login/privilege changes, expire inactive sessions and invalidate on logout.

## Authentication vs authorization
- Authentication: verifies identity — who are you?
- Authorization: checks permissions — what may you do?

Authorization must be enforced server-side for every protected action and object. Hiding a button in the browser is not access control.

## Practical: browser Network panel
1. Open Chrome and press F12.
2. Select Network.
3. Visit a site you own or are permitted to inspect.
4. Select a request and review method, status, headers and response.
5. Record observations.
6. Redact cookies, tokens, authorization headers and personal data from screenshots.

**Evidence:** network overview, redacted request headers and response details.
