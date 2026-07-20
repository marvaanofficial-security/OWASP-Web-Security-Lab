# Cross-Site Scripting (XSS)

## Overview

Cross-Site Scripting occurs when untrusted input is returned to a user's browser without proper validation or output encoding, allowing JavaScript to execute.

## Lab Environment

- OWASP Juice Shop
- Burp Suite
- Firefox
- Docker

## Testing Method

- Tested user input fields for reflected script execution in the lab.
- Observed how the application handled untrusted input.

## Potential Impact

- Session hijacking
- Credential theft
- Defacement
- Browser-based attacks

## Mitigation

- Output encoding
- Input validation
- Content Security Policy (CSP)
