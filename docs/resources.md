# KickStart Resources — Technology and Resources Reference

## The Success Stack Framework

The Success Stack is a 4-layer execution framework used in Trinity Advisory's Kickstart coaching program. Each layer builds on the one before it:

| Layer | Name | Purpose |
|---|---|---|
| 1 | I Am Statement | Identity — who you are becoming |
| 2 | SMART Goal | Specific, measurable 30–90 day target |
| 3 | X-Goal | Bold, ambitious 12-month outcome |
| 4 | Keystone Habits + Daily Actions | The recurring behaviour that drives the result |

---

## Source Files

| File | Purpose |
|---|---|
| `original files/20 Examples of I Am Statements, Smart Goals, X Goals, Keystone Habits and Daily Actions.docx` | Source document containing all 20 examples verbatim |
| `original files/Presentation - Kickstart 01 - Clarity and Identity.pptx` | Kickstart program presentation — context on the framework and brand |

---

## Application Stack

| Component | Technology |
|---|---|
| Runtime | Browser (no server required) |
| Frontend | Vanilla HTML, CSS, JavaScript (ES6) |
| Fonts | Inter via Google Fonts CDN (system fonts fallback) |
| Hosting | GitHub Pages (static file serving) |
| Build process | None — single file, no compilation |
| Dependencies | None (zero npm packages) |

---

## File Structure

```
claude code - kickstart success stack/
├── index.html              ← Entire app: layout, styles, JS, content data
├── docs/
│   ├── setup.md            ← Setup and user guide (source of truth)
│   ├── setup.html          ← Setup guide rendered as HTML
│   ├── resources.md        ← Technology and resources reference (this file)
│   └── resources.html      ← Resources reference rendered as HTML
└── original files/
    ├── 20 Examples of I Am Statements...docx
    └── Presentation - Kickstart 01 - Clarity and Identity.pptx
```

---

## Data Flow

1. All 20 Success Stack examples are stored as a JavaScript array (`EXAMPLES`) inside `index.html`.
2. On page load, `renderSidebar()` reads `EXAMPLES` and builds the navigation list.
3. `selectExample(id)` is called when a user clicks a sidebar item (or on first load for the default selection).
4. `selectExample()` finds the matching example object and calls `renderContent()`, which builds the four layer cards as an HTML string and injects it into the `#content-area` div.
5. No network requests are made after the initial page load (except Google Fonts).

---

## All 20 Success Stack Examples

### Business (Examples 1–12)

| # | Title | Focus |
|---|---|---|
| 1 | Financial Control | Revenue, profit, cash flow, debtors |
| 2 | Pricing and Profit | Margin protection, confident quoting |
| 3 | Working On the Business | CEO Hour rhythm, weekly strategy |
| 4 | Systems-Driven Operator | Documenting and improving processes |
| 5 | Team Ownership | Delegation and building accountability |
| 6 | Leadership and Accountability | Huddles, standards, accountability culture |
| 7 | Empowering Leadership | Check-ins, coaching, reducing interruptions |
| 8 | Sales Pipeline | Follow-up, CRM, pipeline management |
| 9 | Marketing and Demand Generation | Content creation, inbound leads |
| 10 | Ideal Clients | Ideal-client checklist, saying no |
| 11 | Focused Operator | Deep work, time blocking |
| 12 | Disciplined Follow-Through | Non-negotiables, consistency |

### Personal (Examples 13–20)

| # | Title | Focus |
|---|---|---|
| 13 | Calm Under Pressure | Pause-and-plan, stress response |
| 14 | Resilient Owner | Minimum viable habits, self-trust |
| 15 | Health and Energy | Exercise, sleep, energy management |
| 16 | Work-Life Boundaries | Shutdown rituals, 45-hour weeks |
| 17 | Present Parent | Phone-free family time, school holidays |
| 18 | Connected Partner | Weekly date night, relationship presence |
| 19 | Intentional Morning | Morning routine, phone-free planning |
| 20 | Personal Growth and Reflection | Weekly reflection, end-of-day review |

---

## Network and Security Notes

- The app makes no API calls and stores no user data.
- No cookies, no local storage, no analytics.
- The only external resource loaded is Google Fonts (Inter typeface). The app works fully offline if fonts are unavailable — the browser falls back to system fonts.
- No backend, no authentication, no sensitive data.
- Safe to host publicly on GitHub Pages with no additional security configuration.

---

## Brand Colours

| Name | Hex | Usage |
|---|---|---|
| Primary Blue | `#11377F` | Sidebar background, card borders, headings |
| Light Blue | `#E5F6FF` | I Am Statement card background |
| Gold | `#FFC000` | Active sidebar indicator, schedule badges, X-Goal border |
| Gray | `#A6A6A6` | Secondary labels and muted text |
| Light Gold | `#FFF8E1` | X-Goal card background |
| Off White | `#f1f5f9` | Page background |
