# Design system · Clear Glass

**Thesis:** *It should feel like looking through something, not at something.* The concept is about room and lightness, so the visuals are mostly air: pale backgrounds, thin lines, and colour that glows rather than fills.

## Palette

Defined once in [`assets/tokens.json`](../assets/tokens.json). `scripts/check-contrast.mjs` checks every text pairing against WCAG 2.2 AA on each push.

| Token | Hex | Use | Contrast |
|---|---|---|---|
| `bg` | `#F4F5F8` | Page background, "frosted" panels | — |
| `surface` | `#FFFFFF` | Cards | — |
| `line` | `#DDE0E8` | Hairlines and borders | decorative only |
| `ink` | `#101218` | Headings and body text | 17.2:1 on `bg` |
| `ink2` | `#4A505E` | Secondary text | 7.4:1 on `bg` |
| `accent` | `#4338CA` | Links, buttons, key numbers ("Spatial Indigo") | 7.3:1 on `bg` |
| `onAccent` | `#FFFFFF` | Text on accent | 7.9:1 |
| `glowBlue` / `glowViolet` | `#7DB4FF` / `#B8A2FF` | Soft gradients behind content | decorative only, never text |

**Rule:** the glows never carry information. Anything that matters is written in `ink` or `accent`.

## Type

- System sans (`-apple-system`, `SF Pro`, then `Helvetica Neue`, Arial). On Apple devices it renders as SF Pro, the type the audience already associates with the brand, with nothing to download.
- Headlines: 600 weight, tight tracking (-0.02em). Body: 400 weight, 1.6 line height.
- Sizes in `rem` with `clamp()` for headlines, so text scales with the reader's settings.

## Shape and space

- 8px spacing grid. Cards: 20px radius, 1px `line` border, no shadow. Lightness means no heavy drop shadows.
- Graphics use circles and rounded rectangles only: soft geometry, like the device.

## Graphics

| File | Shows |
|---|---|
| `assets/banner.svg` | Project banner: the name over a frosted glass panel with indigo and blue glows |
| `assets/personas.svg` | The three persona cards |
| `assets/messaging-house.svg` | Umbrella message, three pillars, proof foundation |
| `assets/gtm-timeline.svg` | The four launch phases on a June–December timeline |

Each SVG has a `<title>` and `<desc>`, and its content is also written out in the matching document.
