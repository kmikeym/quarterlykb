---
title: "Applications"
date: 2025-09-30
tags: []
publish: true
---

# Applications

[[Company/KmikeyM|Quarterly Systems]] offers an integrated suite of applications designed to support modern business operations, team collaboration, and personal productivity. Each application serves a specific purpose while integrating seamlessly with the broader Quarterly Systems platform.

**Explore all applications**: [quarterly.systems/apps](https://quarterly.systems/apps)

## Live Applications

### Knowledge

#### Knowledge Base
**Status**: Beta
**URL**: [base.quarterly.systems](https://base.quarterly.systems)

Centralized documentation and best practices repository for organizational knowledge management built on Quartz v4.

**Features**:
- Structured documentation
- Version control (git-based)
- Semantic search (FlexSearch)
- Collaborative editing
- Digital garden with Obsidian-style linking
- Graph visualization of page connections
- Auto-deployment via GitHub Actions

**Technology Stack**:
- Quartz v4
- TypeScript
- Preact

**Use Cases**:
- Company documentation
- Technical knowledge sharing
- Process documentation
- Team onboarding resources

---

#### Documentation
**Status**: Live
**URL**: [docs.quarterly.systems](https://docs.quarterly.systems)

Technical documentation hub for K5M projects and tools, focusing on building efficient, local-first applications.

**Features**:
- Project documentation (Water Tracker, etc.)
- Quick start guides
- API and CLI references
- Dark/light theme support
- Built with Starlight

**Philosophy**:
- **Privacy**: Data remains on user devices
- **Performance**: Lightweight, fast applications
- **Simplicity**: User-friendly tools
- **Transparency**: Open source, community-driven

**Use Cases**:
- Developer documentation for K5M projects
- Local-first application guides
- CLI tool references
- Community-contributed projects

---

### Community

#### Live Chat
**Status**: Live
**URL**: [office.quarterly.systems](https://office.quarterly.systems)

Real-time team communication platform that provides secure, private messaging and collaboration.

**Features**:
- Encrypted messaging
- Self-hosted setup
- Collaboration tools
- No vendor lock-in

**Use Cases**:
- Team communication
- Project-specific channels
- Internal announcements
- Community conversations

---

#### Branch
**Status**: Live
**URL**: [branch.quarterly.systems](https://branch.quarterly.systems)
**Source**: [github.com/kmikeym/branch](https://github.com/kmikeym/branch)

GitHub social graph analyzer for discovering influential developers. Branch helps you find "hidden influencers" in your network through BFS spider analysis of follower/following relationships.

**Philosophy**:
"I wasn't looking for a network map. I was looking for friends." Branch is about building **clubware** — small, weird software for ourselves and our friends. Apps that don't need to scale to be successful.

**Features**:
- BFS spider for GitHub follower/following relationships
- Discover "hidden influencers" in your network
- Recommendations based on mutual connection counts
- Background processing via cron (every 5 minutes)
- Simple, focused interface
- Railway deployment with auto-deploy

**Technology Stack**:
- Railway-deployed application
- GitHub API integration
- Auto-deploy via GitHub integration
- Respects GitHub API limits (5,000/hour authenticated)

**Use Cases**:
- Finding collaborators
- Discovering friend-focused developers
- Building your coding community
- Network exploration for small projects

**Related**: See [[Insights#Branch: Building Clubware, Not Software|Branch video]] for the story behind this project.

---

### Status & Analytics

#### Operational Status
**Status**: Beta
**URL**: [quarterly.systems/status](https://quarterly.systems/status)

Real-time operational transparency dashboard providing live activity feeds, location tracking, and multi-source data integration.

**Features**:
- Activity aggregation
- Geographic tracking
- Multi-source data integration (GitHub, RSS, location)
- Transparency tools
- 30-minute cache TTL
- Cron refresh every 10 minutes
- Immutable activity history

**API**: [status-api.quarterly.systems](https://status-api.quarterly.systems)

**Technology Stack**:
- Cloudflare Workers
- KV storage

**Use Cases**:
- Team activity transparency
- Development progress tracking
- Public status updates
- Historical activity records

---

#### [[Applications/The Body Electric|The Body Electric]]
**Status**: Live
**URL**: [body.quarterly.systems](https://body.quarterly.systems)

Weight tracking application with trend analysis using EWMA (Exponentially Weighted Moving Average) methodology and calorie insights.

**Features**:
- Trend smoothing (EWMA)
- 7-day slope calculations
- Local-first storage (Fireproof/IndexedDB)
- Interactive charts (Recharts)
- Calorie deficit/surplus tracking

**Technology Stack**:
- React 18 & TypeScript
- Vite build system
- Tailwind CSS
- Fireproof database

**Use Cases**:
- Personal health tracking
- Weight trend analysis
- Fitness goal monitoring
- Data-driven wellness

→ **[View detailed documentation and roadmap](Applications/The%20Body%20Electric.md)**

---

### Client Solutions

#### [[Applications/BorelCorp.com|BorelCorp.com]]
**Status**: Live
**URL**: [borelcorp.com](https://borelcorp.com)
**Client**: Kathryn Borel

Corporate website for BorelCorp International, a global trading house operating at the intersection of commerce and culture since 1987.

**Key Features**:
- Classic corporate web design with retro aesthetic
- Product showcase (ResMod, TAROT Project)
- Company divisions (Conceptual Logistics, Applied Trade Operations)
- News and announcements section
- Wholesale partnership inquiries

**Design Approach**:
- Authentic 1990s corporate website styling
- CSS-only layout, no JavaScript dependency
- Responsive mobile design
- Professional blue navigation scheme
- Classic web typography and spacing

**Services Highlighted**:
- International trade and logistics (47 countries)
- Specialty goods import/export
- TAROT Project for forecasting and planning
- Conceptual logistics solutions
- Applied trade operations

**Use Cases**:
- Corporate web presence
- Product and service showcase
- Client partnership inquiries
- Company information and history

→ **[View detailed project documentation](Applications/BorelCorp.com.md)**

---

#### Jump Higher
**Status**: Live
**URL**: [jumphigher.horse](https://jumphigher.horse)

Motivational audio training landing page featuring the "Inner Rider" methodology adapted from horse training techniques.

**Key Features**:
- Free MP3 download (jump-higher-training.mp3)
- Email capture via ConvertKit integration
- Tony Robbins-inspired design (navy/gold palette)
- Pure HTML/CSS/JavaScript (no build process)

**Design Approach**:
- Motivational training focus
- Single-page landing design
- ConvertKit form integration (Form UID: 98bfe26c53)
- Cloudflare Pages deployment

**Use Cases**:
- Motivational audio training
- Email list building
- Personal development resources
- Training methodology showcase

---

#### OKR.surf
**Status**: Live
**URL**: [okr.surf](https://okr.surf)

Professional game-board-inspired OKR tracking for ~8 person teams with spaceship command center aesthetic.

**Key Features**:
- Real-time collaborative OKR planning and tracking
- Three-phase workflow: Reflection → Creation → Tracking
- Spaceship command center UI (BSG/The Expanse inspired)
- InstantDB for real-time sync with optimistic updates
- Cloudflare Access protected

**Technology Stack**:
- Next.js 16 with React 19
- InstantDB for realtime collaboration
- Tailwind CSS 4
- Bun runtime
- TypeScript

**Use Cases**:
- Team OKR planning and tracking
- Quarterly goal setting
- Progress visualization
- Collaborative strategic planning

---

## Experimental Projects

### Quarterly Labs

**Exploring new technologies, creative ideas, and future features.**

#### VibeCode Platform
**Status**: Beta (Experimental)
**URL**: [vibecode.quarterly.systems](https://vibecode.quarterly.systems)

Rapid application development platform that transforms ideas into functional systems. No-code/low-code platform forked from vibes.diy.

**Features**:
- No-code/low-code development
- Real-time collaboration
- Enterprise security
- Scalable infrastructure

**Technology Stack**:
- React & TypeScript
- Fireproof database
- pnpm monorepo
- Strict TypeScript with no `any` types

**Use Cases**:
- Rapid prototyping
- Internal tools development
- Customer-facing applications
- Data-driven dashboards

---

#### Vibe News
**Status**: Live (Experimental)
**URL**: [news.quarterly.systems](https://news.quarterly.systems)

AI coding news aggregator with team collaboration features. FETCH-powered dashboard for staying current with development trends.

**Features**:
- Auto-aggregation from HN, Dev.to, RSS feeds
- Shared stars, mags, and trash features
- Team-wide collaborative state
- No authentication required
- Refresh every 30 minutes
- Neon PostgreSQL backend

**Technology Stack**:
- Vanilla HTML/CSS/JS frontend
- Cloudflare Workers backend
- Deployed on Cloudflare Pages

**Use Cases**:
- Team news curation
- Development trend tracking
- Collaborative content discovery
- Technical learning resources

---

#### InstantDemo
**Status**: Research (Internal)
**URL**: Not publicly deployed

Realtime database prototypes built with InstantDB and Next.js 15 for exploring real-time collaboration patterns.

**Technology Stack**:
- Next.js 15 with React 19
- InstantDB for realtime data
- Tailwind CSS 4
- TypeScript

**Projects**:
- `demotime/` - Collaborative todo application
- `demotime2/` - Extended InstantDB demos

**Use Cases**:
- Real-time collaboration prototypes
- InstantDB pattern exploration
- Next.js 15 experimentation

---

#### K5M Dashboard Experiments
**Status**: Experimental
**URL**: [quarterly.systems/labs/k5m](https://quarterly.systems/labs/k5m)

Animation experiments, interactive timelines, and dashboard prototypes exploring creative interfaces and interactions.

---

#### Larga
**Status**: MVP (Development)
**URL**: Not publicly deployed
**Platform**: Railway (planned)

Story Development Tracker for screenwriters tracking document evolution over years.

**Features**:
- Multi-format document upload (.docx, .pdf, .rtf)
- Story Grid visualization tracking character/theme evolution
- AI-powered document analysis (OpenRouter GPT-4o)
- Draft comparison tools
- Multi-project support with per-project settings
- Designed for 150+ documents over years

**Technology Stack**:
- Node.js & Express
- Mammoth.js for document processing
- OpenRouter API integration
- Railway deployment

**Use Cases**:
- Screenplay development tracking
- Character arc visualization
- Theme evolution analysis
- Multi-draft comparison
- Long-term creative project management

---

#### VoteWar
**Status**: Development Phase
**URL**: [votewar.quarterly.systems](https://votewar.quarterly.systems) (planned)

Experimental governance game where everything is fungible - buy/sell shares, spend turns, vote on the game rules themselves.

**Features**:
- Real-time multiplayer gameplay
- Buy/sell shares in game mechanics
- Vote on rule changes
- Immutable transaction ledger
- InstantDB for real-time sync

**Technology Stack**:
- Next.js 15 with React 18
- InstantDB for multiplayer state
- Bun runtime
- Tailwind CSS 4
- TypeScript

**Design Philosophy**:
- Emergent gameplay through player governance
- Economic simulation meets democracy
- Transparent rule-making process
- Community-driven game evolution

**Use Cases**:
- Governance experimentation
- Economic simulation games
- Community decision-making exploration
- Real-time multiplayer experiences

---

#### Water Tracker
**Status**: Personal Tool
**URL**: Local-only (no deployment)

Local-first water intake tracker with web, desktop, and CLI interfaces.

**Features**:
- Daily water intake tracking with progress indicators
- 14-day streak calendar
- Adjustable daily goals
- Desktop app (Electron) shares data with web app
- Separate CLI data store in `~/.water-tracker/`
- localStorage persistence

**Technology Stack**:
- Bun runtime
- TypeScript
- Vanilla HTML/CSS/JS
- Electron for desktop
- CLI for command-line tracking

**Commands**:
- `./water add 16` - Add 16oz of water
- `./water status` - Check progress
- `./water history` - View history

**Use Cases**:
- Personal hydration tracking
- Daily health monitoring
- Multi-device water logging
- Command-line wellness tools

---

## Future Roadmap

- **AI Decision Engine** (Research Phase)
- **Predictive Analytics Suite** (Planned Q3 2025)
- **Autonomous Workflow Engine** (Concept Stage)

---

## Support & Documentation

For detailed documentation on any application, visit the [[index|Knowledge Base homepage]] or explore specific application pages.

For questions or support, refer to project-specific repositories or contact the development team through [[Company/KmikeyM|KmikeyM]].

---

## Related Pages

- [[Company/KmikeyM|Company Overview]] - About the parent company
- [[Insights]] - Videos and tutorials about building with these tools
- [[Operational]] - Technical infrastructure and deployment details
