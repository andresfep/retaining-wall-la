# Retaining Wall Contractor Los Angeles — Cloudflare Pages bundle

Static site, no build step, no dependencies.

```
/
├── index.html      Homepage (H1: Retaining Wall Contractor in Los Angeles, CA)
├── 404.html
├── logo.svg        Full horizontal lockup (mark + wordmark)
├── img/            Hero photo goes here — see img/README.txt
├── favicon.svg
├── robots.txt
├── sitemap.xml
├── _headers
└── _redirects
```

## Deploy
1. Push to a GitHub repo.
2. Cloudflare → Workers & Pages → Create → Pages → connect repo.
3. Framework preset **None**, build command **empty**, output directory **/**.
4. Custom domains tab → add apex + www. `_redirects` forces www → apex.

## Brand palette (locked)

| Token | Hex | Use |
|---|---|---|
| Navy 900 | `#0B1721` | Page base, footer, dark sections |
| Navy 800 | `#12232F` | Cards on dark, hero gradient top |
| Navy 700 | `#1B3040` | Borders on dark |
| Green | `#2E6B4F` | Eyebrows, icons, secondary buttons |
| Green light | `#4A8F6B` | Gradient partner, logo slope |
| Gold | `#D4A62A` | **All primary buttons**, accents, logo courses |
| Gold light | `#EFC44B` | Button gradient top, headings on dark |
| Gold dark | `#A87F17` | Link text on light, button shadow |
| Cream | `#F7F4EC` | Trust strip |
| Paper | `#FBFAF8` | Alternating section background |
| Stone | `#E8E3D7` | Illustration backgrounds |
| Line | `#DCD6C7` | All borders on light |

Type: **Barlow Semi Condensed ExtraBold (800)** for display — H1, section headings,
card titles, brand wordmark, all uppercase with slight negative tracking — paired with
**Barlow (400–700)** for body copy. One family, two widths.

Loaded from Google Fonts in a single request:
`family=Barlow:wght@400;500;600;700&family=Barlow+Semi+Condensed:wght@600;700;800`

To revert display headings to sentence case, remove `text-transform:uppercase` from
`h1`, `h2.sec`, `article h2`, `.h2sub`, `.final h2` and `.acard-title`.

## Swapping in your own Google Map

The homepage "near me" section embeds a map using the keyless format:

`https://maps.google.com/maps?q=Los%20Angeles%2C%20CA&z=10&output=embed`

A `share.google/...` link is a *share* link, not an embed link — it will not work in an
iframe. To use your real Business Profile pin instead:

1. Open the location in Google Maps.
2. **Share** → **Embed a map** tab (not "Send a link").
3. Copy the `src="https://www.google.com/maps/embed?pb=..."` value only.
4. Replace the `src` on the `<iframe>` in `index.html`. Keep the existing
   `title`, `loading="lazy"` and `referrerpolicy` attributes — they matter for
   accessibility and for keeping the map off the critical render path.

Note the map does not need to show a street address. A service-area business can point
the pin at the city or draw the coverage area.

## Before launch
- Decide the business name. Currently "Hillside Stoneworks" in the header, footer, and schema — search and replace in `index.html`.
- Replace `(323) 555-0142` with the real number (appears in topbar, hero, NAP block, final CTA, and schema).
- Replace `CSLB #0000000` with the real licence number in the topbar, NAP block, and footer.
- Replace all cost ranges with the contractor's real numbers. Wrong pricing generates unqualified calls.
- Verify permit thresholds per jurisdiction (City of LA, County, Pasadena, Glendale all differ). Currently hedged in the FAQ and footer.
- Project descriptions are illustrative — swap for real jobs with real photos. Fabricated project claims are an FTC issue.
- Add `/privacy/` and `/terms/` (footer links to both) and a `/contact/` page.
## Hero photo

The hero is built for a photograph. Until one exists at `/img/hero-hillside-wall.jpg`,
an illustrated fallback renders in its place — when you add the file it takes over
automatically, no code change needed.

**Specs:** 2400 x 1350 (16:9), under 300 KB compressed, wall weighted to the RIGHT
of frame with open sky/space on the LEFT where the headline sits. Supply `.avif` and
`.webp` alongside the `.jpg` if you can; the markup already prefers them.

**Sourcing:**
- Unsplash (unsplash.com/s/photos/retaining-wall) — free for commercial use, no attribution required, but a thin selection.
- Pexels — same licence terms, worth checking alongside Unsplash.
- Adobe Stock / iStock — far better selection of hillside and terraced walls if you'll pay.
- Best option: photograph a real completed job. LA hillside light in the late afternoon, shot along the wall so it runs into the frame.

Never pull an image from Google Images or a competitor's site. Contractor photos are
routinely watermarked and rights-holders in this space do send demand letters.

- Photography is the single biggest upgrade available. Real before/after hillside shots convert far better in this trade than any illustration.
