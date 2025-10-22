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

### Comms & Knowledge

#### Office Communications
**Status**: Live
**URL**: [office.quarterly.systems](https://office.quarterly.systems)

Self-hosted team communication platform that provides secure, private messaging and collaboration.

**Features**:
- Encrypted messaging
- Self-hosted setup
- Collaboration tools
- No vendor lock-in

**Use Cases**:
- Secure team communication
- Project-specific channels
- Internal announcements
- Private conversations

---

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

#### GitHub Graph Spider
**Status**: Beta (Experimental)
**URL**: [graph.quarterly.systems](https://graph.quarterly.systems) *(deployment pending)*

Social graph analyzer for discovering influential developers in your GitHub network.

**Features**:
- BFS spider for follower/following relationships
- "Hidden influencer" discovery algorithm
- Recommendations based on mutual connections
- Background processing via cron (every 5 minutes)
- D1 SQLite database
- GitHub API integration (5,000 requests/hour)

**Technology Stack**:
- Vanilla HTML/CSS/JS frontend
- Cloudflare Workers backend
- D1 database (SQLite)

**Use Cases**:
- Network analysis
- Developer discovery
- Collaboration opportunities
- Community insights

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
