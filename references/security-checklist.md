# Security Checklist (OWASP-Based)

## General
- [ ] No secrets in code or git (use `.env`).
- [ ] Dependencies are audited (`npm audit`, `pip-audit`).
- [ ] Use HTTPS everywhere (no mixed content).

## Python (Flask/FastAPI)
- [ ] Secure headers (`Helmet.js` or `Secure-Cookies`).
- [ ] SQL Injection prevention (use ORM or parametrized queries).
- [ ] Rate limiting enabled (`Flask-Limiter`).

## Node.js (Express)
- [ ] Use `helmet` middleware.
- [ ] Input validation (Joi/Zod) on all endpoints.
- [ ] Sanitize HTML inputs (XSS prevention).

## Docker
- [ ] Run as non-root user.
- [ ] Pin base image versions (e.g. `python:3.11-slim`, not `latest`).
- [ ] Minimal base images (Alpine/Distroless).
