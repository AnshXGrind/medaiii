# Contributing to MED-AID SAARTHI

🎉 Thank you for contributing! This guide will help you get started quickly.

## 📋 Quick Start

### 1. Prerequisites

- **Node.js** v20+ and **npm** v10+ ([Download](https://nodejs.org/))
- **Git** ([Download](https://git-scm.com/))
- **Supabase account** (free tier)
- **Code editor** (VS Code recommended)

### 2. Fork and Clone

```bash
# Fork the repo on GitHub, then:
git clone https://github.com/YOUR_USERNAME/medaiii.git
cd medaiii
npm install
```

### 3. Set Up Environment

```bash
# Copy environment template
cp .env.example .env.local

# Add your Supabase credentials
# See docs/deployment/DEPLOYMENT.md for details
```

### 4. Run Locally

```bash
npm run dev
# Visit http://localhost:5173
```

### 5. Make Your Changes

1. **Create a branch**: `git checkout -b feature/your-feature`
2. **Make changes** in the appropriate directory
3. **Test locally**: `npm run dev` and `npm run lint`
4. **Commit**: `git commit -m "Clear description of changes"`
5. **Push**: `git push origin feature/your-feature`
6. **Create Pull Request** on GitHub

## 📁 Project Structure

```
medaiii/
├── src/                # Frontend React code
│   ├── components/     # UI components
│   ├── pages/         # Page routes
│   ├── lib/           # Utilities
│   └── contexts/      # React contexts
├── docs/              # 📚 All documentation
├── supabase/          # Database migrations
├── scripts/           # Setup scripts
└── tests/             # Test files
```

**Pro tip**: Check [docs/README.md](docs/README.md) for complete documentation index!

## 🎯 What to Work On

### Good First Issues

Look for issues tagged with `good-first-issue` or:
- Documentation improvements
- UI/UX enhancements  
- Test coverage
- Bug fixes

### Priority Areas

- Accessibility improvements
- Mobile responsiveness
- Performance optimizations
- Test coverage
- Documentation

## 💻 Development Guidelines

### Code Style

- **TypeScript**: Use strict typing
- **React**: Functional components with hooks
- **Naming**: Clear, descriptive names
- **Comments**: Explain "why", not "what"

### File Organization

- **Components**: `src/components/ComponentName.tsx`
- **Pages**: `src/pages/PageName.tsx`
- **Utilities**: `src/lib/utilityName.ts`
- **Types**: Define in the same file or `types.ts`

### Before Submitting

```bash
# Run linter
npm run lint

# Build to check for errors
npm run build

# Test your changes manually
npm run dev
```

## 🔒 Security

- **Never commit**: API keys, passwords, or sensitive data
- **Review**: [docs/security/SECURITY.md](docs/security/SECURITY.md) before touching auth code
- **Report vulnerabilities**: Email security@medaidsathi.com (do not open public issues)

## 📝 Pull Request Guidelines

### PR Checklist

- [ ] Clear, descriptive title
- [ ] Detailed description of changes
- [ ] Tested locally
- [ ] No console errors
- [ ] Lint passes
- [ ] Screenshots (for UI changes)
- [ ] Documentation updated (if needed)

### PR Description Template

```markdown
## What does this PR do?
Brief description of changes

## Type of change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring

## How to test
1. Step 1
2. Step 2
3. Expected result

## Screenshots (if applicable)
[Add screenshots here]
```

## 🐛 Reporting Bugs

**Before reporting**:
1. Check existing issues
2. Try the latest version
3. Search documentation

**Bug report should include**:
- Clear description
- Steps to reproduce
- Expected vs actual behavior
- Screenshots/error messages
- Environment (OS, browser, Node version)

## 💡 Suggesting Features

We love feature ideas! Please:
1. Check if it's already suggested
2. Explain the use case
3. Describe the solution
4. Consider alternatives

## 📚 Documentation

### Improving Docs

Documentation is in the `docs/` directory:
- **Guides**: Setup and how-tos
- **Features**: Feature-specific docs
- **Deployment**: Deployment guides
- **Security**: Security policies

### Documentation Style

- Use clear, simple language
- Include code examples
- Add screenshots when helpful
- Keep it updated with code changes

## 🤝 Code of Conduct

### Be Kind

- Respectful and constructive feedback
- Welcome newcomers
- Assume good intentions
- Focus on the code, not the person

### Unacceptable

- Harassment or discrimination
- Trolling or insulting comments
- Publishing private information

**Report issues**: security@medaidsathi.com

## 🎓 Learning Resources

### New to the Stack?

- [React Docs](https://react.dev/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Supabase Docs](https://supabase.com/docs)
- [Tailwind CSS](https://tailwindcss.com/docs)

### Project-Specific

- [System Overview](docs/SYSTEM_OVERVIEW.md)
- [Quick Start Guide](docs/guides/QUICK_START.md)
- [Health ID Guide](docs/features/HEALTH_ID_QUICK_START.md)

## ❓ Getting Help

### Stuck? Try:

1. **Documentation**: Check [docs/README.md](docs/README.md)
2. **Search Issues**: Someone might have faced the same problem
3. **Ask Questions**: Open a discussion on GitHub
4. **Discord/Slack**: Join our community (link in README)

### Common Issues

- **Port already in use**: Change port in `vite.config.ts`
- **Module not found**: Run `npm install`
- **Build errors**: Check Node/npm versions
- **Supabase errors**: Verify credentials in `.env.local`

## 🌟 Recognition

Contributors are recognized in:
- README.md contributors section
- Release notes
- Project documentation

Thank you for making healthcare more accessible! 🏥

---

**Questions?** Open an issue or check [docs/README.md](docs/README.md) for more details.
