# Changelog

All notable changes to this site will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.8.0] - 2026-04-21

### Added
- Per-work **theme** support: each work may declare a `theme` object that overrides the site's CSS custom properties (bg, accent, text, etc.)
- Smooth theme transition: selecting a work applies its theme and briefly toggles a `.theming` class on `<body>`, letting every colored surface animate (background, text, border, shadow, fill, stroke) in sync over ~0.55s
- CarbCycle now ships a dark theme matching its actual app (#121212 bg / #1E1E1E cards / #FF9800 orange accent / light text) — clicking CarbCycle in the sidebar smoothly recolors the whole page
- Selecting a work without a `theme`, or returning to the empty state, restores the site's default cream palette

### Changed
- `select()` now applies the work's theme alongside the main-panel render


### Planned
- Extend the EN / 中文 toggle to the rest of the site (index.html)
- Sub-pages for each category: `/games`, `/apps`, `/websites`, `/mods`, `/mc`, `/world`
- Case-study detail pages for individual works
- `/changelog` page rendering this file

## [0.7.0] - 2026-04-21

### Added
- First real work: **CarbCycle** under Apps — hero key art + two phone screenshots (`Image/carbcycle/`), full bilingual title / subtitle / tags / description, platform badge (iOS · Android), IN DEVELOPMENT status
- EN / 中文 language toggle in the Works page nav, persisted via localStorage (`ps_lang`)
- `t()` i18n helper: any string field in UI labels or work data may be a plain string or `{ en, zh }` object
- Image support in the work renderer: `heroImg` renders an `<img>` in the hero banner; each entry in `shots` can be `{ img, alt }` for image screenshots or a plain string for placeholder labels
- Phone screenshot variant (`.screenshot.phone`, aspect-ratio 9/19) and two-column screenshot grid (`.cols-2`) for apps

### Changed
- All UI chrome on the Works page (nav, page header, sidebar title, empty state, screenshots heading, coming-soon card) now renders through the `ui` strings table and switches language instantly
- Category and subgroup labels defined as `{ en, zh }` objects (Games/游戏, Apps/应用, Websites/网站, Mods/模组, Minecraft/我的世界, World/世界观, PC/PC 端, Mobile/移动端)
- Fonts updated to fall back through Noto Sans SC so Chinese characters render correctly in pixel-styled labels

## [0.6.0] - 2026-04-21

### Added
- Data-driven Works page: single `categories` array at the top of the inline script defines every category/subgroup; adding a work is just pushing an object into the matching `works: []`
- Auto-hide empty categories and subgroups — if a group has zero works, its sidebar block doesn't render
- Empty state: when no works exist anywhere, sidebar shows "Nothing here yet" and the main panel shows a "COMING SOON" card with pixel-dot animation
- Inline example comment in the script documenting the work object shape

### Changed
- All placeholder works removed (Game Title, Mobile Game, App Name, This Site, Mod Project, MC Builds, OC World). Categories currently render empty by design
- Sidebar and main panel now rendered entirely from JS rather than hardcoded HTML

## [0.5.0] - 2026-04-21

### Added
- New top-level category **Websites** on the Works page (sidebar group + detail entry for "This Site")
- **Mobile Games** subcategory under Games, alongside the existing PC subcategory (with `subgroup-label` styling in the sidebar)
- Home page: Websites category card; Websites tag in About

### Changed
- Games sidebar group split into two subgroups: PC / Mobile
- Game Title entry clarified as PC-specific; new "Mobile Game" entry added under Mobile
- Home category cards now link to `works.html`

## [0.4.0] - 2026-04-21

### Changed
- Works page redesigned from a single filterable table to a two-column layout:
  left sidebar "Directory" (grouped by category: Games / Apps / Mods / Minecraft / World, each item with platform icon chips), right main area showing the selected work's hero banner, status, title, tags, description, and screenshot grid
- Page header centered with pixel title + subtitle caption
- Clicking a sidebar item swaps the main panel content via JS (single-page detail view)

### Removed
- Filter bar (replaced by sidebar grouping)
- Flat works table layout

## [0.3.0] - 2026-04-14

### Added
- Dedicated `works.html` page listing all projects
- Category filter bar on Works page (All / Games / Apps / Mods / World / Minecraft) with live row filtering and count
- Active-state styling for the current page in the nav

### Changed
- Home page nav "WORKS" link now points to `works.html` instead of an in-page anchor

### Removed
- Works index table from `index.html` (moved to dedicated page)

## [0.2.0] - 2026-04-14

### Added
- Sticky top navigation (Works / Categories / Devlog / About)
- Works index table listing all projects by year, type, status, platform
- Categories grid with five entries: Games, Apps, Mods, Minecraft, World
- Devlog section with dated entries
- "Now" status badge in hero showing current focus
- About section contact card with email, Twitter, Discord, YouTube, Bilibili
- `CHANGELOG.md` following Keep a Changelog format

### Changed
- Hero simplified: removed full-screen key-art placeholder and button row; replaced with tagline + now status
- About moved from its own large section to a compressed block at the bottom
- Featured Game downgraded from standalone section to "current focus" card under the works index
- Tag set expanded from single-genre (SIMULATION / PIXEL / COZY / INDIE) to multi-category (GAMES / APPS / MODS / MINECRAFT / WORLDBUILDING / PIXEL ART)
- Footer reduced to a single copyright line (social links consolidated into About contact card)

### Removed
- Hero button row (VIEW MY GAME / DEVLOG / CONTACT)
- Stats card grid (2025 / SIM / PIXEL / SOLO)
- Three-column footer grid with duplicated links

## [0.1.0] - 2025

### Added
- Initial site: single-page layout with Hero, About, Featured Game, Footer
- Pixel + cream-color visual style (Press Start 2P, Inter, Noto Sans SC)
- Pixel roof beam decoration and twinkling star animation
- `CNAME` for custom domain
