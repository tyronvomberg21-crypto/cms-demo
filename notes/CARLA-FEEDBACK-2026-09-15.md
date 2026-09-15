# Carla's feedback on the CMS demo — email Tue 15 Sep 07:31 (+ voice note 07:39)
_"I am very impressed! You have great visual eye and strong semantic layout fundamentals."_ Then four CSS "gotchas". Her prescribed order: **(1) give these notes to Claude and apply them to the demo → (2) then layer her HTML (attachment `Hermanus Dorpshuys-cds.html`) → (3) share back → (4) she layers SEO improvements → (5) personal-brand SEO / footer backlink conversation.**

## 1. Fixed image frames & 1px borders
- Issue: `.frame::after` offset pseudo-element breaks image alignment, floating artifacts.
- Fix: drop the pseudo-element; explicit `border:1px solid rgba(18,51,60,0.12)` on `.frame`; subtler drop shadows; feature photos in crisp framed boxes.

## 2. Heavy gradient mask on the hero
- Issue: muddy 3-stop overlay (`rgba(18,51,60,.82)…`) → dark band across the page.
- Fix: soft dual-stop mask `rgba(18,51,60,0.45) → 0.75` + `backdrop-filter: contrast(1.05)`.

## 3. Unused grid space / asymmetric columns
- Issue: `.two-col` = `1.05fr .95fr` with heavy right margins → gaps on large desktops.
- Fix: `1fr 1fr`, container max-width **1200px** (from 1140px).

## 4. Code structure
- CSS indented into sections (Base, Typography, Components, Sections).
- Fallback `border` on `.room-card`, `.act`, `.rev` for clean separation on high-DPI/mobile.

## Footer backlink (for every client site)
```html
<footer>Designed & Developed by <a href="https://joshuavomberg.co.za" target="_blank" rel="noopener">Joshua.digital</a></footer>
```
## Voice note 07:39 (transcribed)
"Staggered approach… the notes are all around the technical application of the design — images, a one-pixel border, things floating that shouldn't… look and feel barely different, it's about the technical HTML. Second note: backlinks in footers → your personal brand → AI visibility. SEO for Josh Vomberg / Joshua.digital is different to SEO for your clients. Next: technical SEO. Nothing is prescriptive — if you disagree, motivate why. 30 years of experience; we are collaborating."
