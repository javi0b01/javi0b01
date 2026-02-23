# :memo: Notes
## BRAINSTORMING
### GMS
Garage Management Software or Garage Management System  
A multi-tenant business management platform for automotive service companies.

- Simple SaaS
- multi-tenant SaaS
- single database, shared tables
- Single database + tenant_id column
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
  - one single paid plan
  - One subscription per tenant
  - Store plan type
  - Store expiration date
  - Sell monthly subscription
  - Sell yearly subscription
  - Manual control

* Deployment Strategy
  - Gunicorn
  - Nginx
  - PostgreSQL
  - VPS (DigitalOcean, Hetzner, etc.)
  - All tenants use same app code.

* Data Isolation Security
  - ALWAYS filter by tenant first
  - Prevent Cross-Tenant Access
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
  * Backups
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

* Permission Logic
  - Django Superuser → full system access, creates organizations
  - Organization Admin → full access inside their organization, manages users inside their company

#### Stack
- Django Classic
- HTMX
- Tailwind
- AlpineJS
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

- Custom User (extends AbstractUser)
- Organization (your tenant)
- LoginHistory (immutable)
- ActivityLog (immutable)
- TimeStampedModel (abstract base)

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
  - Organization Admin
  - Manager
  - Assistant
  - Mechanic

---
PLANNING

1. Project setup — Foundation
- [ ] Project runs locally without errors
- [ ] Repository created (git initialized)
- [ ] Environment variables working
- [ ] Basic folder structure defined
- [ ] App starts with one test route/page

✅ You can run the project with one command.

2. Public landing page — Product entry
- [ ] Public home page loads
- [ ] Shows GMS name + description
- [ ] CTA buttons visible (placeholders OK)
- [ ] Accessible without login
- [ ] Basic navigation exists

✅ Anyone can open the app and understand what it is.


3. Auth & basic views — Access layer
- [ ] Login page UI exists
- [ ] Dashboard page exists
- [ ] Successful login redirects to dashboard
- [ ] Non-authenticated users cannot access dashboard

✅ User can enter the system.

4. Custom User + base models — Identity foundation
- [ ] Custom User model implemented
- [ ] Email used as login
- [ ] Organization model created
- [ ] Log/Audit model created (basic)
- [ ] Migrations run successfully

✅ Database schema represents system identity.

5. Database setup — Persistence
- [ ] PostgreSQL connected
- [ ] Migrations apply correctly
- [ ] Data can be created and retrieved
- [ ] Admin/console can view records

✅ Data survives server restart.

6. Auth flow validation — Security check
- [ ] Login works consistently
- [ ] Logout works
- [ ] Protected routes enforced
- [ ] Session/token persists correctly
- [ ] Unauthorized access redirects properly

✅ Authentication lifecycle confirmed.

7. Customer module — First business data
- [ ] Create customer
- [ ] Edit customer
- [ ] List customers
- [ ] Search or basic filtering
- [ ] Data linked to organization

✅ Garage can register clients.

8. Vehicle module — Operational context
- [ ] Create vehicle
- [ ] Vehicle linked to customer
- [ ] List customer vehicles
- [ ] Edit vehicle info
- [ ] Prevent vehicle without customer

✅ Each customer can own vehicles.

9. Work Order module — Core operation
- [ ] Create work order
- [ ] Select customer + vehicle
- [ ] Status field exists (open/closed/basic)
- [ ] List work orders
- [ ] View work order detail

✅ Garage can record real service activity.

* Sequence follows a healthy progression
  - Visibility → Access → Identity → Infrastructure → Business Data → Operations


CORE DOMAIN MAP

<pre>
LEVEL 0 — FOUNDATION (System Identity)
│
├── Organization (tenant)
└── User + Roles

        ↓

LEVEL 1 — CORE BUSINESS ENTITIES (THE HEART)
│
├── Customer
├── Vehicle
└── Work Order (Service Job)

        ↓

LEVEL 2 — OPERATIONAL DOMAIN
│
├── Services / Tasks
├── Mechanics assignment
├── Work Order Status
└── Notes & History

        ↓

LEVEL 3 — COMMERCIAL DOMAIN
│
├── Estimates
├── Invoices
└── Payments

        ↓

LEVEL 4 — SUPPORTING FEATURES
│
├── Dashboard
├── Reports
├── Notifications
└── Audit logs

        ↓

LEVEL 5 — EXPERIENCE LAYER
│
├── Public Landing Page
├── Login
└── UI Improvements
</pre>


ROADMAP
1. Project setup
2. Base layout + Tailwind
3. Custom User + Auth
4. Organization
5. Roles
6. Dashboard skeleton
7. Customers
8. Vehicles
9. Service catalog
10. Work Orders ⭐
11. Payments
12. HTMX enhancements

Phase 1 — SaaS Foundation
- Organization
- Custom User
- Roles
- Auth

Phase 2 — Core Domain ⭐
- Customer CRUD
- Vehicle CRUD
- Work Order CRUD

Phase 3 — Operations
- Services/tasks
- Status workflow
- Assign mechanic

Phase 4 — Money
- Estimates
- Invoice
- Payments

Phase 5 — Insights
- Dashboard
- Reports

Phase 6 — Experience
- Landing page
- UI polish

⭐ The Key Rule (Remember This)  
- Anything that creates business value goes first.
- Anything that visualizes value goes later.

Very Important Mindset  
Do NOT build like: “What features can I add?”  
Build like: “What is the minimum system that a garage would pay $25/month for?”

That question will guide architecture.  
Build real.  
Refactor later.

---

## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
