## Vulnerability VI - Mass Assignment

### Notes
- Bob is not doing any filtering on the server side. Since he is using the mass assignment feature, he is also inserting credit values into the database, which malicious actors can update.
- Before using any framework, one must study how backend insertions and updates are carried out. In the Laravel framework, fillable and guarded arrays mitigate the above-mentioned scenarios.
- Avoid using functions that automatically bind client input to code variables.
- Allowlist only those properties that need to be updated from the client side.

### Questions
- It is not good practice to blindly insert/update user-provided data into the database.
- Completed step 2 as instructed.
- The returned credit value is `50`.

---

## Vulnerability VII - Security Misconfiguration

### Notes
- Arises from improper or incomplete default configuration, publicly accessible cloud storage, misconfigured Cross-Origin Resource Sharing (CORS), and error messages that expose sensitive data.
- Limit access to administrative interfaces to authorized users and disable them for all others.
- Disable default usernames and passwords for public-facing devices (routers, Web Application Firewalls, etc.).
- Disable directory listing and set proper permissions for every file and folder.
- Remove unnecessary code snippets and error logs, and turn off debugging while the code is in production.

### Questions
- It is not a good approach to display error logs from the stack trace to general visitors.
- HTTP response code: `500`.
- Error ID: `1401`.

---

## Vulnerability VIII - Injection

### Notes
- Occurs when user input is not filtered and is directly processed by an API.
- Injection may come from SQL, operating system (OS) commands, XML, and more.
- Ensure use of a well-known library for client-side input validation.
- If a framework is not used, all client-provided data must be validated, filtered, and sanitized before processing.
- Add necessary security rules to the Web Application Firewall (WAF) — most injection flaws can be mitigated at the network level.
- Make use of built-in filters in frameworks like Laravel and CodeIgniter to validate and filter data.

### Questions
- First question: `yes`.
- Second question: `yes`.
- HTTP response code for an incorrect password: `403`.

---

## Vulnerability IX - Improper Assets Management

### Notes
- Occurs when multiple versions of an API are available in a system and older versions are not properly retired.
- A properly maintained, up-to-date API inventory and documentation are more critical than hardware-based security controls for an organisation.
- Access to previously developed sensitive and deprecated API calls must be blocked at the network level.
- APIs developed for R&D, QA, production, etc., must be segregated and hosted on separate servers.
- Ensure documentation of all API aspects, including authentication, redirects, errors, CORS policy, and rate limiting.
- Adopt open standards to generate documentation automatically.

### Questions
- It is not good practice to host all APIs on the same server.
- Alice's balance is `100`.
- Alice's country is `USA`.

---

## Vulnerability X - Insufficient Logging and Monitoring

### Notes
- Occurs when there is not enough evidence available due to the absence of logging and monitoring mechanisms.
- Ensure use of a Security Information and Event Management (SIEM) system for log management.
- Keep track of all denied accesses, failed authentication attempts, and input validation errors using a format compatible with SIEM, with enough detail to identify an intruder.
- Handle logs as sensitive data and ensure their integrity at rest and in transit. Implement custom alerts to detect suspicious activities.

### Questions
- API logs should not be publicly accessible.
- A `200` response code indicates a successful login.
