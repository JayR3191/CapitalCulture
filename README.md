# Capital Culture™ (MVP)
**The Stock Exchange for Us, Built by Us**

Capital Culture™ is a functionality-first MVP for a cultural exchange where creators launch an **ICO — Initial Content Offering™** and supporters buy **Parts** (units) of creative assets (songs/videos/etc.). The MVP focuses on secure backend primitives: offerings, ownership ledger, orders, and auditability. UI and onboarding flows come later.

> **Core Concepts**
- **Asset**: A piece of content (e.g., a song)
- **Offering**: An ICO — Initial Content Offering™ tied to an asset
- **Parts**: Units purchased by fans/investors
- **Ledger**: The source of truth for ownership (append-only/auditable)

---

## Goals (MVP)
1. Secure user authentication (JWT) and role-based access (fan/artist/admin)
2. Create artists and register assets
3. Launch an offering (ICO — Initial Content Offering™) with total Parts + price per Part
4. Buy Parts (primary market) with atomic ledger updates
5. Provide holdings and transaction history
6. Create a clean base to add:
   - payments (Stripe/Aeropay)
   - secondary trading/matching
   - payouts (royalty distributions)
   - compliance modules (KYC/AML)

---

## Tech Stack (recommended)
- **Backend**: FastAPI (Python)
- **DB**: PostgreSQL
- **ORM**: SQLAlchemy 2.x
- **Migrations**: Alembic
- **Auth**: JWT (python-jose) + bcrypt (passlib)
- **Runtime**: Docker + docker-compose

---

## Project Structure (target)
```
/CapitalCulture
  /app
    /api
    /core
    /db
    /models
    /services
    /tests
  /alembic
  docker-compose.yml
  Dockerfile
  README.md
```

---

## Next Steps
- Establish FastAPI skeleton with auth, users, and health endpoints.
- Define database models and migrations for assets, offerings, and ledger.
- Implement core ledger service for atomic issuance and transfers.
- Document local development workflow.
