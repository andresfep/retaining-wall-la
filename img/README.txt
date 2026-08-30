HERO IMAGE — INSTALLED
======================
hero-hillside-wall.{jpg,webp,avif}       1800 x 1200  (2x)
hero-hillside-wall-1100.{jpg,webp,avif}  1100 x 733   (1x)

Wired into index.html via <picture> with srcset. Browsers pick AVIF > WebP > JPG
and the 1100px file on narrow screens. Focal point set to 62% 62% so the terraces
stay in frame while the sky and hills sit under the headline.

Source was 1208px wide, so 1800px is the practical ceiling — upscaling further adds
file size without adding detail. If you get a higher-resolution original, re-run at
2400px wide and keep the JPG under ~300 KB.

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
