# Changelog

All notable changes to this site will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned
- Sub-pages for each category: `/games`, `/apps`, `/mods`, `/mc`, `/world`
- Case-study detail pages for individual works
- Real screenshots and key art replacing placeholders
- `/changelog` page rendering this file

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
