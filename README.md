# My Skills Hub

A collection of custom Claude Code skills to enhance development productivity.

---

<div align="center">

### 🎴 Learn Programming with Card-Based Platform

[![CodeDeck](https://img.shields.io/badge/CodeDeck-Learn_Programming_with_Cards-blue?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTUgNEgxOUMyMC4xIDQgMjEgNC45IDIxIDZWMThDMjEgMTkuMSAyMC4xIDIwIDE5IDIwSDVDMy45IDIwIDMgMTkuMSAzIDE4VjZDMyA0LjkgMy45IDQgNSA0WiIgZmlsbD0id2hpdGUiLz4KPC9zdmc+Cg==)](https://www.codedeck.kr)

Learn programming languages and frameworks in **card news format**!
`Flutter` `React` `TypeScript` `JavaScript` `Python` `Dart`

**👉 [Visit CodeDeck](https://www.codedeck.kr)**

</div>

---

## Quick Installation

| Skill Name | Description | Marketplace Install Command |
|----------|---------|---------------|
| **Flutter Init** | Auto-generate Flutter projects with Clean Architecture | `/plugin marketplace install suji-father-marketplace@flutter-init` |
| **Next.js 15 Init** | Auto-generate Next.js 15 projects with App Router | `/plugin marketplace install suji-father-marketplace@nextjs15-init` |
| **Code Changelog** | Auto-document AI code changes and view in browser | `/plugin marketplace install suji-father-marketplace@code-changelog` |
| **Codex** | OpenAI Codex CLI for code analysis and refactoring | `/plugin marketplace install suji-father-marketplace@codex` |
| **Codex-Claude Loop** | Dual-AI engineering loop for highest quality code | `/plugin marketplace install suji-father-marketplace@codex-claude-loop` |
| **Meta Prompt Generator** | Auto-generate structured custom slash commands | `/plugin marketplace install suji-father-marketplace@meta-prompt-generator` |
| **Prompt Enhancer** | Transform simple requests into detailed requirements | `/plugin marketplace install suji-father-marketplace@prompt-enhancer` |
| **Web to Markdown** | Convert web pages to markdown (normal/AI-optimized/dual modes) | `/plugin marketplace install suji-father-marketplace@web-to-markdown` |
| **Card News Generator** | Auto-generate 600x600 Instagram card news series | `/plugin marketplace install suji-father-marketplace@card-news-generator` |
| **Card News Generator V2** | Card news generator with background image support | `/plugin marketplace install suji-father-marketplace@card-news-generator-v2` |
| **Landing Page Guide** | High-conversion landing page creation guide | `/plugin marketplace install suji-father-marketplace@landing-page-guide` |

### Add Marketplace

```bash
/plugin marketplace add bear2u/claude-plugins
```

## Skills Overview

### 1. [Code Changelog](./skills/code-changelog/)
Auto-documents all AI-generated code changes and provides real-time web browser viewing.

**Key Features:**
- Automatic markdown documentation
- HTML viewer (no installation, Python server)
- Dark mode UI (GitHub style)
- Real-time server (http://localhost:4000)

**Use Cases:**
- Auto-generate code review documentation
- Track change history
- Share changes with team members

### 2. [Meta Prompt Generator](./skills/meta-prompt-generator/)
Automatically generates structured custom slash commands with parallel processing from simple descriptions.

**Key Features:**
- Intelligent knowledge gathering (web search)
- Step-based workflow design
- Comprehensive test generation
- Parallel processing optimization

**Use Cases:**
- Automate complex project workflows
- Create reusable slash commands
- Write systematic test suites

### 3. [Prompt Enhancer](./skills/prompt-enhancer/)
Analyzes project context to transform simple development requests into clear, detailed requirements.

**Key Features:**
- Auto-analyze project structure
- Recognize existing patterns
- Generate structured requirements
- Framework-specific optimization

**Use Cases:**
- "Create login feature" → detailed implementation requirements
- Clean Architecture-based design proposals
- Auto-apply project conventions

**Supported Stacks:**
- Flutter (Clean Architecture, Riverpod)
- Next.js/React (App Router, Zustand)
- Python (Django, FastAPI)

### 4. [Flutter Init](./skills/flutter-init/)
Auto-generates domain-based Flutter projects with Clean Architecture.

**Key Features:**
- Domain selection (Todo/Habit/Note/Expense/Custom)
- Stack presets (Minimal/Essential/Full Stack/Custom)
- Auto-generate Clean Architecture
- Riverpod 3.0, Drift, Freezed setup

**Tech Stack:**
- Riverpod 3.x (state management)
- Drift (local database)
- Freezed (immutable models)
- Easy Localization (i18n)
- FluentUI Icons

**Use Cases:**
- Quick start new Flutter apps
- Clean Architecture boilerplate
- Domain-driven design

### 5. [Next.js 15 Init](./skills/nextjs15-init/)
Auto-generates domain-based Next.js 15 projects with App Router.

**Key Features:**
- Domain selection (Todo/Blog/Dashboard/E-commerce/Custom)
- Stack presets (Minimal/Essential/Full Stack/Custom)
- App Router-based structure
- TypeScript Strict Mode

**Tech Stack:**
- Next.js 15 (App Router)
- ShadCN/ui (UI components)
- Zustand (client state)
- Tanstack Query (server state)
- Drizzle ORM (TypeScript ORM)
- Better Auth (authentication)

**Use Cases:**
- Quick start new Next.js apps
- Type-safe full-stack apps
- Domain-driven design

### 6. [Codex](./skills/codex/)
Uses OpenAI Codex CLI for code analysis, refactoring, and automated editing.

**Key Features:**
- Interactive model and reasoning level selection (gpt-5, gpt-5-codex)
- Sandbox modes (read-only, workspace-write, danger-full-access)
- Session resume (codex exec resume --last)
- Automated code editing (--full-auto)

**Use Cases:**
- Code review and analysis
- Large-scale refactoring automation
- Codebase-wide modifications
- Continue previous sessions

**Sandbox Modes:**
- `read-only`: Code analysis only (read-only)
- `workspace-write`: Local file modifications
- `danger-full-access`: Full access including network

### 6-1. [Codex-Claude Loop](./skills/codex-claude-loop/) 🔄
Dual-AI engineering loop combining Claude Code and Codex for optimal code quality.

**Core Workflow:**
- **Claude (Plan + Implement)** → **Codex (Validate)** → **Feedback** → **Claude (Fix)** → **Codex (Re-validate)** → **Repeat**
- Claude handles all code writing, Codex handles all validation
- Self-correcting system for high-quality engineering

**Key Features:**
- Planning Phase: Claude establishes architecture and implementation plan
- Validation Phase: Codex reviews plan for logic errors and security vulnerabilities
- Implementation Phase: Claude writes code using Edit/Write tools
- Code Review: Codex validates implementation for bugs, performance, security
- Fix Application: Claude fixes code based on Codex feedback
- Re-validation: Codex confirms fixes

**When to Use:**
- ✅ Complex feature development (multiple steps)
- ✅ Security/performance critical tasks
- ✅ Large-scale refactoring
- ✅ When high code quality is required
- ❌ Simple one-off fixes (overkill)
- ❌ Prototype/experimental code (overkill)

**Practical Example:**
```bash
# 1. Claude creates OAuth 2.0 login plan
# 2. Validate plan with Codex
echo "Review this plan..." | codex exec -m gpt-5-codex --config model_reasoning_effort="high" --sandbox read-only

# 3. Claude implements with validated plan (Edit/Write tools)
# 4. Codex reviews implementation
echo "Review implementation..." | codex exec --sandbox read-only

# 5. Claude applies feedback fixes
# 6. Codex re-validates
echo "Verify fixes..." | codex exec resume --last
```

**Role Division:**
- **Claude**: All code writing and modification
- **Codex**: All validation and review

**Command Reference:**
- Plan validation: `codex exec -m gpt-5-codex --sandbox read-only`
- Code review: `codex exec --sandbox read-only`
- Re-validation: `codex exec resume --last` (auto-inherits settings)

**Model Selection Guide:**
- `gpt-5`: Fast general tasks
- `gpt-5-codex`: Complex code analysis (recommended)

**Reasoning Effort:**
- `low`: Simple validation
- `medium`: General tasks (recommended)
- `high`: Security/critical logic

### 7. [Landing Page Guide](./skills/landing-page-guide/)
Comprehensive guide for creating high-conversion landing pages with Next.js and React.

**Key Features:**
- DESIGNNAS 11 essential elements framework
- ShadCN UI component integration
- SEO optimization and accessibility standards
- Responsive design and performance optimization

**11 Essential Elements:**
1. Keyword-rich URL
2. Company logo (top left)
3. SEO-optimized title and subtitle
4. Primary CTA (hero section)
5. Social proof (reviews, statistics)
6. Images or videos
7. Key benefits/features (3-6 items)
8. Customer testimonials (4-6 items)
9. FAQ section (5-10 questions)
10. Final CTA (bottom)
11. Contact info and legal pages

**Tech Stack:**
- Next.js 14+ (App Router)
- TypeScript
- Tailwind CSS
- ShadCN UI

**Use Cases:**
- Marketing landing pages
- Product introduction pages
- Conversion-optimized promotion pages
- SaaS/E-commerce/Service/Event landing pages

### 8. [Card News Generator](./skills/card-news-generator/)
Auto-generates 600x600 Instagram-style card news series.

**Key Features:**
- Input topic and colors to auto-generate
- Auto-create 5-7 card series
- Auto text wrapping and layout
- RGB to Hex color conversion
- Single card/multi-card modes

**Canvas Specs:**
- Size: 600x600 pixels (Instagram optimized)
- Auto text line breaks
- Number badge, title, content hierarchy
- Various color presets

**Recommended Colors:**
- Beige: `245,243,238`
- Pink: `255,229,229`
- Mint: `224,244,241`
- Lavender: `232,224,245`
- Peach: `255,232,214`
- Sky Blue: `227,242,253`

**Use Cases:**
- Social media card news
- Instagram content series
- Information delivery card images
- Educational/marketing content

### 9. [Card News Generator V2](./skills/card-news-generator-v2/) 🆕
Enhanced card news generator with background image support.

**V2 New Features:**
- ✨ **Background Image Support**: Auto-apply folder images as backgrounds
- ✨ **Cafe24Ssurround Font**: Bundled font, no installation needed
- ✨ **Translucent Box + Border**: Rounded box with white border for text area
- ✨ **Compact Design**: Center-aligned box close to square shape
- ✨ **Overlay Control**: Dark overlay for text readability (0.0-1.0)
- ✨ **Auto Text Color**: Auto-switch to white when using background images

**Technical Specs:**
- Auto-crop and resize background images (600x600)
- Supported formats: JPG, JPEG, PNG, WebP, BMP
- macOS/Linux auto font detection
- Text box width: 65% of canvas (margins on both sides)

**Usage Example:**
```bash
python auto_generator.py \
  --topic "Seoul Real Estate" \
  --image-folder ./my-images \
  --overlay-opacity 0.6 \
  --output-dir ./output
```

**Use Cases:**
- Card news with real photos as backgrounds
- Visual-important content (travel, real estate, food)
- Professional and polished design needs
- Strengthen brand identity with background images

### 10. [Web to Markdown](./skills/web-to-markdown/) 🌐
Converts web page URLs to markdown format and saves them.

**Key Features:**
- 3 conversion modes supported
  - **Normal Mode**: Clean markdown conversion
  - **AI-Optimized Mode**: Structured format for AI context (YAML frontmatter, core summary)
  - **Dual Mode**: Generate both original + AI-optimized versions simultaneously ⭐
- **Dynamic Content Handling ⭐ NEW**
  - Auto-detect JavaScript-rendered pages failed by WebFetch
  - Run browser with Playwright to fetch dynamic content
  - Supports MCP Playwright or Node Playwright
- Batch convert multiple URLs
- Extract specific sections only
- Customize markdown formatting
- WebFetch auto-caching (15 minutes)

**Conversion Modes:**
```
# Normal mode
Convert this webpage to markdown

# AI-optimized mode
Convert for AI to read easily
Convert to be good for context

# Dual mode (recommended)
Create both original and AI-optimized versions
```

**AI-Optimized Mode Features:**
- YAML frontmatter (title, URL, topic, core summary, etc.)
- Structured sections (core summary, main content, insights, practical applications)
- 30-50% token reduction
- AI can grasp core in under 3 seconds

**Filename Convention:**
- Original: `article.md`
- AI-optimized: `article.context.md`

**Use Cases:**
- Archive technical documentation
- Backup blog posts
- Build learning materials
- Prepare data for RAG systems
- Generate AI agent context materials

**Usage Examples:**
```
# Dual mode
User: https://docs.python.org/3/tutorial Create both original and AI-optimized versions

Claude: Converting in dual mode.
- python-tutorial.md (original - human-readable)
- python-tutorial.context.md (AI-optimized - for context)

# Dynamic content (NEW)
User: https://www.codedeck.kr/card-news/xxx Convert to markdown

Claude: [WebFetch attempt]
        ⚠️ Content is mostly empty. Looks like a JavaScript-rendered page.
        Retry with Playwright?

User: Yes

Claude: ⏳ Loading page with Playwright...
        ✅ JavaScript rendering complete
        ✅ Markdown conversion complete (1,442 lines)
```

## How to Use Skills

### Method 1: Install via Marketplace (Recommended)

#### 1. Add Marketplace

```bash
/plugin marketplace add bear2u/claude-plugins
```

#### 2. Check Available Plugins

```bash
/plugin marketplace list
```

#### 3. Install Desired Plugin

```bash
# Flutter project initialization
/plugin marketplace install suji-father-marketplace@flutter-init

# Next.js 15 project initialization
/plugin marketplace install suji-father-marketplace@nextjs15-init

# Auto-document code changes
/plugin marketplace install suji-father-marketplace@code-changelog

# Codex CLI integration
/plugin marketplace install suji-father-marketplace@codex

# Codex-Claude dual AI loop
/plugin marketplace install suji-father-marketplace@codex-claude-loop

# Meta prompt generator
/plugin marketplace install suji-father-marketplace@meta-prompt-generator

# Prompt enhancer
/plugin marketplace install suji-father-marketplace@prompt-enhancer

# Web page markdown conversion
/plugin marketplace install suji-father-marketplace@web-to-markdown

# Card news generator
/plugin marketplace install suji-father-marketplace@card-news-generator

# Card news generator V2 (background image support)
/plugin marketplace install suji-father-marketplace@card-news-generator-v2

# Landing page guide
/plugin marketplace install suji-father-marketplace@landing-page-guide
```

#### 4. Check Installed Plugins

```bash
/plugin list
```

#### 5. Update Plugins

```bash
# Update specific plugin
/plugin update suji-father-marketplace@flutter-init

# Or update all plugins
/plugin update
```

#### 6. Remove Plugins

```bash
# Remove specific plugin
/plugin remove flutter-init

# Or remove entire marketplace
/plugin marketplace remove suji-father-marketplace
```

### Method 2: Manual Installation

1. Copy skills to Claude Code skills directory:

```bash
# Install as user skills (global)
cp -r skills/* ~/.claude/skills/

# Or install as project skills (project-specific)
cp -r skills/* ./.claude/skills/
```

2. Check skills in Claude Code:

```
/skills
```

### Running Skills

Each skill can be run by its skill name:

```
code-changelog
meta-prompt-generator
prompt-enhancer
flutter-init
nextjs15-init
codex
codex-claude-loop          # Claude + Codex dual AI loop
landing-page-guide
card-news-generator        # Basic solid background cards
card-news-generator (V2)   # Background image support (same skill, advanced features)
web-to-markdown            # Convert web pages to markdown
```

## Folder Structure

```
my-skills-hub/
├── skills/
│   ├── code-changelog/          # Auto-document code changes
│   │   ├── skill.md             # Skill definition
│   │   └── ...                  # Skill files
│   ├── meta-prompt-generator/   # Meta prompt generator
│   │   ├── skill.md
│   │   └── ...
│   ├── prompt-enhancer/         # Prompt enhancer
│   │   ├── skill.md
│   │   └── ...
│   ├── flutter-init/            # Flutter project generator
│   │   ├── skill.md
│   │   └── ...
│   ├── nextjs15-init/           # Next.js 15 project generator
│   │   ├── skill.md
│   │   └── ...
│   ├── codex/                   # Codex CLI code review/analysis
│   │   └── skill.md
│   ├── codex-claude-loop/       # Claude + Codex dual AI engineering loop
│   │   ├── SKILL.md
│   │   └── README.md
│   ├── landing-page-guide/      # Landing page creation guide
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── 11-essential-elements.md
│   │       └── component-examples.md
│   ├── card-news-generator/     # Auto card news generation
│   │   ├── SKILL.md
│   │   └── ...
│   └── web-to-markdown/         # Web page markdown conversion
│       ├── SKILL.md
│       └── ...
└── README.md                     # This file
```

## Skill Details

See each skill folder's `skill.md` file for detailed information:

- [Code Changelog Details](./skills/code-changelog/skill.md)
- [Meta Prompt Generator Details](./skills/meta-prompt-generator/skill.md)
- [Prompt Enhancer Details](./skills/prompt-enhancer/skill.md)
- [Flutter Init Details](./skills/flutter-init/skill.md)
- [Next.js 15 Init Details](./skills/nextjs15-init/skill.md)
- [Codex Details](./skills/codex/skill.md)
- [Codex-Claude Loop Details](./skills/codex-claude-loop/SKILL.md)
- [Codex-Claude Loop Usage](./skills/codex-claude-loop/README.md)
- [Landing Page Guide Details](./skills/landing-page-guide/SKILL.md)
- [Card News Generator Details](./skills/card-news-generator/SKILL.md)
- [Card News Generator V2 Details](./skills/card-news-generator/V2_FEATURES.md)
- [Web to Markdown Details](./.claude/skills/web-to-markdown/SKILL.md)

## Contributing

To add new skills or improve existing ones:

1. Create new skill directory in `skills/`
2. Write `skill.md` file (skill metadata and description)
3. Add necessary files
4. Add skill info to README.md

## License

MIT License

## Changelog

### [1.5.0] - 2025-11-07

#### Added
- **web-to-markdown**: Dynamic content handling feature ⭐
  - Automatic Playwright fallback when WebFetch fails
  - MCP Playwright and Node Playwright support
  - Auto-detect JavaScript-rendered pages
  - User confirmation process with AskUserQuestion
- **SKILL_DISTRIBUTION_GUIDE.md**: Complete guide for distributing skills as NPM packages
  - Create NPM package structure
  - First deployment and update methods
  - Version management best practices
  - FAQ and practical examples

#### Changed
- **README.md**: Added dynamic content handling feature to web-to-markdown description
- **README.md**: Added dynamic content usage examples

#### Technical Details
- Chromium browser automation via Playwright
- HTML parsing and markdown conversion via Cheerio
- Perfect support for SPA pages (React, Vue, Next.js)

### [1.4.0] - 2025-10-29

#### Added
- **card-news-generator-v2**: Background image support
- **landing-page-guide**: High-conversion landing page creation guide
- **midjourney-cardnews-bg**: Midjourney prompt generation skill

### [1.3.0] - 2025-10-27

#### Added
- **codex-claude-cursor-loop**: Claude + Codex + Cursor triple AI loop
- **codex-claude-loop**: Claude + Codex dual AI engineering loop

### [1.2.0] - 2025-10-25

#### Added
- **web-to-markdown**: Web page markdown conversion skill
  - Normal mode
  - AI-optimized mode
  - Dual mode
- **card-news-generator-v2**: Background image support version

### [1.1.0] - 2025-10-23

#### Added
- **flutter-init**: Flutter Clean Architecture project generation
- **nextjs15-init**: Next.js 15 App Router project generation
- **code-changelog**: AI code change auto-documentation
- **meta-prompt-generator**: Structured custom slash command generation
- **prompt-enhancer**: Project context-based prompt enhancement

### [1.0.0] - 2025-10-20

#### Added
- Initial release
- **card-news-generator**: Instagram card news generation
- **codex**: OpenAI Codex CLI integration
- Marketplace setup and deployment

---

## References

These skills were created with reference to Claude Code official documentation:
- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [Keep a Changelog](https://keepachangelog.com/)
