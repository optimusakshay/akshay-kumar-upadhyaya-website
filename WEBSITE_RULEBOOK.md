# Akshay Kumar Upadhyaya Website Rulebook

**Purpose:** This document is the technical, editorial, visual, and operational specification for rebuilding, maintaining, and troubleshooting the website without relying on the original chat.

**Current live site:** `https://optimusakshay.github.io/akshay-kumar-upadhyaya-website/`

**Repository:** `optimusakshay/akshay-kumar-upadhyaya-website` on GitHub, branch `main`.

**Local project root:** `D:\Pragya\Website_Material\Website`

**Project materials root:** `D:\Pragya\Website_Material`

---

## 1. Project identity and design intent

This is a static personal/research website for Akshay Kumar Upadhyaya. The site presents first-person professional and creative work related to wildlife research, primate ecology, biodiversity conservation, GIS and spatial analysis, human–wildlife interactions, conservation outreach, photography, writing, and music.

The website must feel:

- calm, editorial, and field-oriented;
- professional but personal;
- visually restrained rather than flashy;
- image-led, with real supplied photographs;
- readable over photographs;
- lightweight and dependency-light;
- deployable directly on GitHub Pages without a server or build system.

The site is not an application. It is a collection of ordinary HTML pages sharing one CSS file and one JavaScript translation file.

---

## 2. Non-negotiable editorial rules

1. Use first-person wording: `I am`, `My work`, `I have worked`, and similar forms.
2. Do not describe Akshay in third person in visible site copy.
3. Do not invent credentials, awards, institutions, dates, locations, statistics, species, outcomes, job titles, or affiliations.
4. Use only verified supplied facts and supplied images.
5. Preserve exact user-provided wording when a correction gives replacement wording.
6. If a correction supplies key points rather than a complete sentence, write restrained professional copy without expanding the factual scope.
7. Keep scientific names in semantic italics using `<em>`, not quotation marks or image text.
8. Do not expose passwords, tokens, API keys, credentials, private contact values, private social identifiers, or sensitive URLs in code, documentation, commits, or reports.
9. Contact-page content is frozen unless the owner explicitly requests a Contact-page change. A broad CSS change must not accidentally alter its content or layout.
10. Do not remove source photographs merely because a Gallery entry is removed. Gallery duplicate cleanup removes markup entries only.

### Approved factual content currently used

- Wildlife researcher and conservation professional from Assam, India.
- Background in Wildlife Science.
- Over three years of field experience in wildlife ecology and conservation.
- Research experience with Aaranyak’s Primate Research & Conservation Division (PRCD).
- Work involving Western Hoolock Gibbon ecology and conservation across Assam and Arunachal Pradesh.
- Population surveys, call-count and acoustic monitoring, habitat assessment, GIS-based spatial analysis, and conservation planning.
- Golden Langur population assessment.
- Human–macaque interactions in Guwahati, including the Basistha Temple study context.
- Master’s dissertation on butterfly diversity and abundance in Bhairabkunda Reserve Forest, Assam.
- More than 4000 students reached through conservation education, as supplied for the About highlights.
- Creative practice involving wildlife photography, conservation communication, writing, and music.
- Author of *Optimus Rhymes: A Flat-Footed Journey*.

If a future correction conflicts with this list, the newest explicit owner correction controls that specific item.

---

## 3. File and folder structure

```text
D:\Pragya\Website_Material\
├── Website\                         # Git working tree and deployable site
│   ├── index.html                    # Homepage
│   ├── about.html                    # Full biography and creative practice
│   ├── research.html                 # Research hero, topics, methods, skills
│   ├── outreach.html                 # Outreach stories and training list
│   ├── gallery.html                  # Photos-only Gallery
│   ├── contact.html                  # Frozen contact page
│   ├── resources.html                # Existing resources page
│   ├── fieldwork.html                # Existing fieldwork page
│   ├── styles.css                    # Shared visual system and responsive rules
│   ├── translations.js               # Offline language-switching logic/dictionaries
│   ├── photos/                       # Supplied image assets and logo
│   ├── resources/                    # Supplied PDFs and resource images
│   └── README.md                     # Repository-level notes, if present
├── Website_Version_Links.txt         # Local clickable version index
├── Website_Versions/                 # Immutable ZIP snapshots
├── Corrections_Needed/               # Incoming screenshots/assets; not deployed
└── WEBSITE_RULEBOOK.md               # This document
```

The website has no package manager requirement, no bundler, and no framework. Do not introduce React, Vue, a CSS framework, or a server-side dependency unless explicitly requested.

