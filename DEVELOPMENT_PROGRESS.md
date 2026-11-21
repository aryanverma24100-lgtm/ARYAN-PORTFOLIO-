# Development Progress

## Phase 0 – Backend core (earlier, untested)
Schema (16 tables), weighted scoring, content-hash change detection, `/api/evaluate` route.
Lives in `../portfolio-ai/`. Not connected to the website yet.

## Phase 1 – Portfolio website

### Files
- `../portfolio.html`: the approved single-file Phase 1 version, kept unchanged as the reference.
- `./`: the Next.js App Router conversion (this folder). Source is complete.

### Preserved from the single-file version
- Content: all sections, headings and wording, including the NeevX, PowerCare and AI/ML entries.
- Editable fields with the same storage keys (`neevx.problem`, `sk.s0`, `about.journey`, …).
- Edit mode, drag-and-drop and arrow reordering of skills and projects.
- Links for GitHub, LinkedIn, resume, email and each project, set under Contact → Edit links.
- Photo upload, typing animation, dark/light theme, mobile menu, active section highlight.
- Migration: on first load, data saved by the single-file version is read and copied to the new keys.

### Changes from the single-file version
- Built with Next.js App Router, React, TypeScript, Tailwind CSS and Framer Motion.
- Link prompts replaced by a validated form in Contact.
- Profile completeness is now a clear count of filled fields.
- The contact form only builds a mailto link and stores nothing.
- Added robots.txt, sitemap.xml, JSON-LD Person data, a skip link, security headers, and custom 404 and error pages.

### Architecture notes for Phase 2
- Content state lives in `components/ContentProvider.tsx` and `lib/storage.ts`. Phase 2 can replace
  `loadState` and `saveState` with API calls without changing the components.
- Default content is in `lib/content.ts`.

### Not done
- No backend, database or AI features (by request).
- No resume file upload. The resume is a URL.
- No screenshot upload. Screenshots are a text field.

### Verification status
- DONE: every `@/` import resolves to an existing file, and client components carry `"use client"`.
- NOT DONE: `npm install`, TypeScript check, production build, dev server, browser testing.
  The build environment could not reach the npm registry, so none of these have run.

Pending checks, to run locally:
- [ ] `npm install`
- [ ] `npm run typecheck`
- [ ] `npm run build`
- [ ] `npm run dev`, then check every section at desktop, tablet and phone widths
- [ ] Dark and light themes, mobile menu, drag and arrow reordering, edit mode, link validation

Awaiting approval before Phase 2.
