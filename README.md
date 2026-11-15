# 🧪 SVG lab (WeebProfile)

Temporary tests: what GitHub lets an image in a README do. Files in [`lab/`](lab).

## Part 1 · Several links in one "image"

**1a.** Two `<a>` elements inside the SVG (click one of the buttons):

<img src="lab/12-links-inside.svg" alt="links inside the svg">

**1a'.** The same file from an external host (camo). Click it: GitHub opens the SVG in a new tab, where the buttons work:

<img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/12-links-inside.svg" alt="links inside the svg via camo">

**1b.** Two files glued together, each with its own `<a>` and `title` (fixed width of 415px each):

<p><a href="https://weebprofile-dashboard.pages.dev" title="WeebProfile"><img src="lab/13-split-left.svg" width="415" alt="WeebProfile"></a><a href="https://heartopia.guide" title="Heartopia Guide"><img src="lab/13-split-right.svg" width="415" alt="Heartopia Guide"></a></p>

**1c.** The same, with `width="50%"`:

<p><a href="https://weebprofile-dashboard.pages.dev" title="WeebProfile"><img src="lab/13-split-left.svg" width="50%" alt="WeebProfile"></a><a href="https://heartopia.guide" title="Heartopia Guide"><img src="lab/13-split-right.svg" width="50%" alt="Heartopia Guide"></a></p>

**1d.** Stacked vertically (checks the gap between the lines):

<p><a href="https://weebprofile-dashboard.pages.dev"><img src="lab/13-split-left.svg" width="415"></a><br><a href="https://heartopia.guide"><img src="lab/13-split-right.svg" width="415"></a></p>

## Part 3 · Animation

| # | Technique | Result |
|---|---|---|
| 01 | CSS `@keyframes` | <img src="lab/01-css-keyframes.svg"> |
| 02 | SMIL | <img src="lab/02-smil.svg"> |
| 03 | Typing | <img src="lab/03-typing.svg"> |
| 04 | Carousel | <img src="lab/04-carousel.svg"> |
| 05 | Odometer | <img src="lab/05-odometer.svg"> |
| 06 | `<script>` | <img src="lab/06-script.svg"> |
| 07 | `:hover` | <img src="lab/07-hover.svg"> |
| 08 | foreignObject | <img src="lab/08-foreignobject.svg"> |
| 09 | GIF inside the SVG | <img src="lab/09-gif-inside-svg.svg"> |
| 10 | External `<image>` | <img src="lab/10-external-image.svg"> |
| 11 | `prefers-color-scheme` | <img src="lab/11-prefers-color-scheme.svg"> |
| — | Plain GIF | <img src="lab/anim-frames.gif"> |
| — | Animated WebP | <img src="lab/anim.webp"> |

**External host (goes through GitHub's camo proxy, like WeebProfile's SVGs do):**

<img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/01-css-keyframes.svg" alt="css via camo">
<img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/02-smil.svg" alt="smil via camo">
<img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/03-typing.svg" alt="typing via camo">

## Embed snippet (dashboard)

Snippets as the dashboard now copies them, pointing at two real half cards.

**4a.** Two halves, the "Side by side" snippet (`width="50%"`, tags glued):

<p align="center" id="lab-4a"><img align="top" width="50%" alt="MyAnimeList Stats" src="https://weebprofile-dashboard.pages.dev/svg/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg" /><img align="top" width="50%" alt="GitHub Stats" src="https://weebprofile-dashboard.pages.dev/svg/ea02df1e-d680-4150-9d58-0c8324850fea.svg" /></p>

**4b.** Three halves, same snippet (two on the first row, one on the second):

<p align="center" id="lab-4b"><img align="top" width="50%" alt="MyAnimeList Stats" src="https://weebprofile-dashboard.pages.dev/svg/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg" /><img align="top" width="50%" alt="GitHub Stats" src="https://weebprofile-dashboard.pages.dev/svg/ea02df1e-d680-4150-9d58-0c8324850fea.svg" /><img align="top" width="50%" alt="MyAnimeList Stats" src="https://weebprofile-dashboard.pages.dev/svg/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg" /></p>

**4c.** One half alone, the per-card snippet (no `width`):

<p align="center"><img align="top" alt="MyAnimeList Stats" src="https://weebprofile-dashboard.pages.dev/svg/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg" /></p>

**4d.** Baseline, one half alone with `width="50%"`:

<p align="center"><img align="top" width="50%" alt="MyAnimeList Stats" src="https://weebprofile-dashboard.pages.dev/svg/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg" /></p>

**4e.** Baseline, two halves glued without `width` (what combining the old snippets gave):

<p align="center"><img align="top" alt="MyAnimeList Stats" src="https://weebprofile-dashboard.pages.dev/svg/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg" /><img align="top" alt="GitHub Stats" src="https://weebprofile-dashboard.pages.dev/svg/ea02df1e-d680-4150-9d58-0c8324850fea.svg" /></p>

**4f.** Baseline, two halves at `width="50%"` with a line break between the tags:

<p align="center">
  <img align="top" width="50%" alt="MyAnimeList Stats" src="https://weebprofile-dashboard.pages.dev/svg/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg" />
  <img align="top" width="50%" alt="GitHub Stats" src="https://weebprofile-dashboard.pages.dev/svg/ea02df1e-d680-4150-9d58-0c8324850fea.svg" />
</p>

## Auto theme (light/dark)

One SVG with both palettes: the light one by default, the dark one inside `@media (prefers-color-scheme: dark)`. It should follow GitHub's theme, not the OS.

**5a.** Terminal, auto, from the repo:

<p id="lab-5a"><img src="lab/14-auto-terminal.svg" alt="auto terminal"></p>

**5b.** The same file through camo (how WeebProfile's cards are served):

<p id="lab-5b"><img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/14-auto-terminal.svg" alt="auto terminal via camo"></p>

**5c.** Terminal dracula, auto, through camo:

<p id="lab-5c"><img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/14-auto-terminal-dracula.svg" alt="auto dracula via camo"></p>

**5d.** Default style, purple, auto, through camo (transparent card: text and accent change):

<p id="lab-5d"><img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/14-auto-default-purple.svg" alt="auto default purple via camo"></p>

**5e.** Control, terminal without auto (always dark):

<p id="lab-5e"><img src="https://cdn.jsdelivr.net/gh/LucasHenriqueDiniz/LucasHenriqueDiniz@main/lab/14-fixed-terminal.svg" alt="fixed terminal via camo"></p>

---

<p align="center">
  <img align="top" alt="Myanimelist Stats" src="https://pub-25de70ed316a4aebacfedae6e26b4a87.r2.dev/svgs/c69bcae6-e43f-4eea-8e6f-77e82c80553f.svg?v=1784672385375" />
</p>

<sub>The above images are generated using [LucasHenriqueDiniz/WeebProfile](https://github.com/LucasHenriqueDiniz/WeebProfile)</sub>
