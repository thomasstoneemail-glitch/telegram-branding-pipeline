
# Telegram Vendor Branding Production Pipeline
## Master Specification v1.3

This document is the single source of truth for production.
If a rule is not written here, it does not exist.

---

## 1. Core Principles (Non-Negotiable)

- The approved **master logo layout** is the source of truth for:
  - scale
  - center position
  - padding
  - text / ribbon proportions
- All assets (seasonals, templates, posters, motion prompts) are derived from the master.
- After master lock, **no layout drift** is allowed.
- All static exports must be:
  - 1:1 square
  - centered
  - Telegram dark-mode safe
  - clean (no A/B/C/D labels)

No exceptions.

---

## 2. Packages

### Starter — Logo Only
Includes:
- Master logo
- 1 seasonal logo (client chooses)

Outputs:
- `/logo/master.png`
- `/seasonal/{chosen}.png`

---

### Pro — Brand Kit
Includes:
- Master logo
- All standard seasonal logos
- 3 templates:
  - announcement
  - weekly deal
  - new drop

Outputs:
- `/logo/master.png`
- `/seasonal/*.png`
- `/templates/post_announcement.png`
- `/templates/post_weeklydeal.png`
- `/templates/post_newdrop.png`

---

### Premium — Full Telegram Pack
Includes:
- Master logo
- Dark-mode logo variant
- All seasonal logos
- All templates (6)
- Showcase poster
- 1 motion prompt pack

Outputs:
- `/logo/master.png`
- `/logo/darkmode.png`
- `/seasonal/*.png`
- `/templates/*.png`
- `/exports/brand_poster.png`
- `/animation_prompts/grok_logo_loop.txt`
- `/animation_prompts/grok_storyboard.txt`

---

### Elite — Motion Brand System
Includes:
- All Premium assets
- Motion prompt packs for **every delivered asset**

Adds:
- motion prompts for:
  - master logo
  - darkmode logo
  - all seasonals
  - all templates
  - poster micro-motion

---

## 3. Add-Ons

Add-ons branch the pipeline. They do not override it.

Available:
- Extra seasonal logo
- Extra template type
- Mascot redesign
- Animated logo / motion prompts
- Remove watermark for finals
- Source files

---

## 4. Stage Map (Locked)

0. Intake  
1. Brand Lock  
2. Logo Concepts (A–D in one image)  
3. Final Master Logo  
3B. Dark-Mode Logo (Premium+)  
4. Seasonal Logos  
5. Templates  
6. Showcase Poster  
6A. Motion Prompt Packs  
7. Final Export Pack

Stages run in order. No skipping.

---

## 5. Production Rules

- No batch dumping (except logo A–D concepts).
- No silent regeneration.
- No layout changes after master approval.
- Animated deliverables are **prompt files only**.
- Every exported file must be individually deliverable.

Factory > freestyle.
