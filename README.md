# Django Backend Core Foundation

This repository contains the core backend foundation for a multi-tenant Django application with:

- Organization (tenant) isolation
- Role-Based Access Control (RBAC)
- Centralized audit logging
- Swagger/OpenAPI documentation

## Apps Included
- accounts (users, roles, permissions)
- orgs (tenants)
- vendors
- templates
- assessments
- evidence
- reviews
- remediations
- renewals
- audit

## Key Features
- `org_id` enforced on all org-scoped models
- Cross-tenant access blocked (403)
- Custom DRF permissions: Admin, Reviewer, Requester, Vendor
- Central audit service for critical write actions
- Swagger docs enabled via drf-spectacular

## Setup
```bash
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