---

## 4. Page map and responsibilities

### `index.html` — Homepage

The homepage intentionally contains only the main hero and global navigation/footer. The former green About summary section was removed in the latest correction. Do not re-add it unless explicitly requested.

Current hero components:

- shared header and navigation;
- supplied logo `photos/Logo-transparent.png`;
- eyebrow containing professional fields and IUCN CEM dates;
- hero title: `Reading the forest, sharing its stories.`;
- concise first-person summary;
- `Explore the work` CTA;
- `A little about Akshay` link to `about.html`;
- supplied hero image `photos/phot.JPG`;
- field-notes caption;
- footer.

Important: `Explore the work` currently targets `#research`. If the homepage does not contain a research anchor, inspect this before changing it. A future maintainer may change it to `research.html` if the owner wants a direct page link.

### `about.html` — Full About page

This is the detailed biography page. It contains:

- hero image using `photos/phot.JPG`;
- hero name `Akshay Upadhyaya`;
- professional keyword line;
- large editorial lead heading;
- four compact profile highlights;
- full research and education copy;
- supporting supplied photographs;
- PhotoGallery CTA;
- creative-practice paragraph and book link;
- image lightbox controls;
- YouTube media card;
- footer.

The four highlight facts are marked with `.about-facts` and should remain compact and responsive:

1. `3+ years` — Wildlife Research & Conservation
2. `Primarily` — Western Hoolock Gibbon, Golden Langurs, Macaques of Assam
3. `Assam & Arunachal Pradesh` — Field Research Experience
4. `4000+` — Students Reached Through Conservation Education

### `research.html` — Research page

The Research page contains:

- image hero with class `.research-page-hero`;
- current heading: `Primates in today’s world: habitats, threats, and human bonds.`;
- supporting research sentence;
- Western Hoolock Gibbon topic;
- Human–macaque interactions topic;
- Golden Langur fieldwork topic;
- habitat, butterfly, and overlooked-life topic;
- research images and habitat collage;
- tools and skills section.

Current important images:

- Western Hoolock Gibbon: `photos/IMG_4523.JPG.jpeg`
- Human–macaque: `photos/IMG_1758.JPG (1).jpeg`
- Golden Langur: `photos/IMG_9339-01.jpg.jpeg`
- butterfly/habitat assets: inspect current markup before replacing.

### `outreach.html` — Outreach page

The Outreach page contains:

- centered conservation hero;
- Wildlife Observation Event story;
- awareness/frontline forest-staff training story;
- Workshops & Training section;
- compact wrapped list rather than seven vertically stacked cards.

The training list uses `.clean-list` and separators. Do not convert it back to a tall list unless the owner requests that design.

Important Outreach assets include `photos/IMG_4143.JPG.jpeg`, `photos/IMG_4144.JPG.jpeg`, and the current hero asset `photos/IMG_0508.JPG.jpeg`. Verify exact spelling on disk before changing paths.

### `gallery.html` — Photos-only Gallery

Gallery is a separate top-level navigation page. It displays photographs only; captions were intentionally hidden for the photos-only treatment. There are currently 54 unique displayed entries after duplicate markup removal. Source image files remain in `photos/`.

When deduplicating:

1. parse Gallery markup;
2. detect repeated source paths;
3. compare visually similar files when filenames differ;
4. remove repeated markup entries only;
5. preserve the first intentional occurrence and underlying source files;
6. verify image loading and count.

### `contact.html` — Frozen page

Do not modify Contact content, image, placement, or page-specific treatment without explicit approval. Before publishing any batch, run:

```bash
git diff -- contact.html
```

An empty diff is required unless Contact was explicitly included in the request.

### `resources.html` and `fieldwork.html`

These are existing static pages in the repository. Preserve their current structure and links unless a future correction specifically targets them. They must still return HTTP 200 and remain navigable if linked.

---

## 5. Shared header and navigation

Every page should use the same general header pattern:

- logo link;
- About;
- Research;
- Outreach;
- Gallery;
- Contact;
- Translate control;
- prominent `Get my Book` CTA.

The logo is the supplied static asset `photos/Logo-transparent.png`. Do not recreate the logo with CSS or text.

Use relative links for internal pages:

```html
<a href="about.html">About</a>
<a href="research.html">Research</a>
<a href="outreach.html">Outreach</a>
<a href="gallery.html">Gallery</a>
<a href="contact.html">Contact</a>
```

Use `target="_blank" rel="noreferrer"` for approved external links. Do not place private destinations into public source.

