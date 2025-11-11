# Skill Distribution Guide (NPM Package)

> How to distribute your Claude Code skills as `npx claude-plugins skills install @your-org/skills/skill-name` packages for easy deployment and updates

## Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Creating NPM Package Structure](#creating-npm-package-structure)
4. [First Deployment](#first-deployment)
5. [Deploying Updates](#deploying-updates)
6. [User Installation Guide](#user-installation-guide)
7. [Version Management Best Practices](#version-management-best-practices)

---

## Overview

Current skills in `skills/` folder:
- card-news-generator
- card-news-generator-v2
- code-changelog
- codex
- codex-claude-cursor-loop
- codex-claude-loop
- flutter-init
- landing-page-guide
- meta-prompt-generator
- midjourney-cardnews-bg
- nextjs15-init
- prompt-enhancer
- web-to-markdown

**Goal:**
```bash
# Anthropic's approach
npx claude-plugins skills install @anthropics/skills/pptx

# Your skills (goal)
npx claude-plugins skills install @your-org/skills/card-news-generator
npx claude-plugins skills install @your-org/skills/flutter-init
```

---

## Prerequisites

### 1. Create NPM Account

```bash
# After creating account at npmjs.com
npm login

# Verify login
npm whoami
```

### 2. Choose Scoped Package Name

- **Use Organization**: `@your-org/skills` (recommended)
- **Use Personal Name**: `@username/skills`

Examples: `@bear2u/claude-skills`, `@suji-father/skills`

---

## Creating NPM Package Structure

### Option A: Create New Package Folder (Recommended)

```bash
# Create new package folder
mkdir claude-skills-package
cd claude-skills-package

# Initialize package.json
npm init -y
```

### Option B: Use Current Project As-Is

Add `package.json` to current `my-skills-hub` project

### Configure package.json

```json
{
  "name": "@your-org/claude-skills",
  "version": "1.0.0",
  "description": "Custom Claude Code skills collection - Developer productivity tools",
  "main": "index.js",
  "author": "Your Name <your.email@example.com>",
  "license": "MIT",
  "keywords": [
    "claude-code",
    "skills",
    "ai",
    "automation",
    "productivity"
  ],
  "files": [
    "skills/**/*",
    "README.md"
  ],
  "repository": {
    "type": "git",
    "url": "https://github.com/your-org/my-skills-hub"
  },
  "bugs": {
    "url": "https://github.com/your-org/my-skills-hub/issues"
  },
  "homepage": "https://github.com/your-org/my-skills-hub#readme"
}
```

**Key Configuration Explained:**
- `name`: NPM package name (must be scoped package starting with `@`)
- `version`: Semantic version (major.minor.patch)
- `files`: List of files/folders to include in NPM
- `keywords`: Keywords for search optimization

### Skill Folder Structure

```
claude-skills-package/
├── package.json
├── README.md
├── LICENSE
└── skills/
    ├── card-news-generator/
    │   ├── SKILL.md
    │   ├── generate_card.py
    │   └── ...
    ├── flutter-init/
    │   ├── skill.md
    │   └── ...
    ├── code-changelog/
    ├── codex/
    ├── codex-claude-loop/
    ├── nextjs15-init/
    ├── prompt-enhancer/
    ├── web-to-markdown/
    └── ...
```

### Copy Skills (Option A only)

```bash
# Copy skills from current my-skills-hub
cp -r ../my-skills-hub/skills ./
```

### Write README.md

```markdown
# @your-org/claude-skills

Custom Claude Code skills collection.

## Installation

```bash
# Install individual skills
npx claude-plugins skills install @your-org/claude-skills/card-news-generator
npx claude-plugins skills install @your-org/claude-skills/flutter-init
```

## Included Skills

- **card-news-generator**: Auto-generate 600x600 Instagram card news
- **flutter-init**: Auto-generate Flutter Clean Architecture projects
- **code-changelog**: Auto-document AI code changes
- **codex**: OpenAI Codex CLI integration
- **nextjs15-init**: Next.js 15 App Router project generation
- Plus 8 more skills

## License

MIT
```

---

## First Deployment

### 1. Validate Package

```bash
# Check package.json syntax
npm pkg fix

# Preview package contents
npm pack --dry-run
```

### 2. Create .npmignore File (Optional)

Exclude unnecessary files:

```bash
cat > .npmignore << 'EOF'
.git
.github
.vscode
.DS_Store
node_modules
*.log
test/
examples/
.env
EOF
```

### 3. NPM Login

```bash
# First time only
npm login

# Verify login
npm whoami
```

### 4. Publish Scoped Package

```bash
# Publish as public package
npm publish --access public
```

**Example Output:**
```
+ @your-org/claude-skills@1.0.0
```

### 5. Verify Deployment

```bash
# Check on NPM website
open https://www.npmjs.com/package/@your-org/claude-skills

# Or test installation directly
npx claude-plugins skills install @your-org/claude-skills/flutter-init
```

---

## Deploying Updates

### 1. Modify Code

Make changes to skills or add new skills.

### 2. Update Version

```bash
# Method 1: Auto-increment version
npm version patch   # 1.0.0 → 1.0.1 (bug fixes)
npm version minor   # 1.0.0 → 1.1.0 (new features)
npm version major   # 1.0.0 → 2.0.0 (breaking changes)

# Method 2: Manually edit package.json
# "version": "1.0.1"
```

**Semantic Versioning Guide:**
- **patch (1.0.x)**: Bug fixes
- **minor (1.x.0)**: New features (backward compatible)
- **major (x.0.0)**: Breaking changes

### 3. Write CHANGELOG.md (Recommended)

```markdown
## [1.1.0] - 2025-01-15

### Added
- card-news-generator-v2: Background image support feature
- landing-page-guide: New skill added

### Changed
- flutter-init: Upgraded to Riverpod 3.0
- code-changelog: Improved dark mode UI

### Fixed
- codex: Fixed session resume settings inheritance bug
```

### 4. Git Commit and Tag

```bash
# Commit changes
git add .
git commit -m "chore: Release version 1.1.0"

# Create Git tag (optional)
git tag -a v1.1.0 -m "Release version 1.1.0"
git push origin main --tags
```

### 5. Republish to NPM

```bash
# Republish
npm publish
```

**Example Output:**
```
+ @your-org/claude-skills@1.1.0
```

### 6. Notify Users of Update

Update README.md with latest version info:

```markdown
## Latest Version

Current version: `1.1.0`

### New Features
- card-news-generator-v2 added
- landing-page-guide added
```

---

## User Installation Guide

### Personal Skill (Global Install)

```bash
# Install individual skills
npx claude-plugins skills install @your-org/claude-skills/card-news-generator

# Install multiple skills
npx claude-plugins skills install @your-org/claude-skills/flutter-init
npx claude-plugins skills install @your-org/claude-skills/codex
npx claude-plugins skills install @your-org/claude-skills/nextjs15-init
```

### Project Skill (Project-Specific Install)

```bash
# From project directory
npx claude-plugins skills install @your-org/claude-skills/flutter-init --project
```

### Installation Locations

- **Personal**: `~/.claude/skills/`
- **Project**: `.claude/skills/`

### Using Skills

```bash
# In Claude Code
card-news-generator
flutter-init
codex-claude-loop
```

### Check Installed Skills

```bash
# In Claude Code
/skills
```

### Update Skills

Users update to latest version by:

```bash
# Reinstall skill (overwrites with latest version)
npx claude-plugins skills install @your-org/claude-skills/card-news-generator
```

---

## Version Management Best Practices

### 1. Use Semantic Versioning

```
major.minor.patch
  │     │     │
  │     │     └─ Bug fixes (1.0.1)
  │     └─────── New features (1.1.0)
  └───────────── Breaking changes (2.0.0)
```

**Examples:**
- `1.0.0` → `1.0.1`: codex skill bug fix
- `1.0.0` → `1.1.0`: landing-page-guide skill added
- `1.0.0` → `2.0.0`: Major skill structure overhaul

### 2. Sync with Git Tags

```bash
# Match package.json version with Git tag
npm version patch -m "chore: Release version %s"

# This command automatically:
# 1. Increments package.json version
# 2. Creates Git commit
# 3. Creates Git tag
```

### 3. Maintain CHANGELOG.md

```markdown
# Changelog

## [Unreleased]
### Added
- Work-in-progress features

## [1.2.0] - 2025-01-15
### Added
- card-news-generator-v2: Background image support
- landing-page-guide: Landing page creation guide

### Changed
- flutter-init: Upgraded to Riverpod 3.0
- code-changelog: Improved dark mode UI

### Fixed
- codex: Fixed session resume settings inheritance bug

## [1.1.0] - 2025-01-10
...
```

### 4. Release Workflow

```bash
# 1. Modify code
# 2. Test changes
# 3. Update CHANGELOG.md
# 4. Increment version and tag
npm version minor -m "chore: Release version %s"

# 5. Push to GitHub
git push origin main --tags

# 6. Publish to NPM
npm publish

# 7. Create GitHub Release (optional)
gh release create v1.2.0 --title "v1.2.0" --notes "$(cat CHANGELOG.md)"
```

---

## Advanced Usage

### Private NPM Package Deployment

```bash
# Organization private package
npm publish --access restricted

# Users install after NPM login
npm login
npx claude-plugins skills install @your-org/claude-skills/flutter-init
```

### Managing as Monorepo

For managing multiple skill collections:

```
my-skills-monorepo/
├── packages/
│   ├── ai-skills/          # @your-org/ai-skills
│   │   └── skills/
│   ├── dev-tools/          # @your-org/dev-tools
│   │   └── skills/
│   └── design-skills/      # @your-org/design-skills
│       └── skills/
└── package.json
```

### Using NPM Scripts

```json
{
  "scripts": {
    "test": "echo 'Run skill tests'",
    "lint": "echo 'Lint skill files'",
    "prepublishOnly": "npm run test && npm run lint",
    "release:patch": "npm version patch && npm publish && git push --tags",
    "release:minor": "npm version minor && npm publish && git push --tags",
    "release:major": "npm version major && npm publish && git push --tags"
  }
}
```

**Usage Example:**
```bash
# Version increment, publish, push tags all at once
npm run release:minor
```

---

## References

- [Claude Code Official Documentation](https://code.claude.com/docs)
- [NPM Scoped Packages](https://docs.npmjs.com/about-scopes)
- [Semantic Versioning](https://semver.org/)
- [Keep a Changelog](https://keepachangelog.com/)
- [NPM Scripts](https://docs.npmjs.com/cli/v9/using-npm/scripts)

---

## FAQ

### Q1: Do I need to create separate packages for each skill?

**A:** No, it's better to include all skills in one package:
- Easier to manage
- Consistent version management
- Users can install individual skills selectively
- `@anthropics/skills` uses this approach

**Example:**
```bash
# Install individual skills from one package
npx claude-plugins skills install @your-org/claude-skills/flutter-init
npx claude-plugins skills install @your-org/claude-skills/card-news-generator
```

### Q2: How to deploy private skills?

**A:** Deploy as NPM private package:
```bash
# Publish
npm publish --access restricted

# Users install after login
npm login
npx claude-plugins skills install @your-org/private-skills/internal-tool
```

**Note:** Private packages require paid NPM account (organization account recommended)

### Q3: How to deploy skill updates?

**A:** Simple 3-step process:
```bash
# 1. Increment version
npm version patch

# 2. Publish
npm publish

# 3. Git push
git push --tags
```

Users reinstall to auto-get latest version:
```bash
npx claude-plugins skills install @your-org/claude-skills/flutter-init
```

### Q4: How to create NPM Organization?

**A:** From NPM website:
1. Login to https://www.npmjs.com
2. Click "Create Organization"
3. Enter organization name (e.g., `your-org`)
4. Set package name to `@your-org/claude-skills`

**Free vs Paid:**
- Free: Public packages only
- Paid ($7/month): Private package support

### Q5: How to test before deployment?

**A:** Local testing method:
```bash
# 1. Create package tarball
npm pack

# 2. Test install with .tgz file
npx claude-plugins skills install ./your-org-claude-skills-1.0.0.tgz/flutter-init

# 3. Publish after verifying it works
npm publish --access public
```

### Q6: How to prevent skill name conflicts?

**A:** Scoped packages (`@your-org/`) automatically separate namespaces.

**Examples:**
- `@anthropics/skills/pptx`
- `@your-org/skills/pptx`
- `@another-org/skills/pptx`

All recognized as different packages with no conflicts!

---

## Quick Start Checklist

1. ✅ Create NPM account and login
2. ✅ Create `package.json` (scoped package name)
3. ✅ Organize skills in `skills/` folder
4. ✅ Write `README.md`
5. ✅ Validate with `npm pack --dry-run`
6. ✅ Deploy with `npm publish --access public`
7. ✅ Test installation
8. ✅ Push code to GitHub

**First Deployment:**
```bash
npm login
npm publish --access public
```

**Update Deployment:**
```bash
npm version patch
npm publish
git push --tags
```
