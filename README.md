## Django Vulnerability Reporting Tracker

## Purpose
A web-based ticketing system where internal users can report and triage security vulnerabilities (e.g., XSS, CSRF) found in internal apps or pentests.

## Tech Stack
- **Framework**: Django
- **Security Focus**:
  - Authentication
  - Input validation
  - Data sensitivity
  - Access control

## OWASP Mapped Protections
- **A01**: Broken Access Control — Role-based view enforcement
- **A03**: Injection — Form sanitization and ORM usage
- **A05**: Security Misconfigurations — Middleware, secure cookies, HSTS

## Features
- Django Auth for login
- Submit vulnerability reports (title, type, severity, PoC)
- Tag reports by product/team
- Access-controlled views: reporters vs triagers
- Admin panel for full visibility
- Email alerts on critical vulnerabilities
- Docker support for easy deployment

## 🚀 Getting Started
```bash
# Clone the repo
$ git clone https://github.com/yourusername/django-vuln-tracker.git
$ cd django-vuln-tracker

# Build & run via Docker
$ docker-compose up --build

# Or run locally
$ python3 -m venv venv && source venv/bin/activate
$ pip install -r requirements.txt
$ python manage.py migrate
$ python manage.py runserver
```

## Admin Access
- Create a superuser:
```bash
$ python manage.py createsuperuser
```

## To Do
- Implement custom permissions for triager roles
- Add full email notification flow
- Add automated tests for forms & views
- Add PDF export for report summaries

## 📄 License
MIT
