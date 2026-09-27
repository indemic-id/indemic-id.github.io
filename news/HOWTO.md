# How to add a news post

## What goes here

News is for community appearances and announcements that are not INDEMIC-run events:

- Members presenting at external conferences or workshops
- Media coverage or podcast appearances
- New publications or preprints by community members
- Community milestones (new partnerships, funding, etc.)
- Announcements (new resources, calls for participation, etc.)

For INDEMIC-organised events (workshops, symposia, webinars), use `events/` instead.

---

## Folder structure

Each post lives in its own folder under `news/posts/`:

```
news/posts/
└── 2025-06-10-members-at-iseid/
    ├── index.qmd        ← the news post
    └── images/          ← photos (optional)
        ├── photo1.jpg
        └── photo2.jpg
```

**Naming convention:** `YYYY-MM-DD-short-slug/` — use the date of the appearance/announcement and a short, lowercase, hyphenated slug.

---

## Front matter fields

| Field | Required | Notes |
|---|---|---|
| `title` | Yes | Clear, descriptive headline |
| `date` | Yes | Date of the appearance or announcement, `YYYY-MM-DD` |
| `description` | Yes | 1–2 sentence summary shown on the listing card |
| `categories` | Yes | One or more: `[conference]`, `[training]`, `[publication]`, `[media]`, `[announcement]`, `[award]` |
| `image` | No | Path to a cover image, e.g. `images/cover.jpg` |

---

## Skeleton — copy this into a new `index.qmd`

```markdown
---
title: "HEADLINE"
date: YYYY-MM-DD
description: "One or two sentences summarising the news for the listing card."
categories: [conference]    # conference / training / publication / media / announcement / award
image: images/cover.jpg     # remove if no cover image
---

[1–2 paragraphs with the main story — who, what, where, and why it matters to the community.]

## Presentations / Talks

<!-- For conference appearances: list what was presented -->
- **"Talk title"** — Speaker Name
- **"Talk title"** — Speaker Name

## Publication

<!-- For preprints or papers -->
**Title:** [Paper title](https://doi.org/LINK)  
**Authors:** Author A, Author B, ...  
**Journal/Venue:** Journal Name  
**DOI:** [10.xxxx/xxxxx](https://doi.org/LINK)

## Photos

<!-- Horizontal scrollable strip — add as many images as you like -->
```{=html}
<div class="photo-strip">
<img src="images/photo1.jpg" alt="Caption">
<img src="images/photo2.jpg" alt="Caption">
<img src="images/photo3.jpg" alt="Caption">
</div>
```

<!-- Or link to an external album instead -->
[View photo album →](https://photos.google.com/LINK){target="_blank"}

## Links

<!-- Add any relevant external links -->
- [Conference website](https://LINK){target="_blank"}
- [Recording](https://LINK){target="_blank"}
- [Slides](https://LINK){target="_blank"}
```

---

## Workflow summary

1. **Create the folder** `news/posts/YYYY-MM-DD-slug/`
2. **Copy the skeleton above** into `news/posts/YYYY-MM-DD-slug/index.qmd`
3. **Fill in the front matter** (title, date, description, categories)
4. **Fill in the body** — keep only the sections that apply, delete the rest
5. **Add photos** (optional): put them in `images/` and embed or link in the post. Aim for <500 KB each.

---

## Asking me to build the post

Share rough notes — who attended, what they presented, where, any links — and say "write me a news post for this". I will draft the prose and format it properly.