If CSS changes are made, update the stylesheet cache-busting query consistently, for example:

```html
<link rel="stylesheet" href="styles.css?green-surfaces=8">
```

A query-string change is useful when testing browser/CDN cache behavior, but it is not a substitute for checking the actual deployed source.

---

## 6. Visual system

### Palette

The visual system is restrained olive and cream:

- deep olive for primary text and dark sections;
- pale cream/pale olive for backgrounds;
- mid olive for accents and CTA surfaces;
- muted green-gray for supporting text;
- semi-transparent dark overlays on photographs.

Current CSS tokens are defined at the top of `styles.css` under `:root`. Reuse those tokens rather than adding arbitrary colors.

### Typography

- Serif display font: Libre Baskerville, with Georgia fallback.
- Sans-serif interface/body font: DM Sans, with Arial fallback.
- Large headings use fluid `clamp()` sizes.
- Long hero statements must have a constrained text width and comfortable line-height.
- On narrow screens, reduce heading size deliberately; never rely on clipping.

### Spacing

Use the existing clamp-based spacing system. The site should have breathing room but must not create huge empty bands. Diagnose compounded padding/margins before changing shared rules.

### Photography

- Never distort image proportions.
- Use `object-fit: cover` only when cropping is acceptable.
- Use `object-fit: contain` for certificates, documents, and images where the whole subject must remain visible.
- Keep text over images readable using overlay and contrast.
- Inspect hero crops at desktop and narrow widths after changes.

---

## 7. Offline translation system

`translations.js` implements a browser-only translation layer. There is no translation API and no credential requirement.

Core behavior:

1. dictionaries are defined in JavaScript;
2. a `TreeWalker` visits body text nodes;
3. original node values are retained in a `WeakMap`;
4. each language switch restores the original English node text before applying the next dictionary;
5. selected language is stored in `localStorage` under `site-language`;
6. the selected language persists across page navigation;
7. language buttons update `aria-pressed`.

Supported language codes:

- `en` — English
- `ne` — Nepali
- `hi` — Hindi
- `as` — Assamese

When adding visible English copy, update all requested dictionaries. Translation keys are normalized for whitespace, but inline links and emphasis require care: translate text nodes, not complete HTML blocks. Never replace an entire paragraph if it would destroy an inline `<a>` or `<em>` element.

Required translation QA:

- open each page in English;
- switch to Nepali, Hindi, and Assamese;
- switch back to English;
- repeat a language change twice;
- navigate to another page and confirm persistence;
- inspect narrow viewport for wrapping and overflow;
- confirm external `href` values remain unchanged.

A future launch pass must ensure that all visible current copy, including the latest Correction3 text and the new Research header, has complete verified translations. Do not claim the localization is complete unless those keys are actually present.

---

## 8. Asset rules and filename pitfalls

Asset paths are case-sensitive on GitHub Pages even if Windows is case-insensitive. Always verify exact filenames:

```bash
find photos -maxdepth 1 -type f -print
```

If `find` is unavailable, use the file-search tool or Python. Avoid “correcting” filenames automatically. Some supplied files intentionally have derivative names such as `.jpg.jpeg` or spaces and parentheses.

For a new asset:

1. locate it recursively under `Corrections_Needed`;
2. inspect it visually if placement matters;
3. copy it into `Website/photos/`;
4. use the exact working filename in HTML;
5. add meaningful alt text based only on what the image shows;
6. verify local HTTP loading and GitHub Pages loading.

Never use stock photography when the owner supplied a real image.

---

## 9. Correction intake procedure

For each new correction batch:

1. recursively list the correction folder;
2. inspect every screenshot visually;
3. transcribe requested page, section, exact wording, image, and layout change;
4. separate exact owner wording from assistant-polished wording;
5. inspect the existing DOM to map terms such as “intro,” “header,” or “section”;
6. ask before editing if placement or wording is ambiguous;
7. create a pre-edit ZIP under `Website_Versions/`;
8. apply only confirmed changes;
9. browser-check desktop and narrow layouts;
10. update `Website_Version_Links.txt`;
11. keep the batch local until explicit publication approval;
12. only then commit, push, and verify live propagation.

Do not publish a partial correction batch merely because one screenshot was completed.

---

## 10. Local development and preview

From Git Bash on Windows:

```bash
cd 'D:/Pragya/Website_Material/Website'
python -m http.server 8765
```

Open:

```text
http://127.0.0.1:8765/index.html
http://127.0.0.1:8765/about.html
http://127.0.0.1:8765/research.html
http://127.0.0.1:8765/outreach.html
http://127.0.0.1:8765/gallery.html
http://127.0.0.1:8765/contact.html
```

