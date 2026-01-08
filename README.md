# MED-AID SAARTHI

**A consent-first digital health records platform designed to bridge healthcare access gaps in India.**

This is a **flagship portfolio project** built by a BTech student focusing on product design, system architecture, and user-centered healthcare UX. It demonstrates full-stack capabilities, ethical design decisions, and understanding of complex domain constraints — not a production medical system.

---

## 🎯 Who This Project Is For

- **Recruiters & Hiring Managers**: Evaluating full-stack product + design capabilities in a complex domain
- **Open Source Contributors**: Learning healthcare system design patterns and React/Supabase architecture  
- **Design Reviewers**: Assessing consent flows, emergency access logic, and low-literacy UX considerations

---

## 📊 Project Status & Scope

This is a phased flagship project.

**Phase 1 (Implemented MVP)**
- Health ID creation with privacy-safe identifiers
- Patient and doctor dashboards
- Appointment workflows
- Emergency routing with location-based discovery
- Multi-language UI foundation
- PWA setup for mobile-first access

**Phase 2 (Designed & Partially Implemented)**
- Vaccination reminders and offers modules
- Extended admin workflows
- Optional backend services for search and routing
- Documentation for ABHA/NDHM-aligned flows (non-production)

**Phase 3 (Planned / Vision)**
- Deeper interoperability with national health systems
- Advanced analytics on anonymized data
- Expanded accessibility and offline-first support

---

## 🧠 Design Decisions & Tradeoffs

- Avoided live medical diagnosis or clinical decision-making to reduce ethical and regulatory risk.
- Prioritized consent-driven access and privacy boundaries before AI features.
- Chose Supabase with RLS to enforce data isolation at the database level.
- Focused on frontend and UX clarity over backend complexity in early phases.

---

## 🚀 Project Demo

**Live preview:** https://medaiii.vercel.app

**Suggested walkthrough:**
1. Create a health ID
2. Explore the patient dashboard
3. View emergency routing flow
4. Switch language context

---

## 💡 Problem Statement

Healthcare record fragmentation disproportionately affects underserved populations. Patients lose paper records, switch providers without continuity, and face language barriers in understanding medical information. 

MED-AID SAARTHI explores how **consent-first digital infrastructure** could enable:
- Patient-owned record portability
- Emergency access without compromising daily privacy
- Low-literacy UX for health information comprehension
- Interoperability aligned with India's ABDM standards

This is a **design exploration and technical prototype**, not a licensed medical platform.

---

## 📢 Recommended Hero Copy (Landing Page)

**For product messaging that prioritizes trust and clarity over hype:**

### Option A: Records-First Positioning
**Headline:**  
"Your Health Records. Your Control. Anywhere You Need Them."

**Subheadline:**  
"A consent-first digital vault for medical documents with emergency access design and privacy-aware sharing."

### Option B: Access-Focused Positioning
**Headline:**  
"Healthcare Access Without the Paperwork Chaos"

**Subheadline:**  
"Store prescriptions, share with doctors securely, and access your health history from any device — designed for India's diverse healthcare landscape."

### Option C: Trust-Centered Positioning (Recommended)
**Headline:**  
"Healthcare Records That Put You in Charge"

**Subheadline:**  
"A student-built prototype exploring consent-first record management, emergency access patterns, and interoperability for India's digital health infrastructure."

**Why this works:**  
- Emphasizes user agency over AI magic
- Transparently frames the project scope
- Highlights system design over feature count
- Builds trust through honesty

**Avoid:**  
- "AI-powered healthcare revolution"
- "Blockchain-secured medical records"
- "Real-time disease prediction"
- "Government-certified platform"

---

## 🏗️ Core Features (What's Actually Built)

### Record Management & Privacy
- **Privacy-aware Health ID**: Aadhaar never stored in full — only hashed tokens with last-4 display
- **Document Upload**: Secure storage for prescriptions, reports, and health documents (Supabase backend)
- **Consent-First Sharing**: Record access requires explicit user authorization (UI designed, partial backend)

