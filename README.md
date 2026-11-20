# flowline-site

Public website for **Flowline: Lava Island Puzzle**, a premium puzzle-strategy game for iPhone.
*Steer the lava. Settle the new land.*

Live at <https://jakeintech.github.io/flowline-site/> (GitHub Pages, from `main` /).

| Page | URL |
|---|---|
| Home (App Store marketing URL) | `/` |
| Support and FAQ (App Store support URL) | `/support.html` |
| Privacy Policy (App Store privacy URL) | `/privacy-policy.html` |
| Terms of Use | `/terms-of-service.html` |

Keep the support, privacy and marketing URLs exactly as they are: App Store Connect (app id 6837022564) points at them.

## How it is built

Plain HTML and one stylesheet (`assets/site.css`), the same structure as the Night Signal site. No build step and no third-party requests: fonts and images are served from this repo, and there are no analytics, cookies or CDNs.

- **Type:** Space Grotesk (Medium 500, Bold 700), the game's typeface, self-hosted as TTF in `assets/fonts/` with its SIL Open Font License text.
- **Colour:** the game's palette from `Flowline/Board/Palette.swift`: sea navy `#0A1F2E`, lava `#FF8A1F`, lava front `#FFC23A`, preview cyan `#62E4FF`, land green `#9DF0BF`, text white and `#B9CBD8`. Dark in every theme, like the game. Every text pairing meets WCAG AA.
- **Accessibility:** skip link, landmarks, alt text, 44 px targets, visible focus, smooth scrolling only without `prefers-reduced-motion`. Mobile first.
- **Honesty:** the copy says what the game does. The screenshot is a real capture from the iOS Simulator.

## What is generated

| Output here | Source in the Flowline repo (`~/Developer/GitHub/Flowline`) |
|---|---|
| `assets/img/icon-512.png`, `icon-192.png`, `apple-touch-icon.png`, `favicon.png`, `assets/press/flowline-icon-1024.png` | `swift scripts/make-icon.swift` |
| `assets/img/shot-island-1-{1434,717}.png` | `docs/screenshot-island-1.png` |
| `assets/img/og.png` | drawn with PIL from the icon and the tagline |
