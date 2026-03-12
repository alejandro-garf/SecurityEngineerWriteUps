# OWASP API Security Top 10 - 1 | TryHackMe Writeup

---

## Understanding APIs - A Refresher

### Notes
- The middleware that facilitates the communication of two software components using a set of protocols and definitions.

### Questions
- 1 million records were dumped on the dark web to prove the legitimacy of the breach.

---

## Vulnerability I - BOLA (Broken Object Level Authorization)

### Notes
- Refers to Insecure Direct Object Reference — which occurs when a user uses the input functionality to gain access to resources they are not authorized to view or use.
- An authorization token must be added to fix this vulnerability.

### Questions
- There are only 3 employees.
- Change the ID to 2 to get the flag.
- Change the ID to 3 to get the username.

---

## Vulnerability II - Broken User Authentication

### Notes
- Usually occurs from an invalid implementation of authentication.
- A user can pass an authentication token with an email and no password.
- Do not expose sensitive credentials in GET or POST requests.

### Questions
- For the first question, change the email from `admin` to `hr`.
  - Token: `cOC%Aonyis%H)mZ&uJkuI?_W#4&m>Y`
- Paste the valid token into the header, change the method to GET, then call the details endpoint.
  - Answer: `China`
- It is not good practice to send a username and password in a GET request.

---

## Vulnerability III - Excessive Data Exposure

### Notes
- Instead of relying on the frontend to filter out excess data, only necessary data should be sent from the database.
- Ensure time-to-time review of the API response to guarantee it returns only legitimate data and check whether it poses any security issue.

### Questions
- For the first question, switch the ID from 1 to 2 using the insecure endpoint.
- For the second question, change the ID to 3.
- Network-level devices should not be used to control excessive data exposure — this must be managed through APIs programmatically.

---

## Vulnerability IV - Lack of Resources and Rate Limiting

### Notes
- Rate limiting is required to prevent excessive utilization of API resources.
- Implement a CAPTCHA to prevent requests from automated scripts and bots.
- Implement a limit on how often a client can call an API within a specified time frame and notify the client instantly when the limit is exceeded.
- Define maximum data sizes on all parameters and payloads (e.g., max string length, max number of array elements).

### Questions
- Rate limiting can be carried out at the network layer.
- HTTP response code: `200` — follow the steps in the task.
- Response message: `Invalid Email`.

---

## Vulnerability V - Broken Function Level Authorization

### Notes
- Occurs when a low-privileged user (e.g., sales) bypasses system checks and gains access to confidential data by impersonating a high-privileged user (e.g., Admin).
- Ensure proper design and testing of all authorization systems and deny all access by default.
- Ensure that operations are only permitted to users belonging to the authorized group.
- Regularly review API endpoints for functional level authorization flaws, keeping the application's group hierarchy and business logic in mind.

### Questions
- It is not good practice to send the `isAdmin` value through hidden fields in form requests.
- By hitting `/apirule5/users_v` with Alice's token and the header `isAdmin: 1`, the full API response reveals:
  - Alice's mobile number: `+1235322323`
  - Admin's address flag: `THM{3432$@#2!}`
