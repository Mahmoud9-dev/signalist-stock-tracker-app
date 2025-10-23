# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Development Commands

### Core Development
- `npm run dev` - Start development server with Turbopack for fast hot reloading
- `npm run build` - Build production application with Turbopack optimization
- `npm start` - Start production server (requires build first)
- `npm run lint` - Run ESLint to check code quality and style

### Package Management
- `npm install` - Install all dependencies
- `npm ci` - Clean install for production/CI environments

### Type Checking
This project uses TypeScript but doesn't have a dedicated type-check script. Use `npm run build` to catch type errors during compilation.

## Project Architecture

### Technology Stack
- **Framework**: Next.js 15.5.4 with App Router
- **Language**: TypeScript with strict configuration
- **Styling**: Tailwind CSS v4 with PostCSS
- **Build Tool**: Turbopack (Next.js built-in)
- **Fonts**: Geist Sans and Geist Mono from Google Fonts

### Directory Structure
- `app/` - Next.js App Router directory containing pages and layouts
  - `layout.tsx` - Root layout with font configuration and metadata
  - `page.tsx` - Home page component
  - `globals.css` - Global styles with Tailwind CSS and CSS variables
- `public/` - Static assets (SVG icons, images)
- Configuration files at root level

### Key Architectural Decisions
- Uses Next.js App Router (not Pages Router) for routing and layouts
- Tailwind CSS v4 with inline theme configuration in CSS
- TypeScript with strict mode enabled and path aliases (@/* for root imports)
- ESLint configured with Next.js recommended rules and TypeScript support
- Font optimization using next/font/google with variable CSS custom properties

### Development Notes
- The project is currently a fresh Next.js installation with default template content
- Uses Turbopack for both development and build processes for improved performance
- Dark/light mode support implemented through CSS custom properties and prefers-color-scheme
- ESLint ignores common Next.js build directories (.next/, build/, out/)
- No testing framework is currently configured