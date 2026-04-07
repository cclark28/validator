# DemandScience — Master Project Bundle

**Version:** 2.0 | **Updated:** April 2026 | **Owner:** Charlie Clark (cclark28)

---

## Live URLs

| Resource | URL |
|----------|-----|
| ClickTag Validator (live demo) | https://cclark28.github.io/validator/ |
| GitHub repo | https://github.com/cclark28/validator |

---

## What's in this folder

```
demandscience/
├── README.md                          ← You are here
├── DESIGN.md                          ← Consolidated brand/design reference
├── DEPLOY.md                          ← Deployment notes (Figma sync)
├── FONT-VERIFICATION.md               ← Font QA checklist
├── requirements.txt                   ← Python dependencies
├── demandscience-deck.plugin          ← Cowork plugin installer (deck builder)
│
├── 00-brand/                          ← Logos, color specs, brand guide PDF
│   ├── DS-BrandGuide.pdf              ← Full brand standards PDF
│   ├── ds-design.md                   ← Master brand design system v4.0
│   ├── demandscience-logo.png         ← Primary logo (use on dark backgrounds)
│   ├── demandscience-logo-white.png   ← Reversed logo (use on light backgrounds)
│   ├── ds-icon.png / ds-icon-white.png
│   ├── ds-logo-black.png
│   ├── color.txt                      ← Hex values + gradient stops (source of truth)
│   ├── icons/                         ← UI icon assets
│   ├── misc/                          ← Miscellaneous brand assets
│   └── photography/                   ← Brand photography
│
├── 01-presentations/                  ← PowerPoint decks
│   ├── DS-Master-Deck.pptx            ← Brand-locked master template (do not overwrite)
│   ├── DS-Blank-Deck.pptx             ← Clean starter for new decks
│   ├── DS-Intent-Deck.pptx            ← Intent/demand gen positioning deck
│   └── DS-Presentations-Guide.md      ← Usage + layout instructions
│
├── 02-digital-ads/                    ← Ad creative source files
├── 03-html5/                          ← HTML5 display creative source files
│
├── 04-web-ui/                         ← Browser-based tools
│   └── clicktag-validator.html        ← TTD clickTag validator + auto-fixer
│
├── 05-assets/                         ← Shared media assets
│   ├── icons/
│   ├── misc/
│   └── photography/
│
├── 06-exports/                        ← Final delivery staging area
│
├── fonts/                             ← Locally hosted font files
│   ├── poppins/                       ← Full Poppins family (all weights)
│   └── inter/                         ← Inter variable font
│
├── design-system/                     ← Modular design system documentation
│   ├── README.md
│   ├── tokens/colors.md               ← Full color palette + WCAG specs
│   ├── tokens/typography.md           ← Type scale + font rules
│   ├── tokens/spacing.md              ← 4px base unit grid
│   ├── components/buttons.md          ← Button variants + states
│   ├── components/forms.md            ← Input, select, checkbox rules
│   ├── components/cards-modals.md     ← Card + modal patterns
│   ├── guidelines/dos-donts.md        ← Visual + copy rules
│   ├── guidelines/accessibility.md    ← WCAG 2.1 AA checklist
│   └── reference/agent-prompts.md     ← AI prompt templates for design outputs
│
├── .figma/                            ← Figma integration layer
│   ├── system/                        ← Setup guides, component specs, sync logic
│   │   ├── FIGMA-SETUP.md
│   │   ├── FIGMA-COMPONENTS.md
│   │   ├── FIGMA-SYNC-LOGIC.md
│   │   ├── INTEGRATION-CHECKLIST.md
│   │   └── TOKEN-MAPPING.md
│   └── schema/                        ← JSON registries
│       ├── component-registry.json
│       ├── token-map.json
│       └── sync-log.json
│
└── .setup/                            ← Figma first-time setup tools
    ├── START-HERE.md
    ├── QUICK-START.md
    ├── FIGMA-INTERACTIVE-SETUP.html   ← Open in browser — recommended
    ├── figma-setup-automation.py      ← API-based automated setup
    └── finalize-figma-sync.py         ← Run after Figma file created
```

---

## Brand Tokens (quick reference)

| Token | Hex | Usage |
|-------|-----|-------|
| Navy | `#061947` | H1 headings, footers, dark panels, table headers |
| Electric Blue | `#0266F7` | H2/subheads, links, icons, interactive elements |
| Purple | `#5614c1` | Secondary accent (use sparingly) |
| CTA Red | `#d42f5b` | All pill CTAs — pill-shaped only, never body text |
| White | `#FFFFFF` | Text on dark/gradient; page backgrounds |
| Light Surface | `#F3F6F9` | Form inputs, subtle section backgrounds |
| Mid Surface | `#E8EEF5` | Dividers, borders, table separators |
| Baby Blue | `#cdedfd` | Card fills, table alt rows, light brand tint |
| Body Text | `#1E293B` | Body copy on all light backgrounds |

**Gradient — 4-stop, 135°, hero backgrounds and footers only:**

