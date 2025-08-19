# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

This is a Nuxt.js application using pnpm as the package manager. Use these commands:

- **Install dependencies**: `pnpm install`
- **Development server**: `pnpm dev` (runs on http://localhost:3000)
- **Build for production**: `pnpm build`
- **Preview production build**: `pnpm preview`
- **Generate static site**: `pnpm generate`
- **ESLint checking**: `npx eslint .` (using @nuxt/eslint module)

## Architecture Overview

This is a minimal Nuxt 4 application with the following structure:

### Core Framework
- **Nuxt 4**: Vue.js meta-framework with file-based routing
- **TypeScript**: Configured via tsconfig.json with Nuxt defaults
- **Vue 3**: Component framework with Composition API

### Key Modules
- **@nuxt/content**: Content management system for markdown files
- **@nuxt/ui**: UI component library 
- **@nuxt/image**: Optimized image handling
- **@nuxt/eslint**: ESLint integration with Nuxt-specific rules

### Project Structure
- `app/app.vue`: Root application component with NuxtLayout and NuxtPage
- `pages/`: File-based routing (currently has empty index.vue)
- `content/`: Markdown content files processed by @nuxt/content
- `content.config.ts`: Defines content collections, configured for page-type markdown files
- `nuxt.config.ts`: Main configuration with modules and devtools enabled

### Content System
The @nuxt/content module is configured to treat all markdown files as page-type content. Content is managed through collections defined in content.config.ts, making it suitable for documentation sites or content-heavy applications.

### Development Notes
- Uses pnpm-lock.yaml indicating pnpm is the preferred package manager
- ESLint is configured through the Nuxt module system rather than standalone config
- Devtools are enabled for development debugging
- Currently has minimal page content, appears to be in early setup phase