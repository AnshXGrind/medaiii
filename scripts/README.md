# Scripts Directory

This directory contains utility scripts for setup, migrations, and maintenance.

## Available Scripts

### Setup Scripts

- **`QUICK_SETUP.ps1`** - Quick setup wizard for Windows
  ```powershell
  .\scripts\QUICK_SETUP.ps1
  ```

- **`setup-universal-health-id.ps1`** - Sets up Universal Health ID system
  ```powershell
  .\scripts\setup-universal-health-id.ps1
  ```

### Migration Scripts

- **`apply-migration.ps1`** / **`apply-migration.mjs`** - Apply specific database migration
  ```powershell
  .\scripts\apply-migration.ps1 <migration-name>
  ```
  ```bash
  node scripts/apply-migration.mjs <migration-name>
  ```

- **`apply-migrations-auto.mjs`** - Automatically apply all pending migrations
  ```bash
  node scripts/apply-migrations-auto.mjs
  ```

- **`check-migration.mjs`** - Check migration status
  ```bash
  node scripts/check-migration.mjs
  ```

- **`verify-migration.ps1`** - Verify migration was applied correctly
  ```powershell
  .\scripts\verify-migration.ps1
  ```

- **`run-rls-migration.ps1`** - Apply Row Level Security policies
  ```powershell
  .\scripts\run-rls-migration.ps1
  ```

### Utility Scripts

- **`health-id-check.js`** - Validate Health ID implementation
  ```bash
  node scripts/health-id-check.js
  ```

### Server Scripts

- **`START_SERVER.bat`** - Start development server (Windows)
  ```cmd
  scripts\START_SERVER.bat
  ```

## Usage Examples

### First Time Setup

```powershell
# Windows - Quick setup
.\scripts\QUICK_SETUP.ps1

# Apply migrations
node scripts/apply-migrations-auto.mjs

# Verify everything works
node scripts/health-id-check.js
```

### Applying New Migrations

```bash
# Check current migration status
node scripts/check-migration.mjs

# Apply specific migration
node scripts/apply-migration.mjs add_vaccination_table

# Verify it worked
.\scripts\verify-migration.ps1
```

### Running with npm

Some scripts can be run via npm commands (check `package.json`):

```bash
npm run migrate        # Run migrations
npm run migrate:check  # Check migration status
```

## Prerequisites

- **Node.js** 20+ for `.mjs` scripts
- **PowerShell** for `.ps1` scripts (Windows)
- **Supabase CLI** (optional, for advanced migrations)
- Environment variables configured in `.env.local`

## Adding New Scripts

When adding a new script:

1. Place it in this directory
2. Add documentation to this README
3. Use clear, descriptive names
4. Include usage examples
5. Add error handling
6. Test thoroughly

## Common Issues

### "Cannot be loaded because running scripts is disabled"

**Windows PowerShell**: Run as Administrator:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### "Module not found" in .mjs scripts

Make sure you're in the project root:
```bash
cd /path/to/medaiii
node scripts/your-script.mjs
```

### Migration already applied

Check with:
```bash
node scripts/check-migration.mjs
```

## Need Help?

- Check [docs/guides/MIGRATION_GUIDE.md](../docs/guides/MIGRATION_GUIDE.md)
- Review [docs/deployment/DEPLOYMENT.md](../docs/deployment/DEPLOYMENT.md)
- Open an issue on GitHub
