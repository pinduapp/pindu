# Pindu website

This repo is the public website for the Pindu iPhone app, served by GitHub Pages at
https://pinduapp.github.io/pindu/. It stays public and separate from the private app repo
`pinduapp/pindu-ios`, because Pages builds the address from this repo's name.

## Rules

- **Never commit to `main` directly.** Work on a branch and open a pull request for the owner
  to merge.
- **Plain static HTML and CSS, no build step, no JavaScript.** Pages must work as plain files.
- **No analytics, trackers, third-party scripts, or external fonts.** The site makes the same
  promise the app does: nothing is collected. Images and styles are served from this repo.
- **These two paths must keep working exactly as they are**, because App Store Connect points
  at them: `/pindu/privacy.html` and `/pindu/support.html`. Do not rename or move them.
- **Keep light and dark mode.** Accent colour is `#4651B0` in light mode and `#A2ABF2` in dark
  mode, matching the app. Shared styles live in `assets/site.css`.
- **Positioning.** Lead with "You can already speak it. Now you can read it." Pindu is for people
  who can speak Chinese but were never taught to read it. Do not frame it as a learn-Mandarin
  app or a traveller app. No lessons, flashcards, streaks, or tutors.
- **Keep the privacy page wording stable.** It is the text App Store Connect links to. Restyle
  freely, but change the words only when the owner asks, and update the "Last updated" date
  when you do.
- **Do not put the owner's name on the site.** The About page says "Pindu is made by one person".
- **Credits must stay on the About page:** CC-CEDICT (CC BY-SA 4.0), PaddleOCR (Apache 2.0),
  ONNX Runtime (MIT), and the 字嗨注音標楷 font by But Ko (CC BY 4.0).
- **Screenshots and the app icon come from the app repo** (`pinduapp/pindu-ios`, under
  `marketing/raw/`, `marketing/design/`, and the Xcode asset catalog). Copy and shrink them into
  `assets/img/`; do not edit the originals here. Keep each image under about 100 KB.
- **The App Store badge** in `assets/img/app-store-badge.svg` is Apple's official artwork. Do not
  redraw or recolour it.

## Things that change over time

- **Launch state.** The hero button in `index.html` has two blocks: a "pre-launch" block that is
  live, and a "launch" block inside an HTML comment. At launch, delete the pre-launch block, move
  the launch block out of the comment, and replace `APP_STORE_URL` with the real link.
- **Premium price.** The price appears in two places: the Premium section of `index.html` and the
  Premium question in `support.html`. Change both together.
- **Free allowances.** 10 free Closer Looks and 10 free saves are mentioned on the home page and
  the Help page.

## Working with the owner

The owner is not a programmer. Explain changes in plain language, give one recommendation rather
than a menu of options, and say exactly which file and which words changed.
