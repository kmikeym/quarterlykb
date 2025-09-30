---
title: Landing Platform
date: 2025-09-29
tags:
  - kb
  - operational
  - landing
  - platform
  - astro
  - tailwind
  - cloudflare
publish: true
---
# Landing Platform

The Landing Platform serves as the primary public-facing website for Quarterly Systems, providing company information, application showcases, and operational transparency features.

## Overview

**URL**: `quarterly.systems`
**Purpose**: Marketing site and operational dashboard for Quarterly Systems
**Architecture**: Static site with dynamic status integration

## Technology Stack

### Core Framework
- **Astro 5.14.1** - Static site generator with component-based architecture
- **TypeScript** - Type safety and enhanced development experience
- **Node.js 22+** - Runtime environment

### Styling & UI
- **Tailwind CSS 3.4.0** - Utility-first CSS framework
- **Custom Design System** - Consistent purple/blue accent colors, gradient backgrounds
- **Responsive Grid Layouts** - Mobile-first responsive design
- **Google Fonts** - Montserrat headers, system fonts for body text

### Interactive Features
- **Leaflet 1.9.4** - Interactive maps for status dashboard
- **Three.js 0.180.0** - 3D graphics library (installed, not actively used)
- **Real-time Status Integration** - Live data from external APIs

### Build & Deployment
- **Static Site Generation** - Pre-built HTML/CSS/JS
- **Cloudflare Pages** - Hosting and global CDN
- **Git-based Deployment** - Automatic builds on commit

## Site Architecture

### Pages Structure
```
/                    → Main landing page
/about              → Company information and founder profile
/apps               → Platform applications showcase
/waitlist           → Contact and waitlist form
/status             → Real-time operational dashboard
/status/history     → Historical activity data
/admin/location     → Location update interface (admin)
```

### Key Components

**Layout System**:
- `src/layouts/Layout.astro` - Base template with meta tags, favicon
- Consistent navigation across all pages
- Responsive footer with company branding

**Content Sections**:
- Hero section with value proposition
- Feature grid highlighting platform capabilities
- Client testimonials with company references
- Application showcase cards with status badges

## API Integrations

### Status Dashboard
- **Location API**: `https://status-api.quarterly.systems/api/location`
- **Activity Feed**: `https://status-api.quarterly.systems/api/status`
- **Admin Updates**: POST endpoints for location management

### Contact Form
- **Formspree Integration**: `https://formspree.io/f/xrbyewjk`
- **Form Fields**: Name (required), Email (required), Company (optional), Message
- **Email Delivery**: Automated routing to configured recipient
- **Response Time**: 24-hour commitment displayed to users

### Data Flow
1. Real-time location tracking via geolocation API
2. Activity aggregation from multiple sources
3. Live map updates using Leaflet with dark theme
4. Fallback to mock data if external services unavailable

## Hosting & Infrastructure

### Cloudflare Pages Configuration
- **Build Command**: `npm run build`
- **Output Directory**: `dist/`
- **Node Version**: 22
- **Static Asset Optimization** - Automatic compression and caching

### Domain Setup
- Primary: `quarterly.systems`
- SSL/TLS encryption enabled
- Global CDN distribution
- Custom error pages

## Content Strategy

### Messaging Architecture
- **Primary Value Prop**: "Transform Ideas Into Operational Systems"
- **Target Audience**: Business leaders and technical teams
- **Positioning**: "Business-grade vibe coding platform"

### Application Showcase
1. **VibeCode Platform** (Beta) - No-code/low-code development
2. **Office Communications** (Live) - Self-hosted team messaging
3. **Operational Status** (Beta) - Real-time transparency dashboard

### External Links
- Knowledge Base: `https://base.quarterly.systems`
- VibeCode Platform: `https://vibecode.quarterly.systems`
- Office Communications: `https://office.quarterly.systems`

## Performance & Analytics

### Optimization
- Static generation for fast load times
- Tailwind CSS purging for minimal bundle size
- Image optimization for logos and founder photo
- Responsive images with proper sizing

### Monitoring
- Real-time status monitoring via activity feed
- Error handling for API failures
- Graceful degradation for JavaScript-disabled users

## Development Workflow

### Local Development
```bash
npm run dev     # Development server
npm run build   # Production build
npm run preview # Preview build locally
```

### Content Updates
- Markdown-based content in Astro components
- Direct editing for testimonials and feature descriptions
- Version controlled through Git

### Deployment Process
1. Commit changes to main branch
2. Cloudflare Pages automatically builds
3. Global deployment within minutes
4. Status API continues serving real-time data

## Operational Notes

### Status Dashboard Features
- Live location tracking with interactive map
- Activity feed from development and deployment systems
- Administrative interface for location updates
- Historical activity archive

### Maintenance
- Static site requires minimal ongoing maintenance
- API dependencies managed separately
- Regular content updates via Git workflow
- Cloudflare handles infrastructure scaling

## Recommended Enhancements

### Analytics Integration
**Current Status**: No analytics currently implemented on landing page

**Recommended Options**:
- **Umami Analytics** - Privacy-focused, cookieless tracking (consistent with Knowledge Base)
- **Plausible Analytics** - Simple, privacy-respecting alternative
- **Google Analytics 4** - Comprehensive tracking with enhanced privacy controls
- **Fathom Analytics** - Paid privacy-focused solution

**Implementation**: Add analytics script to `src/layouts/Layout.astro` head section

### Site Monitoring
**Current Status**: Basic status monitoring via activity feed

**Recommended Services**:
- **UptimeRobot** (Free tier) - Monitor site availability and response times
- **Pingdom** - Advanced performance monitoring
- **Better Uptime** - Modern uptime monitoring with status pages
- **Sentry** - Error tracking for JavaScript issues

**Key Metrics to Monitor**:
- Site availability and response times
- Contact form submission success rates
- Status API endpoint health
- Core Web Vitals and performance metrics

### Service Dependencies for Recreation

**Required Services**:
1. **Cloudflare Pages** - Static hosting and CDN (Free tier available)
2. **Formspree** - Contact form backend (Free: 50 submissions/month)
3. **Custom Status API** - Backend service for real-time features
   - **Railway** (recommended, $5-10/month)
   - **Vercel Functions** (serverless alternative)
   - **Digital Ocean App Platform**
4. **GitHub** - Git repository hosting (Free for public repos)
5. **Domain Registration** - Through Cloudflare or preferred registrar

**Estimated Monthly Cost**: 
- $6-11 (minimal setup)
- $45-70 (professional setup)

---

*Last updated: 2025-09-29*