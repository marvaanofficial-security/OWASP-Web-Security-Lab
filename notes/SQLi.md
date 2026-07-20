# SQL Injection (SQLi)

## Overview

SQL Injection is a web application vulnerability that allows an attacker to interfere with database queries by injecting malicious SQL code through user input.

## Lab Environment

- Application: OWASP Juice Shop
- Tool: Burp Suite Community Edition
- Platform: Kali Linux
- Environment: Docker

## Testing Method

- Intercepted HTTP requests using Burp Suite.
- Identified input fields that interacted with the backend.
- Performed SQL injection testing in the controlled lab environment.

## Potential Impact

- Unauthorized data access
- Authentication bypass
- Data modification
- Information disclosure

## Mitigation

- Use parameterized queries
- Validate and sanitize input
- Apply least-privilege database permissions