Always use a cache-busting query while reviewing a just-edited page, for example:

```text
http://127.0.0.1:8765/research.html?review=latest
```

A static server is preferable to opening files directly because relative assets, navigation, and browser behavior then match deployment more closely.

---

## 11. Verification checklist

### Source checks

```bash
cd 'D:/Pragya/Website_Material/Website'
git status --short --branch
git diff --stat
git diff -- contact.html
```

### Page availability

Check every HTML page returns HTTP 200 locally and, after publishing, on GitHub Pages.

### DOM checks

Confirm:

- title and requested headings are present;
- old superseded wording is absent;
- navigation labels and destinations are correct;
- all expected image `src` values exist;
- `alt` text is present;
- no duplicate `.jpeg.jpeg` path was accidentally introduced;
- Contact remains unchanged;
- homepage does not contain the removed About section unless explicitly re-requested.

### Browser checks

At minimum inspect:

- desktop width around 1280px;
- tablet width around 768px;
- phone width around 390px;
- wide desktop if a hero or gallery is changed.

Check:

- heading wraps;
- text contrast over images;
- image proportions;
- navigation wrapping;
- CTA visibility;
- `scrollWidth <= clientWidth`;
- no console errors;
- no broken images.

### Simple browser-console expression

```javascript
JSON.stringify({
  broken: Array.from(document.images).filter(i => i.complete && i.naturalWidth === 0).length,
  overflow: document.documentElement.scrollWidth > document.documentElement.clientWidth,
  title: document.title
})
```

### Search for stale wording

When replacing copy, search for both the new and old sentence. A replacement is incomplete if the old visible sentence remains in another section, translation dictionary, or duplicate markup.

---

## 12. Versioning and backups

Every meaningful iteration must be preserved under:

```text
D:\Pragya\Website_Material\Website_Versions\
```

Recommended naming:

```text
Before_<change-description>.zip
After_<change-description>.zip
```

The local index is:

```text
D:\Pragya\Website_Material\Website_Version_Links.txt
```

Use `file:///` links in that index. Do not overwrite earlier snapshots.

To create a ZIP with Python when the `zip` utility is unavailable:

```bash
python -c "import os,zipfile; base=r'D:\Pragya\Website_Material\Website'; out=r'D:\Pragya\Website_Material\Website_Versions\Snapshot.zip'; z=zipfile.ZipFile(out,'w',zipfile.ZIP_DEFLATED); [z.write(os.path.join(dp,f),os.path.relpath(os.path.join(dp,f),base)) for dp,dn,fs in os.walk(base) for f in fs if '.git' not in dp]; z.close(); print(out)"
```

Before publishing, refresh the final archive so it includes every approved local change and this must be done after the final verification, not before the final edit.

---

## 13. GitHub Pages publishing procedure

Publishing is intentionally one consolidated operation after approval.

1. Inspect status and frozen-page diff:

```bash
cd 'D:/Pragya/Website_Material/Website'
git status --short --branch
git diff -- contact.html
```

2. Run local verification and browser QA.
3. Refresh the final ZIP under `Website_Versions/`.
4. Stage only repository files:

```bash
git add about.html index.html research.html outreach.html gallery.html styles.css translations.js photos resources
```

Do not stage `Website_Version_Links.txt` from inside the repository if it is outside the repository root. It is maintained separately.

5. Commit with a descriptive message:

```bash
git commit -m "Apply approved website corrections"
```

6. Push the selected branch:

```bash
git push origin main
```

7. Confirm the push returned a successful remote update.
8. Poll cache-busted live HTML until unique new markers appear.
9. Open the deployed pages in a browser and check the rendered DOM, images, overflow, and console.

The deployed site uses the repository root and `main` branch through GitHub Pages. There is no application server to restart.

Never place authentication values in this document. Git credentials and authentication are managed by the local Git/GitHub setup.

---

## 14. Troubleshooting guide

### The live site shows the old page

1. Confirm the commit exists locally:

```bash
git log -3 --oneline
```

2. Confirm the push succeeded:

```bash
git status --short --branch
```

3. Fetch the raw `main` file and compare it to GitHub Pages.
4. Add a query string to the Pages URL.
5. Wait for GitHub Pages/CDN propagation.
6. If raw GitHub contains the change but Pages does not after a reasonable delay, inspect repository Pages settings and deployment state.

### A page returns 404

