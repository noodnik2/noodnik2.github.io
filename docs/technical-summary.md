# Repository Summary (as of 2026-08-09)

This is a static, no-build-step GitHub Pages site (noodnik2.github.io) based on the HTML5 UP "Forty" 
template — plain HTML5/CSS/jQuery, with no Jekyll, bundler, or templating engine.
Each page is a standalone, hand-copied .html file.

## Page Structure

Every live page (index.html, side-projects.html, adventures.html, older-investigations.html) repeats the same skeleton:

- &lt;div id="wrapper"&gt;
  - &lt;header id="header" class="alt[ styleN]"&gt;
  - &lt;nav id="menu"&gt; — identical four links duplicated on every page: Home, Resume (PDF), Side Projects, Adventures
  - &lt;section id="banner"&gt; — its styleN class must match the header's
  - &lt;div id="main"&gt; — one or more &lt;section&gt; blocks:
      - plain id="one" content sections, or
    - grid sections using class="tiles" / class="spotlights", each built from repeated &lt;article&gt;/&lt;section&gt; + &lt;span class="image"&gt; +
  &lt;header class="major"&gt; + &lt;div class="content"&gt; / &lt;div class="indent"&gt;
    - &lt;footer id="footer"&gt; — shared GitHub/LinkedIn icons + copyright line

## Assets

- Stylesheet: assets/css/main.css (plus assets/css/noscript.css fallback); SCSS source lives in assets/sass/ if recompilation is ever
  needed
- Scripts, loaded in this fixed order from assets/js/: jquery.min.js → jquery.scrolly.min.js → jquery.scrollex.min.js → browser.min.js
  → breakpoints.min.js → util.js → main.js
- Images: /images/
- Downloadable files (resumes, PDFs): /static/

## Template scaffolding files

__generic__.html, __landing__.html, __elements__.html are the original Forty template's unused boilerplate/reference pages (confirmed:
not linked from anywhere in the site) — kept around as scaffolding for building new pages, not live content.

## Exception: firesafehome/

A self-contained Vite-built React PWA (own manifest, service worker, hashed JS/CSS bundle) mounted as an isolated subdirectory. It does
not share the Forty template's markup or CSS — treat it as an independent app, not a pattern to replicate.

## Guidance for adding new pages

1. Copy an existing page (e.g. side-projects.html) as a starting template.
2. Preserve the wrapper/header/nav/banner/main/footer skeleton.
3. Add the new page to the shared nav list on every existing page.
4. Reuse existing CSS classes from main.css (tiles, spotlights, major, indent, actions, button) rather than inventing new ones.
5. Place new images in /images/ and new downloads in /static/.

Note: adventures.html currently has an uncommitted, work-in-progress edit (a commented-out YouTube embed) — not a finished pattern,
just local in-progress work.
