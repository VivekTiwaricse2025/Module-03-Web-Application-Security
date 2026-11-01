# Day 12 — OWASP Top 10:2025

OWASP means Open Worldwide Application Security Project. The Top 10 is an awareness document describing important web application security risk categories.

| Rank | Category | Meaning | Prevention |
|---|---|---|---|
| A01 | Broken Access Control | Users access data/actions beyond their permission. | Server-side authorization; deny by default; object-level checks. |
| A02 | Security Misconfiguration | Unsafe defaults, exposed services, verbose errors or weak settings. | Harden configurations; remove defaults; review headers/services. |
| A03 | Software Supply Chain Failures | Risks in dependencies, build systems and updates. | Inventory, scan and update dependencies; protect build pipelines. |
| A04 | Cryptographic Failures | Sensitive information is inadequately protected. | Modern cryptography, TLS and appropriate password hashing. |
| A05 | Injection | Untrusted input is interpreted as a command/query. | Parameterized queries, safe APIs and output encoding. |
| A06 | Insecure Design | Security requirements/threat scenarios missing from design. | Threat modeling, abuse cases and secure design requirements. |
| A07 | Authentication Failures | Weak login, recovery or session controls. | MFA, rate limits, secure recovery and sessions. |
| A08 | Software or Data Integrity Failures | Software/data trusted without integrity verification. | Verify artifacts/updates; protect pipelines and data. |
| A09 | Security Logging and Alerting Failures | Events are not logged, monitored or acted on. | Protected security logs, monitoring and alerting. |
| A10 | Mishandling of Exceptional Conditions | Unexpected states/errors handled unsafely. | Fail safely and handle errors consistently. |

## Important concepts
**Injection:** Untrusted input becomes part of a query or command. Use parameterized queries and least-privilege database accounts.

**XSS:** Untrusted content executes as script in another user's browser. Use context-aware output encoding, safe DOM APIs, suitable sanitization when rich HTML is required, and CSP as an additional layer.

**Broken access control:** A user accesses another user's data or restricted functions. Enforce authorization server-side for every request and object.

**Authentication failures:** Weak login, recovery or session controls. Use strong password hashing, MFA where appropriate, rate limiting and secure session management.

**Security misconfiguration:** Default credentials, debug mode, unnecessary services or verbose errors. Use secure defaults and hardening.

Review: explain each category, give an example, describe impact and list prevention.
