---

## Section 5: Sustainable & Responsible Strategic Design

**Section heading:** `Sustainable & Responsible Strategic Design`
**Section subheading:** `The frameworks behind multidimensional value creation`

### Layout
A **two-column "Tool Profile" grid** — one card per framework tool, equal width, vertically aligned. Same card spec as Sections 2, 3, and 4: `--surface` background, `1px --border` outline, `24px` padding.

Generous vertical whitespace above and below the card grid (`80px` top padding, `80px` bottom padding). This is the most whitespace-heavy section on the page — intentional brand breathing room.

---

### Left Card: The Triple Layered Business Model Canvas (TLBMC)

**Card heading:** `Triple Layered Business Model Canvas`
**Heading style:** `16px`, uppercase, `letter-spacing: 0.08em`, charcoal

#### Tool Icon (top of card, above heading)
Render as inline SVG — three concentric/stacked squares, each offset `4px` down and right from the one above, `1px` charcoal stroke, no fill. Dimensions: `48px × 48px` bounding box. No labels on the icon itself.

#### Purpose Label
- **Style:** `11px`, uppercase, `letter-spacing: 0.1em`, Safety Green (`var(--accent-green)`)
- **Text:** `Economic · Environmental · Social`

#### Reasoning Block 1
- **Label** *(Safety Green `●` dot prefix, `11px`, uppercase)*: `Environmental Accountability`
- **Body:** Essential for managing the AI-Energy Nexus. Training frontier models requires gigawatts of compute — this tool maps electricity and water usage directly against economic goals, making environmental cost visible inside the business model.

**Visual separator:** `1px --border` horizontal rule between reasoning blocks.

#### Reasoning Block 2
- **Label** *(Safety Green `●` dot prefix, `11px`, uppercase)*: `Multidimensional Reporting`
- **Body:** As a Public Benefit Corporation, Anthropic must account for social benefits beyond revenue. The TLBMC provides a dedicated layer to track how "Alignment Science" creates value for society and regulators.

#### Card footer tag
- **Style:** `11px`, charcoal, `opacity: 0.5`, italic, flush to bottom of card
- **Text:** `Applies to: AI-Energy Nexus · PBC Compliance · Frontier Engineering`

---

### Right Card: The Flourishing Business Canvas

**Card heading:** `Flourishing Business Canvas`
**Heading style:** Same as left card

#### Tool Icon (top of card, above heading)
Render as inline SVG — a circle (`40px` diameter, `1px` charcoal stroke, no fill) containing a smaller concentric target circle (`20px` diameter), with a minimal leaf shape (two curved `<path>` lines forming a pointed oval) centered inside. Bounding box: `48px × 48px`. No labels on the icon.

#### Purpose Label
- **Style:** `11px`, uppercase, `letter-spacing: 0.1em`, Safety Green
- **Text:** `Purpose · Ecosystem · Flourishing`

#### Reasoning Block 1
- **Label** *(Safety Green `●` dot prefix, `11px`, uppercase)*: `Purpose-Centric Design`
- **Body:** Unlike standard canvases, this tool places Purpose at the center — ensuring the "Outcome-Based Agentic Workforce" model stays aligned with Anthropic's legal mission to serve humanity's long-term well-being, not just quarterly revenue targets.

**Visual separator:** `1px --border` horizontal rule.

#### Reasoning Block 2
- **Label** *(Safety Green `●` dot prefix, `11px`, uppercase)*: `Ecosystem Orchestration`
- **Body:** The "Ecosystem Actors" block is critical for designing the Governance-as-a-Service pathway — allowing Anthropic to involve regulators and partners (Palantir, AWS) in the co-creation of safety standards rather than imposing them unilaterally.

#### Card footer tag
- **Style:** `11px`, charcoal, `opacity: 0.5`, italic, flush to bottom of card
- **Text:** `Applies to: GaaS Pathway · Agentic Workforce · PBC Mission`

---

### Bottom Strategic Alignment Footer

Render below the two-column card grid, separated by `48px` of vertical whitespace.

A single full-width text block, centered:

> *"Moving from profit-only modeling to a multidimensional value system that protects the integrity of human-AI interaction."*

- **Style:** `14px`, italic, charcoal, `opacity: 0.65`, centered, max-width `640px`, `margin: 0 auto`
- **No border, no background** — pure typographic element floating in beige space

This is distinct from the global page footer (the legal disclaimer line) — it is a section-specific statement and sits inside `<section id="responsible">` above the global footer.

---

### Section 5 — Responsive Behaviour

| Breakpoint | Behaviour |
|---|---|
| `>= 1024px` | 2-column card grid, full whitespace margins |
| `768px – 1023px` | 2-column grid maintained; reduce top/bottom padding to `48px` |
| `< 768px` | Cards stack to single column; padding reduces to `32px`; SVG icons scale to `40px` |

---

### Section 5 — Implementation Notes

1. **SVG icons must be inline** — no `<img>` tags, no external files. Both icons are described precisely enough above to be constructed with 3–5 SVG primitives each (`<rect>`, `<circle>`, `<path>`).
2. **Whitespace is structural, not decorative** — do not reduce the `80px` vertical padding to fit content. If content is tight, reduce font size before reducing whitespace.
3. **Card height:** Both cards must be equal height. Use CSS `align-items: stretch` on the grid container so shorter content does not produce uneven card heights.
4. **Footer tags at card bottoms:** Use `margin-top: auto` on the footer tag element inside a flex column card to push it to the bottom regardless of content height — ensuring visual alignment across both cards.
5. **Narrative continuity:** The card footer tags (`Applies to:`) explicitly reference pathways from Sections 2 and 3. This creates a visible connective thread across the full page without requiring the reader to scroll back.
6. **Section `id`:** `id="responsible"` for anchor consistency.