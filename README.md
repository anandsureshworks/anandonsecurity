# anandonsecurity

**anandonsecurity.com** — the opinionated-analysis ("the column") counterpart to the
neutral reference at [anandsureshworks.dev](https://anandsureshworks.dev).

Static, zero-dependency, zero-build. Deploys on Vercel as a static project.

## Structure
- `index.html` — the column home: masthead + essay list + subscribe link.
- `<slug>/index.html` — one directory per essay (clean URLs, e.g. `/freshness-is-not-liveness/`).
- `style.css` — shared styling (dark, readable long-form; mono chrome, green accent).
- `feed.xml` — hand-rolled Atom feed; add an `<entry>` per essay (stable `id` = canonical URL).
- `as-logo.svg` / `icon.svg` — the woven AS brand mark (masthead + favicon).

## Publishing an essay
1. Create `<slug>/index.html` from an existing essay (same `<head>` + `.wrap` + `<article>`).
2. Add an `.entry` to `index.html` and an `<entry>` to `feed.xml`; bump the feed `<updated>`.
3. Essays are human-authored — opinion, reviewed before publish (no LLM-generated security
   takes shipped unreviewed).
