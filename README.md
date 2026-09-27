# INDEMIC Website

Source for the [INDEMIC community website](https://indemic-id.github.io) — built with [Quarto](https://quarto.org) and deployed to GitHub Pages.

---

## For contributors

You don't need to know how to code to add news or events. The steps below cover everything.

### Prerequisites

- A GitHub account with write access to this repository
- [Git](https://git-scm.com/) installed, or use [GitHub Desktop](https://desktop.github.com/) if you prefer a GUI
- [Quarto](https://quarto.org/docs/get-started/) installed (optional — only needed if you want to preview locally)

---

## Adding a news post

News is for community appearances at **external** events: conferences, workshops, training courses, publications, awards, and media coverage. For INDEMIC-organised events (webinars, seminars, symposia), use **Events** instead.

### Step 1 — Create the folder

Inside `news/posts/`, create a new folder named `YYYY-MM-DD-short-slug`, for example:

```
news/posts/2026-10-05-iseid-conference/
```

### Step 2 — Create `index.qmd`

Copy this skeleton into `news/posts/YYYY-MM-DD-slug/index.qmd`:

```markdown
---
title: "HEADLINE"
date: YYYY-MM-DD
description: "One or two sentences for the listing card."
categories: [conference]   # conference / training / publication / media / announcement / award
---

[Body text here.]

## Photos

​```{=html}
<div class="photo-strip">
<img src="images/photo1.jpg" alt="Caption">
<img src="images/photo2.jpg" alt="Caption">
</div>
​```

## Links

- [Link text](https://url){target="_blank"}
```

### Step 3 — Add photos (optional)

Put photos in `news/posts/YYYY-MM-DD-slug/images/`. Aim for **under 500 KB per image** — use [Squoosh](https://squoosh.app) to compress if needed (fully local, nothing is uploaded).

### Step 4 — Commit and push

```bash
git add news/posts/YYYY-MM-DD-slug/
git commit -m "Add news: short description"
git push
```

The site rebuilds automatically in ~2 minutes.

---

## Adding an event

Events are INDEMIC-organised activities: webinars, seminar series, workshops, and symposia.

### Step 1 — Create the folder

Inside `events/posts/`, create a folder named `YYYY-MM-DD-short-slug`.

### Step 2 — Create `index.qmd`

Copy this skeleton:

```markdown
---
title: "EVENT TITLE"
date: YYYY-MM-DD
location: "Online (Zoom)"
event-format: "Online"       # Online / In-person / Hybrid
status: "upcoming"           # change to "past" after the event
description: "One or two sentences for the listing card."
categories: [webinar]        # webinar / workshop / symposium / conference
---

## About this event

[Description of the event.]

## Registration

[Register here →](https://forms.google.com/){.btn .btn-primary target="_blank"}

---

## Summary

[Fill in after the event, then change status to "past".]

## Recording

[Watch recording →](https://youtu.be/LINK){.btn .btn-primary target="_blank"}

## Photos

​```{=html}
<div class="photo-strip">
<img src="images/photo1.jpg" alt="Caption">
</div>
​```
```

**After the event:** change `status: "upcoming"` to `status: "past"` and fill in the Summary, Recording, and Photos sections.

---

## Asking Claude to write posts

You can share rough notes with Claude Code (or Claude.ai) and ask it to draft the post for you. Give it:

- Who attended / presented / organised
- Where and when
- Any links (event website, recording, news article)
- Photos to add

Claude will format the front matter, write the prose, and embed the photo strip correctly.

---

## Project structure

```
indemic-id.github.io/
├── _quarto.yml          # site config, navbar, footer
├── custom.scss          # brand styles (colors, fonts, photo strip)
├── index.qmd            # homepage
├── about.qmd            # about page
├── people.qmd           # members page
├── contact.qmd          # contact page
├── resources.qmd        # resources page
├── news/
│   ├── index.qmd        # news listing page
│   ├── HOWTO.md         # detailed guide for news contributors
│   └── posts/           # one folder per news post
│       └── YYYY-MM-DD-slug/
│           ├── index.qmd
│           └── images/
└── events/
    ├── index.qmd        # events listing page
    ├── HOWTO.md         # detailed guide for events contributors
    └── posts/           # one folder per event
        └── YYYY-MM-DD-slug/
            ├── index.qmd
            └── images/
```

For more detail on news or events, see the `HOWTO.md` files inside each section folder.

---

## Local preview (optional)

If you have Quarto installed, run this from the project root to preview the site locally before pushing:

```bash
quarto preview
```

---

## Brand reference

| | |
|---|---|
| **Primary colour** | `#21B0BA` (cyan) |
| **Secondary colour** | `#13213C` (navy) |
| **Background** | `#F4F5F8` (light gray) |
| **Typeface** | Figtree (Google Fonts) |

Logo files are in `assets/logos/`.
