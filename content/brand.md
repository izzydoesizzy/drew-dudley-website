# Drew Dudley Website — Brand & Design Tokens

Shares The Gathering Place's visual system. The point of difference is the serif wordmark.

## Color Tokens (identical to TGP)

| Token | Hex | Use |
|-------|-----|-----|
| `--bg` | `#0c0a08` | Primary background (near-black charcoal) |
| `--bg2` | `#111009` | Alternate section background |
| `--bg3` | `#161210` | Card background |
| `--text` | `#f0ebe2` | Primary text (warm off-white) |
| `--text2` | `#d4cbbe` | Secondary text |
| `--muted` | `#9a8f82` | Body prose |
| `--muted2` | `#6a5e52` | Supporting text |
| `--muted3` | `#4a3e32` | Captions, fine print |
| `--muted4` / `--border` | `#2e2822` | Borders, dividers |
| `--muted5` | `#1e1a16` | Finest borders |
| `--gold` | `#c4922a` | Accent (amber gold), labels, buttons, embers |
| `--gold2` | `#c4a882` | Soft gold (inline emphasis) |
| `--gold-h` | `#d4a85a` | Button hover |

## Typography

- **Wordmark** (`.wordmark`, "Drew Dudley" + "The Gathering Place" only): `--serif`
  - Currently **Cormorant Garamond** 700 (Google Fonts) as the **West Wing stand-in**.
  - Swap when Drew provides the real West Wing font: change the one `--serif` variable in `:root`.
- **Everything else**: Inter (400/500/600/700 + italic).
- **Section labels**: 12px, uppercase, `letter-spacing: 0.3em`, gold.
- **Headings**: `letter-spacing: -0.02em`, tight line-height. Fluid `clamp()` scale `.h-xl`…`.h-xs`.
- **Buttons**: 0.875rem, uppercase, `letter-spacing: 0.15em`.

## Layout

- Container widths: `--sm` 42rem · `--md` 52rem · `--lg` 80rem.
- Section padding: `6rem 1.5rem`.
- Border radius: **2px** everywhere. No shadows.
- Section background alternation: `--bg` / `--bg2` for rhythm.

## Hero — Ember Particles

Sparse embers drifting upward (embers escaping a fire, not a wall of fire). Replaces TGP's fire simulation; keeps the same warmth and the same two gradient overlays on top.

- ~60 particles, respawn on death
- Per particle: rise `0.3–0.8 px/frame`, horizontal drift `±0.2`, radius `1.5–3px`, life `120–200` frames
- Color `--gold` `#c4922a`, soft radial glow, alpha `0.6–0.8` fading to 0 across the top third of the rise
- Honors `prefers-reduced-motion` (single static frame, no loop)
- Two gradient overlays (copied verbatim from TGP hero): linear top→middle→bottom + radial bottom vignette

## Motion

- Keynote counter: count-up 0 → `KEYNOTE_COUNT` (easeOutCubic, ~1.5s); snaps to final under reduced-motion.
- Nav: gains background + bottom border after 40px scroll.
- Button hover: `--gold` → `--gold-h`, 200ms. No scale, no shadow.

## Source of Truth

Built directly on `/Users/gallifrey/madscience/thegatheringplace/index.html`. When TGP's tokens change, mirror them here.
