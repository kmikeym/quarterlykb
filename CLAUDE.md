# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

- **Build site**: `npx quartz build`
- **Serve site locally**: `npx quartz build --serve`
- **Serve docs locally**: `npm run docs`
- **Type checking**: `npm run check`
- **Format code**: `npm run format`
- **Run tests**: `npm run test`
- **CLI access**: `npm run quartz` or `npx quartz`

## Architecture Overview

This is a **Quartz v4** static site generator project configured as the "Quarterly Knowledge Base" for Quarterly Systems. Quartz transforms Markdown content into a connected digital garden with sophisticated linking, search, and navigation capabilities.

### Key Technologies

- **Quartz v4** - Static site generator with digital garden features
- **TypeScript** - Configuration and component development
- **Preact** - Component rendering (instead of React)
- **esbuild** - Fast bundling and compilation
- **Umami Analytics** - Privacy-focused analytics integration

### Configuration Architecture

**Core Files:**
- `quartz.config.ts` - Main configuration defining plugins, theme, analytics, and site behavior
- `quartz.layout.ts` - Layout definitions for different page types (content pages vs list pages)
- `content/` - Markdown content directory that becomes the knowledge base

**Plugin System:**
The site uses a comprehensive plugin architecture with three phases:
1. **Transformers** - Process Markdown (frontmatter, syntax highlighting, LaTeX, etc.)
2. **Filters** - Content filtering (removes drafts)
3. **Emitters** - Generate final output (HTML pages, RSS, sitemap, etc.)

### Content Structure

- `content/index.md` - Homepage with knowledge base overview
- `content/*.md` - Individual knowledge base articles
- **Obsidian-style linking** - Uses `[[Page Name]]` syntax for internal connections
- **Git-based dating** - Uses git history for created/modified dates

### Site Configuration

**Branding:**
- Page Title: "Quarterly Knowledge Base"
- Suffix: " | Quarterly Systems"
- Base URL: `base.quarterly.systems`

**Features Enabled:**
- Single Page Application (SPA) navigation
- Interactive popovers for link previews
- Full-text search with FlexSearch
- Graph visualization of page connections
- Table of contents generation
- LaTeX math rendering with KaTeX

**Theme Customization:**
- Custom color scheme with light/dark modes
- Typography: Montserrat headers, Inter body, IBM Plex Mono code
- Professional blue/teal color palette

### Layout System

**Content Pages** (individual articles):
- Left sidebar: Search, Explorer, Dark mode toggle, Reader mode
- Right sidebar: Graph view, Table of Contents, Backlinks
- Main content: Breadcrumbs, Article title, Content metadata, Tags

**List Pages** (folders, tags):
- Simplified layout without right sidebar
- Focus on content discovery and navigation

### Build Process

Quartz uses a sophisticated build pipeline:
1. **Content Discovery** - Scans `content/` directory
2. **Markdown Processing** - Transforms content through plugin chain
3. **Link Resolution** - Resolves `[[links]]` and builds connection graph
4. **Static Generation** - Outputs HTML, CSS, JavaScript to `public/`
5. **Asset Processing** - Handles images, favicons, and static resources

The build system supports both one-time builds and watch mode with hot reloading during development.

### Analytics Integration

Configured with Umami analytics:
- Website ID: `b956deb8-6083-434b-b9ca-ee9a02bb1842`
- Host: `https://umami-production-b991.up.railway.app`
- Privacy-focused tracking without cookies

### Development Workflow

Content is written in Markdown within the `content/` directory. The build process automatically:
- Resolves internal `[[links]]` between pages
- Generates navigation and discovery features
- Creates search indexes
- Builds the connection graph for visualization
- Processes LaTeX math and syntax highlighting

### Deployment

The site deploys automatically via GitHub Actions:
- **Branch**: `v4` (main branch for this project)
- **Trigger**: Push to `v4` branch or manual workflow dispatch
- **Target**: GitHub Pages (maps to base.quarterly.systems via DNS)
- **Build**: `npx quartz build` generates static files to `public/`
- **Requirements**: Node.js 22+, npm 10.9.2+

The workflow fetches full git history to enable git-based dating for articles.

### Static Assets

The `static/` directory contains files copied directly to the output:
- `_headers` - Cloudflare/CDN security headers configuration
- `robots.txt` - Search engine crawler configuration

### Performance Optimization

**Build Time:** The `CustomOgImages()` plugin generates Open Graph images but significantly increases build time. Comment it out in `quartz.config.ts:94` if faster builds are needed during development.

**Content Patterns Ignored:**
- `private/` - Private notes not for publication
- `templates/` - Template files
- `.obsidian/` - Obsidian vault configuration
- `drafts/` - Work-in-progress content
- `.DS_Store` files