- Confirm the filename and capitalization.
- Confirm the link is relative and points to an existing `.html` file.
- Confirm the file is committed and pushed.
- Do not use Windows backslashes in HTML URLs.

### An image is broken

- Check exact spelling, spaces, parentheses, and extension.
- Confirm the file is inside `Website/photos/` or `Website/resources/`.
- Check the HTML path relative to the page.
- Test the URL through the local HTTP server.
- Check Git status to ensure the asset is tracked and pushed.
- Remember GitHub Pages is case-sensitive.

### Images look stretched or cropped badly

- Inspect the source image dimensions.
- For subject-critical photographs use `object-fit: contain`.
- For decorative card images use `object-fit: cover` only if the crop is acceptable.
- Tune `object-position` on the page-specific selector.
- Do not globally change all image rules to fix one image.

### Text is unreadable over a photograph

- Increase the page-specific overlay darkness.
- Use cream/high-contrast text.
- Check italic text separately.
- Inspect the rendered image, not just the CSS source.

### A heading takes too much space

- Constrain its `max-width`.
- Use `font-size: clamp(...)`.
- Tighten `line-height` moderately.
- Add a narrow-screen rule.
- Do not force long text onto one line on a phone.

### A section has too much blank space

Inspect computed `padding-top`, `padding-bottom`, margins, hero height, and inline styles. Look for stacked shared and page-specific rules. Use a scoped selector for one page. Do not collapse all spacing to zero.

### The translation switcher loses text or links

- Confirm `translations.js` loads.
- Confirm the key matches normalized visible English text.
- Preserve inline HTML by translating text nodes rather than replacing full HTML.
- Confirm the original English is restored before each new language.
- Check `localStorage.getItem('site-language')` in the browser console.
- Add dictionaries for every new visible sentence.

### The page has horizontal overflow

Use the browser console:

```javascript
({ scrollWidth: document.documentElement.scrollWidth, clientWidth: document.documentElement.clientWidth })
```

Common causes:

- fixed-width image or grid child;
- long unbreakable text;
- `white-space: nowrap` on mobile;
- a hero title with excessive width;
- negative margins;
- a collage child without `min-width: 0`.

Fix the page-specific cause first.

### Contact changed unexpectedly

Run:

```bash
git diff -- contact.html
```

If it changed unintentionally, restore only Contact from the last approved snapshot or Git revision. Do not manually rewrite it from memory.

### A Gallery duplicate is reported

Do not delete photographs from `photos/`. Compare Gallery markup and image content, remove only repeated entries, recount displayed photos, and rerun broken-image and overflow checks.

### The local server does not respond

- Confirm the server is running from the correct directory.
- Confirm port `8765` is not occupied.
- Start again with `python -m http.server 8765`.
- Use `http://127.0.0.1:8765/`, not a `file:///` URL, for browser QA.

---

## 15. Safe change patterns

### Changing a page heading

1. Read the exact existing HTML.
2. Replace only the targeted heading.
3. Search for old and new wording.
4. Check translations if the heading is visible on all languages.
5. Browser-check desktop and phone.

### Changing a hero

1. Verify the supplied image and crop.
2. Use a page-specific hero class.
3. Keep title and supporting paragraph in one overlay block.
4. Preserve contrast overlay.
5. Check the bottom edge and following section spacing.

### Adding a supplied photograph

1. Copy the exact file.
2. Use a relative path.
3. Add factual alt text.
4. Preserve aspect ratio.
5. Confirm natural dimensions and no broken-image state.

### Removing a homepage section

1. Remove the full section markup, not merely its opacity or visibility.
2. Update any CTA that targeted the deleted anchor.
3. Check the page DOM for the old section ID and class.
4. Confirm the separate page containing the detailed content is still linked.
5. Verify the homepage has no unintended blank band.

---

## 16. Current known state and handoff notes

- The latest approved correction batch has been pushed to GitHub Pages.
- Current public URL is listed at the top of this document.
- Homepage About summary block is removed.
- Homepage `A little about Akshay` link points to `about.html`.
- Research hero uses the shorter primate heading.
- About contains the detailed Correction3 wording and compact highlights.
- Research, Outreach, and Gallery corrections are part of the published site.
- Gallery duplicate entries were removed while source files were retained.
- Contact is intended to remain frozen.
- The local preview server is normally run on port `8765`.
- Any future correction batch must be archived before editing and published only after explicit approval.
- The translation architecture is offline/static; any new visible English strings require corresponding dictionary work before claiming complete multilingual coverage.

This rulebook is the first place to update when the site architecture, deployment method, palette, page boundaries, or translation mechanism changes.
