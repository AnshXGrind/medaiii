# MED-AID SAARTHI

A privacy-first healthcare platform focused on bridging care gaps across India. The project delivers digital health IDs, appointment workflows, emergency routing, and privacy-aware data handling with Supabase-backed storage and a Vite + React frontend.

## Problem Statement

Access to secure, interoperable healthcare records is limited across many regions. MED-AID SAARTHI aims to provide a unified, privacy-conscious experience for patients, doctors, and administrators while aligning with ABHA/NDHM standards and minimizing exposure of sensitive identifiers.

## Features

- Secure health ID creation with hashed Aadhaar tokens and last-4 display only
- Patient and doctor dashboards with routing, appointments, and records views
- Emergency assistance with location-based hospital discovery
- Vaccination reminders and offers modules
- Multi-language support via shared language context
- Progressive Web App install prompts for mobile-first access

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

## Security and Privacy Practices

- Aadhaar numbers are never stored in full; only hashed tokens with last-4 display
- Review [docs/security/SECURITY.md](docs/security/SECURITY.md) before making changes to auth or data access
- Follow Supabase RLS guidance when modifying schemas (see [docs/guides/MIGRATION_GUIDE.md](docs/guides/MIGRATION_GUIDE.md))

## Future Improvements

- Add automated test coverage (unit and integration) for core flows
- Provide example `.env` templates scoped for local and staging use
- Harden CI with lint/build/test/security scanners
- Expand accessibility audits and multi-language content coverage

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
