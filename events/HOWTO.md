# How to add an event page

## Folder structure

Each event lives in its own folder under `events/posts/`:

```
events/posts/
└── 2026-04-15-workshop-modelling-basics/
    ├── index.qmd        ← the event page
    └── images/          ← photos for this event (optional)
        ├── photo1.jpg
        └── photo2.jpg
```

**Naming convention:** `YYYY-MM-DD-short-slug/` — use the event start date and a short, lowercase, hyphenated slug.

---

## Front matter fields

| Field | Required | Notes |
|---|---|---|
| `title` | Yes | Full event title |
| `date` | Yes | Start date, `YYYY-MM-DD` |
| `date-end` | No | End date if multi-day, `YYYY-MM-DD` |
| `location` | Yes | City/venue or "Online (Zoom)" |
| `event-format` | Yes | `"In-person"`, `"Online"`, or `"Hybrid"` |
| `status` | Yes | `"upcoming"` or `"past"` — controls which listing it appears in |
| `description` | Yes | 1–2 sentence summary shown on the listing card |
| `categories` | Yes | One of: `[workshop]`, `[symposium]`, `[webinar]`, `[conference]` |
| `image` | No | Path to a cover image, e.g. `images/cover.jpg` |

**To move an event from upcoming to past:** change `status: "upcoming"` → `status: "past"` in the front matter.

---

## Skeleton — copy this into a new `index.qmd`

```markdown
---
title: "EVENT TITLE"
date: YYYY-MM-DD
date-end: YYYY-MM-DD          # remove if single-day
location: "City, Country"
event-format: "In-person"     # or Online / Hybrid
status: "upcoming"            # change to "past" after the event
description: "One or two sentences describing the event for the listing card."
categories: [workshop]        # workshop / symposium / webinar / conference
image: images/cover.jpg       # remove if no cover image
---

## About this event

[2–3 paragraphs describing what the event is, who it is for, and why it matters.]

## Programme / Agenda

<!-- Optional: add schedule or session list -->
- **09:00** Opening remarks
- **09:15** Session 1: ...
- **12:00** Lunch
- **13:00** Session 2: ...

## Details

| | |
|---|---|
| **Date** | DD Month YYYY |
| **Format** | In-person / Online / Hybrid |
| **Location** | City, Country |
| **Language** | Bahasa Indonesia / English |

## Registration

<!-- Replace with actual form link, or remove if registration is closed -->
[Register here →](https://forms.google.com/){.btn .btn-primary target="_blank"}

*[Any note on eligibility, capacity, or deadline.]*

## Contact

Questions? Email us at **indemic.community@gmail.com**

---

<!-- ============================================================
     FILL IN BELOW AFTER THE EVENT — then change status to "past"
     ============================================================ -->

## Summary

[A short recap of what happened, key takeaways, number of participants, etc.]

## Recording

<!-- Remove if no recording -->
[Watch recording →](https://youtube.com/LINK){.btn .btn-primary target="_blank"}

## Presentations

<!-- Add slide links as they become available -->
- **Talk title** — Speaker Name ([slides](LINK))

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
```

---

## Workflow summary

1. **Create the folder** `events/posts/YYYY-MM-DD-slug/`
2. **Copy the skeleton above** into `events/posts/YYYY-MM-DD-slug/index.qmd`
3. **Fill in the front matter** (title, date, location, format, description, categories)
4. **Fill in the body** (about, programme, details, registration)
5. **Add a cover image** (optional): put it in `images/` and set `image: images/cover.jpg` in front matter
6. **After the event:**
   - Change `status: "upcoming"` → `status: "past"`
   - Fill in Summary, Recording, Presentations, Photos sections
   - Add photos to `images/` folder (JPG or PNG, reasonable file size — aim for <500 KB each)

---

## Asking me to build the page

Share the filled-in skeleton (or even rough notes with the key details) and say "build me the event page for this". I will format it properly, write polished prose for the about/summary sections, and handle any layout details.
