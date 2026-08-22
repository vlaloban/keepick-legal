# Keepick — site

Public site for [Keepick: Photo Cleaner](https://apps.apple.com/app/id6800228517),
an iPhone app that finds similar photos and helps you clean your library. All
photo analysis runs on-device.

Published via GitHub Pages: **https://vlaloban.github.io/keepick-legal/**

| Page | What it is |
|---|---|
| [`index.html`](https://vlaloban.github.io/keepick-legal/) | Product page: what the app does, the three passes, real screens, the App Store preview |
| [`press.html`](https://vlaloban.github.io/keepick-legal/press.html) | Press kit: fact sheet, copy blocks, downloadable assets. Linked from the App Store featuring nomination |
| [`support.html`](https://vlaloban.github.io/keepick-legal/support.html) | The App Store "Support URL" for the app record |
| [`privacy.html`](https://vlaloban.github.io/keepick-legal/privacy.html) | Privacy Policy — also the App Store "Privacy Policy URL" |
| [`terms.html`](https://vlaloban.github.io/keepick-legal/terms.html) | Terms of Use |

**The last three URLs are filed with Apple and must not move.** They are wired
into the app record in App Store Connect; renaming a file breaks a link the
review process checks.

## Assets

`assets/` holds everything the press kit hands out. Nothing here is generated at
build time — the files are produced in the app repo and copied over:

| File | Source |
|---|---|
| `screens/full/*.png` | `Marketing/AppStore/cards/en-US/` — the App Store set, 1290×2796 |
| `screens/*.jpg` | the same cards, resized to 760 px for the page |
| `app/*.jpg` | `Marketing/AppStore/shots/` — raw screens, no marketing copy on them |
| `rail.jpg` | crop of `shots/from-phone/IMG_1083.PNG`: one pack of eight near-identical frames |
| `keepick-preview.mp4` | `Marketing/AppStore/preview-2-886x1920.mp4`, the App Store preview |
| `keepick-press-kit.zip` | `zip -j` of the full-res screenshots plus the icon |

The product page shows **raw app screens**, not the App Store cards: the cards
carry their own headline, and two headlines side by side fight each other. The
cards live in the gallery, where they are labelled as the App Store set.

**No recognisable children's faces on this site.** The rule comes from the app
repo and holds here for the same reason: the pages get mirrored and cannot be
recalled. That is why the hero uses `review-no-people`, the pack strip is the
aquarium (silhouettes, from behind), and the "On this day" screen is the one
with clouds.

## Style

One stylesheet for all five pages. The palette is the App Store listing's —
deep teal `#0C4F45`, turquoise `#22D3C5` — chosen there because the competitors'
shelf is uniformly light and cold. Type has three roles: Fraunces for anything
about photographs, Karla for text, JetBrains Mono for machine facts (passes,
sizes, dates). Both light and dark are defined; the site follows the visitor's
system setting.

## Local preview

    python3 -m http.server 8899

Contact: main@3vlbn.com
