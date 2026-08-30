IMAGE CONVENTIONS — APPLY TO EVERY NEW IMAGE
===========================================
FILENAME   Keyword slug matching the page it serves, e.g. wood-retaining-walls.jpg,
           areas/sherman-oaks.jpg. The filename is itself a ranking signal.

FORMATS    Always ship three: .avif, .webp, .jpg — referenced through <picture>
           with the .jpg as the <img> fallback. Browsers pick AVIF > WebP > JPG.

SIZES      Hero      1100px wide (raise to 1800 when a bigger source exists)
           Type card  800 x 500  (16:10, ~2x the rendered card)
           Body slot 1600 x 900  (16:9)
           Area card 1000 x 800  (5:4)

QUALITY    Cards/body: avif q46 · webp q74 · jpg q78 — lands ~40/90/110 KB.
           Hero: avif q60 · webp q80 · jpg q82 (above the fold, worth the bytes).

ALT        Describes what is actually in the photo AND carries the page's target
           keyword. Never keyword-stuffed, never a bare keyword. Example:
             "Poured concrete retaining wall with a board-formed face curving along
              a driveway on a Los Angeles hillside property"

TITLE      A short label, NOT a copy of the alt — some screen readers announce both,
           and duplicate text is read twice. Example: "Concrete retaining wall in
           Los Angeles".

LOADING    Below the fold: loading="lazy" decoding="async".
           Hero: fetchpriority="high", never lazy.
           Always set width and height so the layout doesn't shift.

FALLBACK   Type cards keep their SVG illustration underneath the photo
           (svg z-index 1, picture z-index 2) with onerror removing the <picture>.
           A missing or failed image degrades to the illustration, never to a
           broken-image icon.

HONESTY    Alt text must not claim a photo shows your completed work in a specific
           neighbourhood unless it actually does. Area-card alt is phrased as
           descriptive, not as a claim of a finished job at that address.

HERO IMAGE — INSTALLED
======================
hero-hillside-wall-1100.{jpg,webp,avif}  1100 x 733

Wired into index.html and areas/*/index.html via <picture> with srcset.
Browsers pick AVIF > WebP > JPG. Focal point set to 62% 62% so the terraces
stay in frame while the sky and hills sit under the headline.

Sizes: avif 113 KB · webp 133 KB · jpg 188 KB

NO 2x FILE YET. The source supplied was 1100px wide, so there is nothing to
build an 1800px variant from — upscaling would add bytes without adding
detail. The srcset lists only the 1100px candidate, which is correct: a
srcset must never claim a width it cannot deliver.

To add the 2x set later: drop a >=1800px original in here and re-run the
resize, then restore the "hero-hillside-wall.{ext} 1800w" candidates and the
width="1800" height="1200" attributes in index.html and every area page.

SERVICE PAGE HERO
=================
Filename:  hero-installation.jpg  (+ .webp / .avif)
Size:      2400 x 1050, under 300 KB
Subject:   A newly built wall, ideally mid-build or freshly finished, wall weighted
           to the RIGHT of frame. Same fallback behaviour as the homepage hero.

AREA CARD IMAGES  (/img/areas/)
===============================
Filenames match the URL slug: sherman-oaks.jpg, studio-city.jpg, encino.jpg,
woodland-hills.jpg, pasadena.jpg, glendale.jpg, burbank.jpg,
la-canada-flintridge.jpg, los-feliz.jpg, silver-lake.jpg, highland-park.jpg,
beverly-hills.jpg, brentwood.jpg, pacific-palisades.jpg, topanga.jpg

Size:   1000 x 800 (5:4), under 120 KB each
Subject: a completed wall in that neighbourhood. Shoot wide enough that the
         street or hillside context reads — the point is proving you work there.
Also:   /img/areas-overview.jpg  (1600 x 1000) for the section intro.

Cards render an illustrated terrace fallback until the file exists, so partial
coverage is fine — add photos neighbourhood by neighbourhood as you shoot them.

SERVICE PAGE PHOTO SLOTS  (/img/services/installation/)
=======================================================
Each slot renders a dashed placeholder showing its own filename until the file
exists. Drop the .jpg in and it takes over — no code change.

what-are-retaining-walls.jpg   Finished tiered wall on a hillside, shot along the run
how-installed.jpg              Mid-build: gravel, filter fabric and drain pipe going in
when-you-need.jpg              Before-shot: eroding slope or failing older wall
/img/areas-overview.jpg        Wide shot in a recognisable LA hillside neighbourhood

Size: 1600 x 900 (16:9), under 250 KB each.
Area cards under /img/areas/ are listed further up this file.
