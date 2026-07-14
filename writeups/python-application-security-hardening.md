# Python Application Security Hardening

## Authentication, Secrets Management, and Access Control

## Overview

This project focused on improving the security posture of an existing Python Flask application by remediating multiple application security vulnerabilities. The remediation included replacing hardcoded secrets with environment variables, implementing PBKDF2-SHA256 password hashing, enforcing API key authentication, introducing role-based access control (RBAC), and validating the implementation through automated security testing.

These improvements strengthened the application's authentication and authorization mechanisms while reducing the risk of credential exposure, unauthorized access, and insecure application configuration.

---

# Project Objectives

The primary objectives of this project were to:

- Replace hardcoded secrets with secure configuration management.
- Eliminate plaintext password storage.
- Implement secure password hashing using PBKDF2-SHA256.
- Require API authentication before accessing protected resources.
- Enforce role-based authorization using the principle of least privilege.
- Validate each security control through automated testing.

---

# Initial Assessment

Before implementing any changes, I reviewed the application's source code to identify security weaknesses that could expose sensitive information or allow unauthorized access.

The review identified several vulnerabilities:

- Sensitive application secrets were hardcoded directly in the source code.
- User passwords were stored in plaintext.
- Protected API endpoints lacked authentication.
- Authorization checks did not properly restrict user permissions.
- Security controls had limited automated validation.

These findings established the remediation plan implemented throughout the project.

---

# Security Improvements

## Secure Secrets Management

Hardcoded application secrets were replaced with environment variables to prevent sensitive credentials from being stored directly within the application's source code. Secure random values are generated when environment variables are unavailable, allowing the application to operate safely during development without relying on predictable default credentials.

> Screenshot:
> Secure Secret Management Using Environment Variables

---

## Password Security

Plaintext password storage was replaced with PBKDF2-SHA256 password hashing. User credentials are now stored as password hashes rather than plaintext, significantly reducing the risk of credential exposure if the user database is compromised.

> Screenshot:
> PBKDF2-SHA256 Password Hashing Implementation

---

## Secure Password Verification

Authentication was updated to verify user credentials using password hash verification instead of direct plaintext password comparison. This allows the application to authenticate users without storing or exposing their original passwords.

> Screenshot:
> Secure Password Verification Using check_password_hash()

---

## API Authentication

Protected API endpoints now require a valid Bearer token before granting access. Requests containing missing or invalid API keys are rejected, preventing unauthorized users from accessing protected resources.

> Screenshot:
> Bearer Token Authentication

---

## Role-Based Access Control

Role-based access control (RBAC) was implemented to enforce the principle of least privilege. Administrative endpoints now require administrator privileges, preventing lower-privileged users from accessing restricted functionality.

> Screenshot:
> Role-Based Authorization Implementation

---

# Testing & Verification

After implementing the security improvements, the application was validated using automated security tests to confirm each remediation functioned as expected.

## Automated Security Testing

Automated tests were executed using **pytest** to verify that each security control operated correctly after remediation.

> Screenshot:
> Successful Pytest Execution

---

## Security Validation

Individual test cases verified:

- Hardcoded secrets were successfully removed.
- Password hashing replaced plaintext password storage.
- API authentication rejected unauthorized requests.
- Role-based authorization enforced least privilege.

> Screenshot:
> Security Test Results

---

# Lessons Learned

This project demonstrated how multiple application security vulnerabilities can be mitigated through secure coding practices. Replacing hardcoded secrets, protecting passwords with modern hashing algorithms, enforcing authentication and authorization, and validating functionality through automated testing significantly improved the application's overall security posture.

---

# Skills Demonstrated

- Python
- Flask
- Application Security
- Secrets Management
- Environment Variables
- PBKDF2-SHA256
- Password Hashing
- Password Verification
- API Authentication
- Role-Based Access Control (RBAC)
- Secure Coding Practices
- Automated Testing (Pytest)
- Software Security Testing
