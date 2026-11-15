# Garden Tracker — AI guide

Garden Tracker is an **offline** garden planning app by **Little Acre Labs**.
This folder is the **public reference library** (crops, lessons, recipes, and more).
It has **no personal garden data**, no accounts, and no GPS.

Gardeners can paste a plain-text summary of *their own* garden into any AI chat ("Share with my AI" in the app).
When you get that summary, you may look up facts here.

## How to use these files

- Start at the manifest: `https://neoblanks.github.io/garden-tracker-data/manifest.json` (lists every pack, version, size, sha256).
- Fetch only the JSON packs you need. Prefer https.
- Content is for gardeners **worldwide** (all hardiness zones, both hemispheres). Do not assume United States seasons or months.
- Keep answers clear and simple (about a 3rd-grade reading level when you can).
- Cite the pack name and version when you lean on a fact.

## Data set

- Manifest version: **v20**
- Needs app: **1.17.1+**
- Generated: 2026-11-15T23:44:41Z

## Packs

### Crop library (`crops.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/crops.json
- Version: **v16** · items: 140 · updated: 2026-11-15
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `crops` (see file).
- What it holds: Each crop: id, name, type (Vegetable/Grain/Herb/Fruit), family, days to maturity (dtm), spacing, sun, season, method, zones [min,max], notes, sources (src). Groups nest varieties. Worldwide hardiness zones — not US-only.

### Lessons (`lessons.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/lessons.json
- Version: **v14** · items: 210 · updated: 2026-11-15
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `lessons` (see file).
- What it holds: Short gardening lessons at about a 3rd-grade reading level. Fields: id, title, level, body (paragraphs), tip, quiz, optional series {id, part}. Part labels are Part 1, Part 2, …

### Recipes / garden meals (`recipes.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/recipes.json
- Version: **v14** · items: 197 · updated: 2026-11-14
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `recipes` (see file).
- What it holds: Recipes that use garden crops. Fields include id, title, course, time, diet tags, ingredients linked to crop ids, steps, sources.

### Preserve & Store (`storage.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/storage.json
- Version: **v14** · items: 9 · updated: 2026-11-15
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `methods` (see file).
- What it holds: Food preservation methods (canning, freezing, drying, cellar, pickling, …) plus per-crop method lists. Prefer trusted process times (USDA / NCHFP / extension).

### Garden projects (`projects.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/projects.json
- Version: **v7** · items: 35 · updated: 2026-11-09
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `projects` (see file).
- What it holds: DIY garden builds (beds, trellises, compost, …). Fields: id, title, level, materials, tools, steps, cost notes. Works for many climates.

### Explore fact cards (`explore.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/explore.json
- Version: **v10** · items: 142 · updated: 2026-11-13
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `cards` (see file).
- What it holds: Short fun facts and tips. Fields: id, kind, title, body, optional related crop/lesson, photo credit.

### Nutrition facts (`nutrition.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/nutrition.json
- Version: **v6** · items: 138 · updated: 2026-11-04
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `crops` (see file).
- What it holds: Per-crop nutrition drawn from public data (e.g. USDA). Amounts are for common serving sizes; notes say when data is generic.

### Fish & water systems (`soilless.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/soilless.json
- Version: **v4** · items: 7 · updated: 2026-11-06
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `fish` (see file).
- What it holds: Aquaponics, hydroponics and aeroponics help: fish kinds, system parts, checklists. For indoor / greenhouse growers worldwide.

### Spices guide (`spices.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/spices.json
- Version: **v3** · items: 59 · updated: 2026-11-04
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `spices` (see file).
- What it holds: Growable spices: part used, climate, harvest, dry/cure, store, cooking uses, safety warnings, sources. Includes hot peppers group.

### Currency rates (`rates.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/rates.json
- Version: **v3** · items: 30 · updated: 2026-11-13
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `rates` (see file).
- What it holds: Exchange rates so project cost estimates can show in the gardener's money. Updated from public ECB data when publishing.

### Crops around the world (`countrycrops.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/countrycrops.json
- Version: **v1** · items: 198 · updated: 2026-11-14
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `countries` (see file).
- What it holds: Top 20 crops in each country (FAOSTAT Crops and livestock products, "area harvested" in hectares, newest year; CC BY 4.0, cite FAO). Fields: id (UN M49 code), name, fao (FAO name), cont, year, nCrops, crops [{n, ha, crop?}] where crop links to a crop id.

### Crop history timeline (`crophistory.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/crophistory.json
- Version: **v1** · items: 32 · updated: 2026-11-14
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `items` (see file).
- What it holds: About how many years ago people first farmed (domesticated) each crop. Fields: id, name, ago (years, approximate), region, text, crops (crop ids), sure (false = still debated), atLeast, src. noDate lists library crops with no trusted date yet.

### Plant info words (`glossary.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/glossary.json
- Version: **v3** · items: 45 · updated: 2026-11-15
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `terms` (see file).
- What it holds: One-line meanings of words on the crop page (days to harvest, sun, zones, pollination, ⓘ tips). Fields: id, term, definition, lesson_id (links to a Plant info words lesson).

### More crop varieties (`varieties-more.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/varieties-more.json
- Version: **v1** · items: 8 · updated: 2026-11-14
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `crops` (see file).
- What it holds: Extra researched varieties beyond the first 25 on a crop page. Fields: id (crop id), varieties [{n, era (modern|historic), color, size, dtm, habit, resist, climate}]. The app uses the newest of the bundled pack and a later download; works offline. Own-words summaries of extension lists; not a catalog reprint.

### Winterizing checklists (`winterize.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/winterize.json
- Version: **v3** · items: 4 · updated: 2026-11-15
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `guides` (see file).
- What it holds: Cold-season prep guides with tickable checklists for beehives, the garden, greenhouses, and sheds or root cellars. Fields: id, title, blurb, intro, climate notes, items [{id,t}], links to existing lessons and projects, sources. Worldwide wording; metric first.

### Bees reference (`bees.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/bees.json
- Version: **v2** · items: 4 · updated: 2026-11-15
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `guides` (see file).
- What it holds: How-to-start guides (local laws, sting and allergy safety, placing a hive, nucs and packages), hive diseases and pests with notifiable notes, pollinator flowers for the Bee Happy badge, and hive health labels. Fields: guides, diseases, flowers, health, sources. Worldwide wording; metric first.

### ZIP → zone table (`zipzones.json`)

- URL: https://neoblanks.github.io/garden-tracker-data/zipzones.json
- Version: **v1** · items: 40283 · updated: 2026-10-25
- Top-level keys: `schema`, `version`, `updated`, and a list/map named `zips` (see file).
- What it holds: US ZIP codes mapped to USDA plant hardiness zones (and lat/lon). Useful for US gardeners; growers elsewhere set zone or place another way.

## Related

- Human index: https://neoblanks.github.io/garden-tracker-data/
- This guide: https://neoblanks.github.io/garden-tracker-data/ai-guide.md
- LLMs shortcut file: https://neoblanks.github.io/garden-tracker-data/llms.txt

## What is NOT here

- No user accounts, forums, or chat.
- No live weather API keys.
- No photos of people's gardens.

