# Project Organization Guide

This document explains the new organized structure of the MED-AID SAARTHI project.

## 📂 Directory Structure

```
medaiii/
├── 📄 Root Files (Essential only)
│   ├── README.md              # Main project overview
│   ├── CONTRIBUTING.md        # Full contribution guide
│   ├── CONTRIBUTING_SIMPLE.md # Quick start for contributors
│   ├── CHANGELOG.md           # Version history
│   ├── ROADMAP.md            # Future plans
│   ├── package.json          # Dependencies and scripts
│   ├── *.config.{js,ts}      # Configuration files
│   └── docker-compose.yml    # Docker setup
│
├── 📚 docs/                   # All documentation (organized!)
│   ├── README.md             # Documentation index
│   ├── guides/               # Setup and how-to guides
│   ├── features/             # Feature-specific docs
│   ├── deployment/           # Deployment guides
│   ├── security/             # Security documentation
│   └── implementation/       # Technical implementation details
│
├── 💻 src/                    # Source code
│   ├── components/           # React components
│   ├── pages/               # Page components
│   ├── contexts/            # React contexts
│   ├── hooks/               # Custom hooks
│   ├── lib/                 # Utilities
│   └── integrations/        # Third-party integrations
│
├── 🔧 scripts/               # Utility scripts
│   ├── README.md            # Scripts documentation
│   ├── *.ps1                # PowerShell scripts
│   ├── *.mjs                # Migration scripts
│   └── *.js                 # Utility scripts
│
├── 🧪 tests/                 # Test files
│   └── *.html               # Test pages
│
├── 🗄️ supabase/              # Database
│   └── migrations/          # SQL migrations
│
├── 🐳 docker/                # Docker configs
│   └── nginx.conf           # Nginx config
│
├── 📱 mobile/                # React Native app
│   └── ...
│
├── 🔌 backend-modules/       # Optional backend services
│   └── ...
│
└── 🌍 public/                # Static assets
    └── ...
```

## 🎯 Benefits of This Organization

### For New Contributors

✅ **Cleaner root directory** - Essential files only at root level  
✅ **Organized docs** - Easy to find information  
✅ **Clear structure** - Know where to add new files  
✅ **Better onboarding** - Simplified CONTRIBUTING guide

### For Maintainers

✅ **Easier maintenance** - Logical grouping of files  
✅ **Better navigation** - Less clutter  
✅ **Scalable** - Easy to add new documentation  
✅ **Professional** - Industry-standard structure

## 📖 Documentation Organization

### docs/guides/
Setup guides, quick starts, integrations, and how-tos:
- Quick start guides
- Setup instructions
- Migration guides
- Integration documentation

### docs/features/
Feature-specific documentation:
- Health ID system
- Vaccination reminders
- Village mode
- PWA features

### docs/deployment/
Everything related to deploying the application:
- Deployment guides
- Checklists
- Environment setup

### docs/security/
Security policies and compliance:
- Security policy
- Audit reports
- Compliance guides
- Secret management

### docs/implementation/
Technical implementation details:
- Architecture decisions
- Implementation summaries
- Technical specifications

## 🔍 Finding Information

### I want to...

| Goal | Location |
|------|----------|
| Set up locally | [docs/guides/QUICK_START.md](docs/guides/QUICK_START.md) |
| Contribute code | [CONTRIBUTING_SIMPLE.md](CONTRIBUTING_SIMPLE.md) |
| Deploy to production | [docs/deployment/DEPLOYMENT.md](docs/deployment/DEPLOYMENT.md) |
| Understand features | [docs/features/](docs/features/) |
| Run scripts | [scripts/README.md](scripts/README.md) |
| Security info | [docs/security/SECURITY.md](docs/security/SECURITY.md) |
| System architecture | [docs/SYSTEM_OVERVIEW.md](docs/SYSTEM_OVERVIEW.md) |

## 📝 Adding New Files

### Documentation

```bash
# Feature docs
docs/features/new-feature.md

# Setup guides
docs/guides/setup-xyz.md

# Deployment info
docs/deployment/deploy-to-xyz.md
```

**Remember to update** [docs/README.md](docs/README.md)!

### Scripts

```bash
# Add to scripts directory
scripts/your-script.{ps1,mjs,js}

# Document in scripts/README.md
```

### Source Code

```bash
# Components
src/components/YourComponent.tsx

# Pages
src/pages/YourPage.tsx

# Utilities
src/lib/yourUtility.ts
```

## 🚀 Quick Start Paths

### For Contributors

1. **Start here**: [README.md](README.md)
2. **Set up**: [CONTRIBUTING_SIMPLE.md](CONTRIBUTING_SIMPLE.md)
3. **Understand structure**: This file
4. **Find docs**: [docs/README.md](docs/README.md)
5. **Start coding!**

### For Reviewers

1. **System overview**: [docs/SYSTEM_OVERVIEW.md](docs/SYSTEM_OVERVIEW.md)
2. **Architecture**: [docs/STRATEGIC_SUMMARY.md](docs/STRATEGIC_SUMMARY.md)
3. **Security**: [docs/security/SECURITY.md](docs/security/SECURITY.md)

### For Deployers

1. **Deployment guide**: [docs/deployment/DEPLOYMENT.md](docs/deployment/DEPLOYMENT.md)
2. **Checklist**: [docs/deployment/DEPLOYMENT_CHECKLIST.md](docs/deployment/DEPLOYMENT_CHECKLIST.md)
3. **Scripts**: [scripts/README.md](scripts/README.md)

## 🎨 Maintaining This Structure

### Best Practices

✅ **Keep root clean** - Only essential config files  
✅ **Organize by purpose** - Group related files together  
✅ **Update indexes** - Keep README files current  
✅ **Clear naming** - Use descriptive file names  
✅ **Consistent structure** - Follow established patterns

### When to Create New Directories

Create a new subdirectory when:
- You have 5+ related files
- Files form a logical group
- It improves clarity

### Don't Forget

- Update documentation indexes
- Add README files to new directories
- Link from main README
- Keep CHANGELOG updated

## 📊 Migration Summary

### What Changed?

- **40+ documentation files** moved from root to `docs/`
- **10+ scripts** moved from root to `scripts/`
- **Test files** moved to `tests/`
- **Documentation organized** into logical subdirectories
- **New README files** created for navigation

### What Stayed in Root?

- Essential project files (README, CONTRIBUTING, package.json)
- Configuration files (*.config.*, docker-compose.yml)
- Version control files (.gitignore, .env.example)

### Breaking Changes?

❌ **None!** All paths are relative within the project.  
✅ Links updated in main README  
✅ Documentation index created  
✅ Scripts directory documented

## 🤝 Questions?

- Check [docs/README.md](docs/README.md) for complete documentation index
- See [CONTRIBUTING_SIMPLE.md](CONTRIBUTING_SIMPLE.md) for contribution guidelines
- Open an issue on GitHub

---

**This organization makes the project more accessible and professional. Thank you for maintaining this structure!** 🎉
