# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website built with Astro, TailwindCSS v4, and TypeScript.

## Commands

- `bun run dev` - Start development server at localhost:4321
- `bun run build` - Build production site to `./dist/`
- `bun run preview` - Preview production build locally

No testing or linting frameworks are configured.

## Architecture

**Framework:** Astro v5 with file-based routing
**Styling:** TailwindCSS v4 via Vite plugin, plus scoped Astro component styles
**TypeScript:** Strict mode via `astro/tsconfigs/strict`

**Key directories:**
- `src/pages/` - Route pages (index.astro → /)
- `src/layouts/` - Base HTML layout wrapper (Layout.astro)
- `src/components/` - Reusable Astro components (Welcome.astro, Link.astro)
- `src/styles/` - Global CSS with Tailwind imports
- `public/` - Static assets (favicons, PWA manifest)

**Design:** Dark theme (black background, white text), Roboto Flex variable font

## Component Patterns

- Layout.astro wraps all pages with common HTML structure
- Link.astro is a reusable component with `href`, `title`, and optional `description` props
- Use TailwindCSS utilities for styling; scoped `<style>` blocks for component-specific styles
