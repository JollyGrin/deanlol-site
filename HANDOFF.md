# dean.lol — handoff

*Last updated: 2026-08-19 · state: live; housekeeping done (legacy source deleted, other repos archived, repo renamed deanlol_ssg → deanlol-site), awaiting copy pass*

## What this repo is

The repo that serves **dean.lol** via GitHub Pages from `docs/` (`docs/CNAME` → dean.lol). The site is now a **single self-contained file**: `docs/index.html` — no build step, no dependencies. Edit it, commit, push, done.

## How we got here (2026-07-27 → 28)

Three design rounds in the claude.ai/design project **"dean.lol redesign"**:

1. **Round 1 (loud)**: The Table (game-table world), The Grid (wireframe/Tron world), Ex Libris (library card-catalog world) — all loved, all too loud for a hub. Kept as candidate aesthetics for future destination subdomains.
2. **Round 2 (quiet hub)**: Hushed Paper, Threshold, The Index. Verdict: minimal + delight balance right, needed more visible frontend jazz and a tiered gallery instead of few items.
3. **Round 3 (the goof)**: Hushed Gallery, Index Remixed, One Screen. **Winner: Hushed Gallery** — warm stationery, Newsreader + DM Mono, tiered headliners (unbrewed / zen / table.place / waterhouse), "by day: thegrid.id" set apart, 12-repo goof shelf with per-chip micro-tricks, tappable Go-stone dot in the wordmark, games ribbon, previously/library/colophon beneath the fold.

Design taste settled on: **understated, graceful, surprising sparks of joy** — austere at rest, quick (200–500ms) physical micro-interactions as reward; mobile-first (~390px is the primary audience); copy says less, clicks say more.

## Safekeeping — what was here before

The previous site (Next.js 9 static-export, built 2020) lives only in git history now — `_legacy-next-ssg/` was deleted 2026-08-19 (it triggered 156 dependabot alerts); recover with `git checkout 60865bf -- _legacy-next-ssg` if ever needed. It pulled hobby cards from a **Google Sheet** via a gson proxy (`process.env.URL` — env not in repo). Its rendered content, for the record:

- **Drones** — mavic air, occasional videos
- **3D Animation** — blender goofs
- **Fun Links** — stored videos/articles
- **Pocket Band** — pocket operator backups via YouTube playlists
- **Go (better than chess)** — link to OGS profile ← *worth resurfacing in the new site*
- **th3build** — blockchain lifestyle vids with Phil
- **Ur** — Mesopotamian boardgame, local 2p in browser (lives on as ur3d.dean.lol)
- **Unbrewed** — deck simulator for Unmatched variants
- **Keyforge Cafe** — find keyforge events (pre-covid)
- Footer links: twitter @dmasley · github JollyGrin · medium post · YouTube channel


## Open work (in priority order)

1. **Copy pass** — walk every line with Dean. Known offender: colophon says *"hand-built, still goofing"* but the site was built with Claude — reword honestly (candidate: "built with a robot friend, still goofing"). Also consider resurfacing: OGS profile link on the Go stone / games ribbon, social links from the old footer.
2. **Library system** — the "the library →" doorway needs a destination. Sketch: a `library.json` (title, author, status: read/reading/next, finished date, one-line verdict) rendered client-side; start as a section or page here, graduate to `library.dean.lol` later (round-1 "Ex Libris" mockup is the candidate costume).
3. **GitHub-driven goof shelf** — shelf is currently hand-curated in HTML. Sketch: build-time or client-side fetch of JollyGrin repos + a small curation file (pin / hide / custom whisper per repo). Keep the whispers hand-written — they're the charm.
4. **Subdomain constellation** — loud round-1 directions as destination sites (games., library., museum. for BEN/unsung/nestegg/innkeeper.eth). ur3d.dean.lol is the precedent.
5. ~~**Housekeeping**~~ — done 2026-08-19: `JollyGrin/dean.lol` archived on GitHub with a README pointer here; stale local clones (`~/git/dean.lol`, `~/git/deanlol`) deleted — the only local checkout is `~/git/deanlol-site`. Still optional: a custom 404.html (old Next one was deleted).

## Assets & references

- Design explorations (all rounds): claude.ai/design → project **"dean.lol redesign"**
- Winner source of truth: `docs/index.html` in this repo
- Claude session memory: start sessions in this repo (`~/git/deanlol-site`) from this HANDOFF.md — the old `~/git/dean.lol` clone (and its session memory path) is gone.