### User Experience
- **Role-Based Dashboards**: Separate patient and doctor interfaces with contextual navigation
- **Emergency Routing**: Location-based hospital discovery for urgent care scenarios
- **Vaccination Tracking**: Multi-dose reminder interface with schedule management
- **Low-Literacy UX**: Visual workflows, large touch targets, simplified language options
- **PWA Installation**: Mobile-first design with offline capability scaffolding

### Technical Foundations
- **Authentication**: Supabase Auth with role-based access control
- **Database**: PostgreSQL with Row-Level Security (RLS) policies for data isolation
- **Multi-Language Architecture**: i18n infrastructure (English/Hindi contexts wired)
- **Real-Time Ready**: Supabase Realtime subscriptions configured (not actively used in MVP)

## Architecture and Tech Stack

- Frontend: React 18 + TypeScript, Vite, React Router, TanStack Query
- UI: shadcn-ui components, Radix primitives, Tailwind CSS
- Data: Supabase (PostgreSQL, RLS) and Supabase Realtime where enabled
- Mapping: Google Maps / OpenStreetMap integrations (see `integrations/`)
- PWA: Vite PWA plugin and `PWAInstallPrompt` component
- Optional services: `backend-modules` for search and supporting APIs

## Repository Structure

```
medaiii/
├── src/                    # React application source code
│   ├── components/         # Reusable UI components
│   ├── pages/             # Page components and routes
│   ├── contexts/          # React contexts (auth, language, etc.)
│   ├── hooks/             # Custom React hooks
│   ├── lib/               # Utility functions and helpers
│   └── integrations/      # Third-party integrations (Maps, etc.)
├── public/                # Static assets and PWA icons
├── backend-modules/       # Optional backend services (search API, etc.)
├── supabase/             # Database migrations and seed data
├── scripts/              # Utility scripts (migrations, setup, etc.)
├── tests/                # Test files and utilities
├── docs/                 # 📚 All documentation (see below)
├── docker/               # Docker and nginx configuration
└── mobile/               # React Native mobile app
```

### 📚 Documentation

All project documentation is organized in the [docs/](docs) directory:

- **[docs/guides/](docs/guides)** - Setup guides, quick starts, and how-tos
- **[docs/features/](docs/features)** - Feature-specific documentation (Health ID, Vaccination, etc.)
- **[docs/deployment/](docs/deployment)** - Deployment guides and checklists
- **[docs/security/](docs/security)** - Security policies and compliance guides
- **[docs/implementation/](docs/implementation)** - Implementation summaries and technical details

**📖 Full documentation index**: [docs/README.md](docs/README.md)

Key documents:
- [CONTRIBUTING_SIMPLE.md](CONTRIBUTING_SIMPLE.md) - Quick start for contributors
- [PROJECT_ORGANIZATION.md](PROJECT_ORGANIZATION.md) - Understanding the project structure
- [CHANGELOG.md](CHANGELOG.md) - Version history and changes
- [ROADMAP.md](ROADMAP.md) - Future plans and features

## Getting Started

### Prerequisites

- Node.js 20+ and npm 10+
- Supabase project (for database and RLS-enabled auth)
- Optional: Docker for local containerized runs

### Quick Setup

```bash
# Clone the repository
git clone https://github.com/AnshXGrind/medaiii.git
cd medaiii

# Install dependencies
npm install

# Set up environment (copy and edit with your Supabase credentials)
cp .env.example .env.local
```

**📖 Detailed setup guide**: [docs/guides/QUICK_START.md](docs/guides/QUICK_START.md)  
**👥 Contributing**: [CONTRIBUTING_SIMPLE.md](CONTRIBUTING_SIMPLE.md)

### Environment configuration

