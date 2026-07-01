# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository. The project is **Arcade Vault**, a Next.js 16 (React 19) web application for playing online arcade games and competing on leaderboards. Built with TypeScript, Tailwind CSS v4, and the App Router.

## 📐 Architecture Overview

This is a single-app-router Next.js project with minimal source structure:

```
app/
  layout.tsx    # Root layout — configures Geist Sans & Mono fonts, dark mode, HTML shell
  page.tsx      # Landing page (currently default Next.js starter)
  globals.css   # Tailwind v4 import, CSS custom properties for light/dark themes
public/         # Static assets (Next.js icons to be replaced with arcade assets)
next.config.ts  # Next.js config (empty — all defaults)
```

There are no separate pages directories, API routes, components folders, or utility libraries beyond React and Next.js core. This is a greenfield app — the starter template has not yet been customized for the Arcade Vault feature set.

**Stack:** Next.js 16 App Router | React 19 | TypeScript 5 | Tailwind CSS v4 (via `@tailwindcss/postcss`) | Geist fonts



## 📚 Project Context & Requirements

- **Goal:** Online arcade game platform with scoring and competition. The README mentions "Spec Driven Design" via `/spec` and `/spec-impl` directories, following practices from the [fernando-skills](https://github.com/Klerith/fernando-skills) collection.
- **Current state:** Greenfield — the app currently renders the default Next.js starter page. No arcade game code or leaderboard logic exists yet.
- **TypeScript paths:** `@/*` maps to project root (`./*`).
- **CSS architecture:** Tailwind v4 uses `@import "tailwindcss"` in `globals.css`. Theme colors are controlled via CSS custom properties (`--background`, `--foreground`) with automatic light/dark mode based on `prefers-color-scheme`.
- **PostCSS plugin:** `@tailwindcss/postcss` (not the standalone CLI).

## Skills

Usa siempre /frontend-design para diseñar la interfaz de usuario
