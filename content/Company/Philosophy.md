---
title: "Philosophy"
date: 2025-11-05
tags: [company, philosophy, vibe-coding, clubware]
publish: true
---

# Company Philosophy

Quarterly Systems is built on a foundation of principles that prioritize people over scale, creativity over convention, and ownership over dependency. Our approach to building software reflects a belief that the best tools are made for specific communities, not mass markets.

## Core Principles

### Vibe Coding

**Vibe coding** is about building software that feels right, not just software that works. It's an approach that values:

- **Intuition over process** - Trust your instincts about what users need
- **Speed over perfection** - Ship quickly, iterate based on real feedback
- **Joy over optimization** - Build things that are fun to use and fun to make
- **Experimentation over planning** - Try ideas in production, learn from users

Vibe coding doesn't mean sloppy coding. It means prioritizing the human experience of both building and using software over rigid methodologies and premature optimization.

**In practice:**
- [[Applications/OKR-surf|OKR.surf]] has a spaceship command center aesthetic because work should feel epic
- [[Applications#Vibe News|Vibe News]] uses collaborative curation because discovery should be social
- [[Applications#Branch|Branch]] focuses on finding friends, not building networks

---

### Clubware, Not Software

From [[Insights#Branch: Building Clubware, Not Software|Branch]]: *"I wasn't looking for a network map. I was looking for friends."*

**Clubware** is software built for ourselves and our friends. Apps that don't need to scale to be successful.

**Characteristics of clubware:**
- **Small by design** - Built for ~8-50 people, not millions
- **Weird on purpose** - Embraces unconventional features and interfaces
- **Community-first** - Serves specific groups with specific needs
- **No growth pressure** - Success isn't measured in user counts
- **Personal connection** - You know who you're building for

**Examples:**
- [[Applications/OKR-surf|OKR.surf]] is designed for ~8 person teams, not enterprises
- [[Applications/BorelCorp.com|BorelCorp]] is built specifically for Kathryn Borel
- [[Applications#Water Tracker|Water Tracker]] is a personal tool with no deployment

This philosophy draws inspiration from:
- **[[Home-Cooked Software and Barefoot Developers]]** - Maggie Appleton's vision of software made by and for small communities
- **[[Clubware]]** - Robin Sloan's concept of software for friends
- **[[What the world needs now is groupcore]]** - Small-group software that strengthens communities

---

### Local-First Architecture

Quarterly Systems prioritizes **local-first** design patterns where data lives on user devices, not in corporate clouds.

**Core tenets:**
- **Privacy by default** - Data stays on your device unless you choose to sync
- **Works offline** - Core functionality doesn't require internet
- **User ownership** - You control your data, not us
- **Fast by nature** - Local operations are instant
- **Sync when needed** - Collaboration happens through peer-to-peer or minimal servers

**Technology choices:**
- **Fireproof** - Used in [[Applications/The Body Electric|The Body Electric]] for local-first weight tracking
- **InstantDB** - Powers real-time collaboration in [[Applications/OKR-surf|OKR.surf]] and VoteWar
- **localStorage** - Simple persistence in [[Applications#Water Tracker|Water Tracker]]
- **IndexedDB** - Browser-based storage for offline-capable apps

**Benefits:**
- Users aren't locked into our services
- Privacy is architectural, not policy
- Apps work anywhere, anytime
- No vendor dependency for critical data

See [[Development/Tech-Stack|Tech Stack]] for detailed implementation patterns.

---

### Business-Grade Vibe Coding

While we embrace experimentation and speed, we maintain professional standards where it matters:

**Professional foundations:**
- **TypeScript** - Type safety prevents runtime errors
- **Real-time collaboration** - InstantDB enables true multiplayer experiences
- **Automated deployment** - GitHub Actions, Cloudflare Pages, Railway
- **Observability** - Umami analytics, worker logs, status monitoring
- **Security** - Cloudflare Access, encrypted messaging, secure-by-default patterns

**The balance:**
- Move fast, but write tests for critical paths
- Ship experiments, but monitor production carefully
- Build for friends, but respect their time and data
- Embrace weird UIs, but make them accessible

---

## Design Philosophy

### Aesthetic Coherence

Every application should have a clear visual identity that matches its purpose:

- **OKR.surf** - Spaceship command center (BSG/The Expanse aesthetic)
- **Jump Higher** - Tony Robbins-inspired navy/gold motivational design
- **The Body Electric** - Clean, data-focused health tracking
- **BorelCorp** - Authentic 1990s corporate web styling

Design is not decoration—it communicates what the tool is for and how it should feel to use.

---

### Transparent Operations

We build in public and operate transparently:

- **[[Applications#Operational Status|Status Dashboard]]** - Real-time activity feeds and location tracking
- **Open source templates** - [[Applications#K5M Obsidian Template|Obsidian templates]] shared publicly
- **[[Insights]]** - Video documentation of building process and lessons learned
- **This Knowledge Base** - Public documentation of how everything works

Transparency builds trust and helps others learn from our work.

---

### Experimental Mindset

Quarterly Systems maintains **[[Applications#Quarterly Labs|Quarterly Labs]]** as a space for exploration:

- Try new technologies before committing
- Build prototypes to test ideas
- Share experiments even if they're unfinished
- Learn from failures publicly

**Current experiments:**
- [[Applications#VoteWar|VoteWar]] - Governance games with fungible rules
- [[Applications#Larga|Larga]] - AI-powered story development tracking
- [[Applications#K5M Dashboard Experiments|Dashboard experiments]] - Animation and interface exploration

Not every experiment becomes a product. That's the point.

---

## Technology Philosophy

### Choose Boring Technology (Where It Matters)

For infrastructure and data persistence:
- **Cloudflare Pages** - Proven, fast, reliable static hosting
- **PostgreSQL** - Battle-tested database (Neon for [[Applications#Vibe News|Vibe News]])
- **Git** - Version control for content and code
- **Railway** - Simple, reliable deployment platform

### Choose Exciting Technology (Where It Helps)

For user experience and development speed:
- **InstantDB** - Real-time collaboration made simple
- **Bun** - Fast runtime for modern TypeScript projects
- **Astro** - Islands architecture for performance
- **Quartz** - Digital garden features out of the box

The rule: **Boring for reliability, exciting for velocity.**

---

## Community Philosophy

### Building for ~8 Person Teams

Most of our tools are designed for small teams:
- [[Applications/OKR-surf|OKR.surf]] - Optimal for ~8 person teams
- [[Applications#Vibe News|Vibe News]] - Team-wide collaborative curation
- [[Applications#Live Chat|Office Communications]] - Small team messaging

**Why small teams?**
- Everyone knows each other
- No need for complex permissions
- Decisions happen quickly
- Culture is coherent
- Tools can be opinionated

---

### Open Source When Possible

We share what we build:
- **[[Applications#K5M Obsidian Template|K5M Obsidian Template]]** - Productivity frameworks
- **VibeCode Platform** - Fork of open source vibes.diy
- **This Knowledge Base** - Public documentation

The exception: Client work like [[Applications/BorelCorp.com|BorelCorp]] and [[Applications/Jump-Higher|Jump Higher]] remains proprietary unless clients choose otherwise.

---

## What We're Not

To clarify our philosophy, here's what Quarterly Systems explicitly **is not**:

- **Not building for scale** - We don't optimize for millions of users
- **Not chasing funding** - We're not on the VC treadmill
- **Not focused on growth** - Success isn't measured in DAUs or MRR
- **Not enterprise-focused** - We build for small teams, not corporations
- **Not following frameworks** - We use what fits, ignore what doesn't
- **Not obsessing over perfection** - Shipped beats polished

---

## Related Reading

Our philosophy is influenced by and documented in:

- **[[Clubware]]** - Robin Sloan's vision of software for friends
- **[[Home-Cooked Software and Barefoot Developers]]** - Maggie Appleton on local software
- **[[What the world needs now is groupcore]]** - Small-group focused applications
- **[[Insights#Branch: Building Clubware, Not Software|Branch video]]** - Building for discovery, not scale
- **[[Company/KmikeyM|KmikeyM Project]]** - The company context and history

---

## Living Philosophy

This philosophy isn't static. It evolves as we build, learn, and discover what works.

**Current explorations:**
- How small can successful software be?
- What does real-time collaboration enable for small teams?
- Can AI tools accelerate vibe coding without losing the vibe?
- What happens when game rules are themselves tradeable assets? ([[Applications#VoteWar|VoteWar]])

---

*This philosophy guides our work but doesn't dictate it. When principles conflict with user needs, users win.*
