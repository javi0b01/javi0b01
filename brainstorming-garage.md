# :memo: Notes
## BRAINSTORMING
### Garage
Garage Management System  
A multi-tenant business management platform for automotive service companies.

- Simple SaaS
- multi-tenant SaaS
- single database, shared tables
- You must be careful with data isolation
- This is the most common SaaS pattern.
- Custom User Model
- Link user to tenant

* Tenant Resolution Strategy
  - Option A — Subdomain (Highly Recommended)
  - Option B — URL prefix

- Middleware to detect tenant
- Load tenant into request

* Subscription & Billing
  - One subscription per tenant
  - Store plan type
  - Store expiration date

* Deployment Strategy
  - Gunicorn
  - Nginx
  - PostgreSQL
  - VPS (DigitalOcean, Hetzner, etc.)
  - All tenants use same app code.

* Data Isolation Security
  - ALWAYS filter by tenant first
  - Never trust user input
  - Every business model must include tenant as foreing key (No exceptions)
  * ALWAYS Prevent Cross-Tenant Access
    - Use a Custom Manager (Advanced & Clean)
  * PostgreSQL Row-Level Security (Advanced)
    - Row Level Security (RLS)
  * Single DB strategy:
    - Daily automated backup
    - Restore full database
  * If one tenant asks for data export:
    - Filter by tenant
    - Generate CSV / Excel

* Migrations Strategy
  - One DB → One migration → All tenants updated.

* Backups
  - Automated daily backups.

* Data Modeling
  - Customer → has many Vehicles
  - Vehicle → has many WorkOrders
  - WorkOrder → generates Invoice
  - Invoice → has Payments

* One Tenant = Multiple Branches

* Pricing
  - Base subscription: $29/month
  - +$10 per additional branch

#### Stack
- Django Classic
- HTMX
- PostgreSQL

#### Architecture
- Monolith
- Modern Server-Driven Architecture
* Modular Monolith
  - Apps are isolated
  - No circular imports
  - Business logic inside services
  - Views are thin
- Clean Architecture Pattern (Recommended)

#### Structure
- Clean SaaS Monolith

#### MVP
- Minimum Viable Product

* Garage System
  - Customers
  - Vehicles
  - Work orders
  - Mechanics
  - Inventory
  - Invoices
  - Payments
  - Reports (PDF / Excel)
  - Roles (owner, mechanic, receptionist)

This is classic CRUD + business logic.

* Roles
  - Owner (see all branches)
  - Branch Manager
  - Mechanic
  - Receptionist

## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