```
#0F399C  0%
#121970  20%
#181776  75%
#3C13A5  100%
```

White text only on gradient. Never use for body backgrounds.

**Fonts:**
- Headlines: `Poppins SemiBold` (weight 600)
- Body: `Inter` (weight 400–500)
- Code/mono: `IBM Plex Mono` (weight 400)

---

## Setup on a New Computer

### 1. Install Claude Cowork

Download the Claude desktop app:
https://claude.ai/download

Enable Cowork mode and select this `demandscience/` folder as your workspace.

### 2. Install the DemandScience Deck plugin

Double-click `demandscience-deck.plugin` in this folder.
Cowork will prompt for confirmation. Accept.

This installs the brand-locked PowerPoint builder with all fonts embedded, colors locked, and all 6 layout templates ready. Outputs save to `01-presentations/`.

### 3. Reinstall marketplace plugins

These are cloud-hosted. Reinstall from Cowork → Plugins for the ones you need:

| Plugin | What it does |
|--------|-------------|
| `brand-voice` | Enforce brand voice in content; generate guidelines from docs/calls |
| `design` | Design critique, dev handoff specs, accessibility audits, UX copy |
| `marketing` | Campaign plans, content drafts, email sequences, SEO audits |
| `sales` | Account research, call prep, outreach drafting, pipeline review |
| `engineering` | Code review, architecture decisions, debugging, standup updates |
| `product-management` | PRDs, sprint planning, roadmaps, stakeholder updates |
| `data` | SQL queries, dashboards, statistical analysis, data visualization |
| `operations` | Process docs, runbooks, change requests, risk assessments |
| `legal` | Contract review, NDA triage, compliance checks, legal responses |
| `finance` | Journal entries, reconciliation, SOX testing, variance analysis |
| `enterprise-search` | Cross-platform knowledge search + daily/weekly digests |
| `productivity` | Task management + persistent memory across sessions |
| `customer-support` | Ticket triage, draft responses, KB articles, escalations |

### 4. Python dependencies (automation scripts)

```bash
cd demandscience
pip install -r requirements.txt --break-system-packages
```

### 5. Node.js (deck build script)

Node 18+ is required for the deck builder's `build/build-pptx.js` script.

```bash
node --version   # must be v18 or higher
```

### 6. Figma integration (optional)

If you want Figma bidirectional sync, three paths are available:

| Method | Time | How |
|--------|------|-----|
| Interactive HTML guide (recommended) | ~2 hrs | Open `.setup/FIGMA-INTERACTIVE-SETUP.html` in browser |
| API automation script | ~10 min | `python3 .setup/figma-setup-automation.py TOKEN TEAM_ID` |
| Manual detailed setup | ~3 hrs | Follow `.figma/system/FIGMA-SETUP.md` |

After creating the Figma file, run:
```bash
python3 .setup/finalize-figma-sync.py "YOUR_FIGMA_FILE_URL"
```

---

## ClickTag Validator

**Local use:** Open `04-web-ui/clicktag-validator.html` directly in any browser. No server, no install.

**Hosted:** https://cclark28.github.io/validator/

**Validation rules (The Trade Desk spec):**

| Check | Severity | Auto-fixed? |
|-------|----------|------------|
| `index.html` present in ZIP | Error | No — structural |
| `var clickTag` declared | Error | Yes — injects into `<head>` |
| Variable name is exactly `clickTag` | Error | Yes — normalizes casing |
| Declaration is in `<head>` | Warning | Yes — moves from body |
| `window.open(clickTag)` call present | Warning | No — flagged for manual fix |
| ZIP filename has no spaces | Error | Yes — kebab-case rename |

**Workflow:** Drop ZIP files → Validate All → Fix & Repackage All → Download corrected ZIPs

Output ZIPs are renamed to `kebab-case-no-spaces.zip` automatically.

---

## Deck Builder

In Cowork, say: *"Build me a deck about [topic]"* and the plugin generates a fully branded `.pptx` in under 60 seconds. Saved to `01-presentations/`.

Layouts available: `cover`, `section-divider`, `title-body`, `title-only`, `two-column`, `image-text`, `data-table`.

---

## File Naming Conventions

| Type | Convention | Example |
|------|-----------|---------|
| All files | No spaces, kebab-case | `my-file-name.html` |
| Presentations | `DS-[Name]-Deck.pptx` | `DS-Q2-Review-Deck.pptx` |
| HTML creatives | `[client]-[size]-[version].html` | `acme-300x250-v2.html` |
| Creative ZIPs | `[client]-[size]-[date].zip` | `acme-300x250-2026-04.zip` |
| Design docs | UPPERCASE for top-level | `DESIGN.md`, `README.md` |

---

## Changelog

| Date | Change |
|------|--------|
| 2026-04-07 | v2.0 — Full bundle with clickTag validator, deck builder plugin, Figma integration layer, complete design system v4.0 |
| 2026-04-07 | ClickTag validator deployed to GitHub Pages (https://cclark28.github.io/validator/) |
| 2026-04-07 | Figma integration setup tools added (.setup/ directory) |