1. Create an `.env.local` file for the frontend and add Supabase keys and URLs. See [docs/deployment/DEPLOYMENT.md](docs/deployment/DEPLOYMENT.md) for required variables.
2. Apply Supabase migrations from [supabase/](supabase) to set up tables and RLS policies. Run `npm run migrate` or use scripts in [scripts/](scripts).
3. (Optional) Configure `backend-modules/.env` if running search or auxiliary services locally.

### Run locally

```bash
npm run dev
```

The app will start at `http://localhost:5173`. The dev server uses Vite and supports hot module replacement.

### Quality checks

- Lint: `npm run lint`
- Build verification: `npm run build`
- Preview production build: `npm run preview`

Automated tests are not yet wired; add targeted tests under `src/__tests__/` when contributing.

## 🔒 Security & Privacy Practices

**Implemented Controls:**
- Aadhaar numbers hashed with salt, never stored or transmitted in full
- Last-4 digits displayed for user verification only
- Supabase RLS policies enforce user-level data isolation
- HTTPS enforced for all data transmission
- Session-based authentication with secure token storage

**Design Patterns (Not All Enforced in Code):**
- Consent logging for record access (designed, partially implemented)
- Audit trails for sensitive operations (schema exists, logging incomplete)
- Time-limited share tokens for doctor access (designed, not wired)
- Emergency override with audit requirements (documented in [docs/security/](docs/security))

**Review before modifying:**  
- [docs/security/SECURITY.md](docs/security/SECURITY.md) - Security architecture and threat model
- [docs/guides/MIGRATION_GUIDE.md](docs/guides/MIGRATION_GUIDE.md) - RLS policy management

**What's NOT implemented:**  
- End-to-end encryption (records encrypted at rest by Supabase, not E2EE)
- Multi-factor authentication (planned, not active)
- Penetration testing or security audits (no external review conducted)

## 🛣️ Roadmap & Future Work

**Next Milestones (If Continued):**
1. Connect AI summarization pipeline (OCR + NLP for uploaded reports)
2. Implement secure share token generation with expiry logic
3. Add automated testing (unit + integration coverage)
4. Conduct accessibility audit and WCAG compliance review
5. Real ABDM sandbox integration (requires institutional partnership)

**Long-Term Vision (Research Phase):**
- Pharmacy integration for medication adherence
- Lab test result ingestion and interpretation
- Public health analytics (anonymized, aggregated data only)
- Wearable device sync for vitals tracking

**See full roadmap:** [ROADMAP.md](ROADMAP.md)

---

## 🤝 Contributing & Learning

This project welcomes contributors interested in:
- Healthcare UX/UI design patterns
- Consent and privacy architecture
- Low-literacy interface design
- React/TypeScript/Supabase full-stack development

**Start here:**  
- [CONTRIBUTING_SIMPLE.md](CONTRIBUTING_SIMPLE.md) - Quick contributor guide
- [docs/guides/QUICK_START.md](docs/guides/QUICK_START.md) - Local development setup
- [PROJECT_ORGANIZATION.md](PROJECT_ORGANIZATION.md) - Codebase structure walkthrough

**Good first issues:**  
- Add unit tests for authentication flows
- Improve accessibility scores in Lighthouse audits
- Translate existing UI strings to additional Indian languages
- Document API response shapes for backend modules

---

## ⚖️ Legal & Disclaimers

**MIT License** - See [LICENSE](LICENSE) for details

**Not a Medical Device:**  
This software is a student portfolio project demonstrating system design capabilities. It is NOT:
- A licensed medical device or diagnostic tool
- Approved for clinical use or patient care
- Compliant with HIPAA, FDA, or other healthcare regulations
- Suitable for storing real patient health information

**Data Responsibility:**  
Do not upload real medical records or personally identifiable health information to the demo deployment. Any data you enter should be considered test data only.

**Use at Your Own Risk:**  
This software is provided "as is" without warranty. See license for full disclaimer.
