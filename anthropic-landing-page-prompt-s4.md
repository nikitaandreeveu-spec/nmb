---

## Section 4: Strategic Foresight – Designing for the Agentic Future

**Section heading:** `Strategic Foresight – Designing for the Agentic Future`
**Section subheading:** `A scenario-based view from 2026 to 2035`

### Layout
A **split-pane vertical structure** within the section:
- **Top pane:** Full-width Future Cone illustration (pure CSS/SVG — no images)
- **Bottom pane:** Two equal-width cards in a **2-column grid** — "Scenario-Informed Redesign" (left) and "Risks & Mitigation" (right)

---

### Top Pane: The Future Cone (2026–2035)

**Implementation instruction:** Render the Future Cone as a pure CSS trapezoid or SVG shape — a horizontal cone that expands left-to-right. The leftmost tip is labeled `Now (2026)` and the rightmost open edge is labeled `Future (2035)`. The cone interior is divided into three horizontal bands, stacked top-to-bottom within the cone shape.

**Cone dimensions:** Full section width, `220px` tall. Beige background. The cone outline uses a `1px` charcoal stroke.

**Timeline axis:** A thin `1px` charcoal horizontal baseline runs along the bottom of the cone from left to right, with three tick marks labeled `2026`, `2028`, and `2035`.

#### Three Future Bands (rendered inside the cone, left to right, increasing width)

| Band | Label | Color treatment | Content |
|---|---|---|---|
| **Probable** | `Probable Future — 2026` | Charcoal text, no fill | **"The Digital Coworker"** — AI evolves from a simple instrument into a partner that automates dynamic, multi-step processes |
| **Plausible** | `Plausible Future — 2028` | Charcoal text, faint `--border` tint fill | **"The Trust Crisis"** — Unsupervised agentic loops lead to an accountability crisis; only 1 in 3 consumers currently trust AI to act in their best interest |
| **Preferable** | `Preferable Future — Our Goal` | Safety Green text (`var(--accent-green)`), faint green tint fill (`#4A7C5912`) | **"The Outcome Economy"** — AI as a reliable "Invisible Workforce"; companies pay only for measurable, successful results |

**Cone label positions:** Each band label sits above its corresponding section of the cone in `11px`, uppercase, wide-tracked text. The Preferable Future label renders in `--accent-green`; the others in `--text-primary`.

**Connector note:** A small `▶` arrow or dot at the leftmost tip of the cone indicates the starting point, labeled `Now`. No other decorative elements.

---

### Bottom Pane: Two-Column Action Cards

Same card styling as Sections 2 and 3: `--surface` background, `1px --border` outline, `24px` padding.

---

#### Bottom Left Card: Scenario-Informed Redesign

**Card heading:** `From "Talk" to "Task"`
**Heading style:** `16px`, uppercase, `letter-spacing: 0.08em`, charcoal

**Decision 1**
- **Label** *(Safety Green, `11px`, uppercase)*: `Decision 1`
- **Title:** Outcome-Based Economics
- **Body:** Shifted from seat-based SaaS because agents decouple output from human headcount. Revenue model now charges per "Successful Mission" — e.g., ticket resolved, contract drafted.

**Decision 2**
- **Label** *(Safety Green, `11px`, uppercase)*: `Decision 2`
- **Title:** Digital Provenance Integration
- **Body:** To close the "Trust Gap," verifiable audit trails are added to core model activities — ensuring every autonomous action is explainable and audit-ready.

**Visual separator between decisions:** A single `1px --border` horizontal rule.

**Narrative link** *(bottom of card, `12px`, charcoal, `opacity: 0.6`, italic)*:
> "Justified by the Preferable Future scenario above — see Slide 3 recommendation."

---

#### Bottom Right Card: Risks & Mitigation

**Card heading:** `Guarding Autonomy`
**Heading style:** Same as left card

**Primary Risk row**
- **Label** *(Alert Orange `var(--accent-orange)`, `11px`, uppercase)*: `Primary Risk`
- **Icon:** `▲` in `--accent-orange`, `12px`
- **Title:** Fragility of Autonomy
- **Body:** Autonomous agents are vulnerable to "action hallucinations" — an incorrect sequence of steps can cause real-world operational or financial damage.

**Visual separator:** `1px --border` horizontal rule.

**Mitigation 1**
- **Label** *(Safety Green, `11px`, uppercase)*: `Mitigation 1 — Human-in-the-Loop`
- **Body:** Mandatory safety checkpoints for high-consequence actions (e.g., mass communications or financial transfers) requiring human sign-off before execution.

**Mitigation 2**
- **Label** *(Safety Green, `11px`, uppercase)*: `Mitigation 2 — Regulatory Sandboxes`
- **Body:** All agentic workflows tested in isolated environments before production to prevent cascading errors.

**Visual treatment for Mitigation labels:** Render each mitigation label with a small Safety Green `●` dot prefix to visually distinguish them from the risk row.

---

### Section 4 — Responsive Behaviour

| Breakpoint | Behaviour |
|---|---|
| `>= 1024px` | Full split-pane: cone top, 2-column cards bottom |
| `768px – 1023px` | Cone scales to full width; cards stack to single column |
| `< 768px` | Cone simplifies to a styled text list (Probable / Plausible / Preferable as stacked rows with left-border color coding); cards remain stacked |

**Mobile cone fallback:** When the SVG/CSS cone cannot render cleanly, replace it with three stacked `<div>` rows, each with a `4px` left border:
- Probable: `--border` color border
- Plausible: `--border` color border, faint grey background
- Preferable: `--accent-green` border, faint green background

---

### Section 4 — Implementation Notes

1. **Future Cone rendering:** Prefer an inline `<svg>` with a `<polygon>` or `<path>` for the cone outline, and `<rect>` or `<clipPath>` elements for the three internal bands. This avoids any image dependency and keeps the file self-contained.
2. **No JS required** for this section. All states are static.
3. **Narrative continuity:** This section must visually reference Section 3's "Most Viable" recommendation (Outcome-Based Agentic Workforce). The Preferable Future band in the cone should feel like a deliberate callback — same Safety Green treatment, same language ("Invisible Workforce", "Outcome Economy").
4. **Section `id`:** `id="foresight"` for anchor linking consistency with the rest of the page.