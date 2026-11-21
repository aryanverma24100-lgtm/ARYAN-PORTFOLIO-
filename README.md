# Aryan Verma – Portfolio (Phase 1, Next.js)

Content is editable in the browser with the **Edit** button. Saved edits live in the visitor's browser.

## Run locally
```bash
npm install
cp .env.example .env.local
npm run typecheck
npm run dev        # http://localhost:3000
npm run build && npm start
```

## Structure
- `app/`: routes, layout, SEO files (`robots.ts`, `sitemap.ts`), 404 and error pages
- `components/`: page sections and shared UI
- `lib/`: default content, browser storage, completeness, helpers
- `hooks/`: `useTypewriter`

See `DEVELOPMENT_PROGRESS.md` for status and pending checks.
