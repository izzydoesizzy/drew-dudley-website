# Drew Dudley Speaking Website

A best-in-class speaker site for **Drew Dudley** — WSJ bestselling author and one of the world's most-watched TED speakers (5M+ views, "Everyday Leadership / The Lollipop Moment"). The job of every version: land new bookings.

**Five complete design directions + a full booking wizard.** All are standalone static HTML (no build step) — open any `index.html` in a browser.

## View the versions

| | Slug | Direction | Theme |
|--|------|-----------|-------|
| **V1** | `/index.html` | Minimal · ember particles | Dark, centered, restrained |
| **V2** | `/v2/` | The Marquee · editorial | Dark + light contrast, asymmetric, serif display, credential ticker |
| **V2B** | `/v2b/` | The Marquee + bio + dark proof | V2 design with a "The Speaker" bio section and a dark social-proof band (animated counters, company wall, media) |
| **V3** | `/v3/` | The Spotlight · theatrical | Deep black, cursor-follow spotlight, scene-based, indigo counterpoint |
| **V4** | `/v4/` | The Editorial · premium light | Ivory/cream magazine, drop-cap, keynote index, dark "watch" interlude |
| **V5** | `/v5/` | The Bento · modern modular | Glassy rounded bento tiles, gradients, kinetic hover + count-ups |
| **Book** | `/book/` | Booking wizard (Phase 2) | Multi-step, branching, live price estimate |

```bash
open index.html      # V1
open v2/index.html   # V2 … etc.
open book/index.html # the wizard
```

Each version's **"Book Drew"** nav button opens the wizard at `/book/`.

## The booking wizard (`/book/`)

A 5-step, branching inquiry that pre-qualifies leads and shows an instant estimate:

1. **Engagement** — Keynote / Keynote + Workshop / Half-Day / Virtual / Pro-bono (each with a price band)
2. **When & where** — date + location (date drives a season multiplier)
3. **Audience** — organization + size
4. **Budget** — tiered ranges · *the Pro-bono path swaps this for a "tell us about your cause" step*
5. **Contact** — name + email + goals
6. **Result** — a computed estimate range, a qualification message (Great fit / Let's find a way / Pro-bono), a summary, and a **Send to Drew** button that composes a fully detailed email to `drew@dayoneleadership.com`

**Pricing engine:** base band by format × season factor (peak Sep–Nov & Feb–Apr +12%, off-peak Jul/Aug/Dec −8%) × audience nudge. Clearly labeled an estimate, not a quote.

## Real content & assets (pulled from Drew's live presence)

- **Sizzle reel:** official Vimeo demo reel — `player.vimeo.com/video/910976563`
- **TED talk:** `ted.com/talks/drew_dudley_everyday_leadership` (5M+ views, "one of the 15 most inspirational TED talks of all time")
- **Book:** *This Is Day One* (#6 WSJ debut) — Amazon
- **6 real keynotes:** The Leadership Test · This Is Day One · Courage · Self Respect · Elevate Don't Escalate · The Game Has No Winners
- **8 real testimonials:** US Air Force, Redfin, Monster, Blissdom Canada, California Grocers Assoc., Halton IEC, ACC New Jersey, Responsible Distribution Canada
- **Real clients:** Coca-Cola, American Express, JP Morgan Chase, United Nations, McDonald's, Procter & Gamble, PwC, Estée Lauder, 100+ universities
- **Bio + stats:** Founder & Chief Catalyst, Day One Leadership · 8 yrs U of T leadership program · charity chair (35,000 volunteers / $1M/yr)
- **Photo:** `drewdudley.com/wp-content/uploads/2021/10/Drew_Home_Page_2.jpg`
- **Contact:** drew@dayoneleadership.com · 1.855.685.3253

## Design system (shared DNA)

Rooted in The Gathering Place palette so Drew's properties feel related:
`#0c0a08` charcoal · `#c4922a` amber gold · `#f0ebe2` warm off-white · Cormorant Garamond (serif/wordmark, a West Wing stand-in) + Inter (everything else). V4 inverts to an ivory base; V5 adds glassy gradients; V3 adds a cool indigo.

All versions: responsive, `prefers-reduced-motion` honored, CDP-verified for zero horizontal overflow at 390/768px.

## Project structure

```
drew-dudley-website/
├── index.html          V1
├── v2/ v3/ v4/ v5/     four redesigns (each index.html)
├── book/index.html     booking wizard (Phase 2)
├── assets/             shared images (TGP hearthstone)
├── content/            copy.md · brand.md
├── TRANSCRIPT_SUMMARY.md
└── transcripts-link/   symlink to Drew's Fathom transcripts
```

## Open items (from Drew, before launch)

- [ ] West Wing font file (Cormorant Garamond stands in via the `--serif` variable)
- [ ] Pick the winning design direction (V1–V5)
- [ ] Confirm/replace estimate bands in `/book/` with Drew's real fee ranges
- [ ] Approve hero taglines and the "coming soon" Gathering Place link target (V1)
- [ ] Swap testimonial still-frames for real audience-reaction clips when available
```
