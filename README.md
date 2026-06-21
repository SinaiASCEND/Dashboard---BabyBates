# Baby Bates — Clinical Reference Dashboard

A web-based study companion for medical students: a unified **Core + Cluster physical-examination
framework**, **71 illness scripts**, lab references, clinical pathways, **device-modification guides**,
and an abbreviation lookup — all searchable, with tick-off checklists and pinnable favorites.

> **Acknowledgement.** All clinical content is adapted from *Bates' Pocket Guide to Physical
> Examination and History Taking* (Rainier P. Soriano, MD). This dashboard simply makes that
> material searchable and easy to study at the bedside. Full credit for the content belongs to the
> author. See the in-app **Acknowledgement** section for sources cited within the text.

## Features

- **Core PE Skills** — 8 universal sections with FULL / PARTIAL performance criteria and saved checklist progress.
- **Cluster Exams** — 8 clinical-concern groups, each with its core baseline plus cluster-specific and optional maneuvers.
- **Illness Scripts** — 71 presenting complaints, each opening to a full comparison table of differential diagnoses across symptom, pathophysiology, epidemiology, timing, signs, diagnostics, and treatment.
- **Lab Values** and **Clinical Pathways** — supplementary quick reference.
- **Device Modifications** — how to adapt the exam for 32 devices, prostheses, and procedures, with illustrations.
- **Abbreviations** — filterable lookup.
- **Search** across everything, **favorites**, and a fully responsive phone/desktop layout.

## Running it

This is a static site — no build step. Because it loads its data with JavaScript modules, it must be
served over HTTP (not opened with `file://`).

**Locally:**

```bash
# from the repo root
python3 -m http.server 8000
# then open http://localhost:8000
```

**On GitHub Pages:**

1. Push these files to a repository.
2. In **Settings → Pages**, set the source to your default branch, root (`/`).
3. Your site publishes at `https://<user>.github.io/<repo>/`.

The included empty `.nojekyll` file tells GitHub Pages to serve all files as-is.

## Files

```
index.html         The dashboard (a self-rendering component page)
support.js         Lightweight runtime that renders the page
data.js            PE framework, clusters, devices, labs, pathways, abbreviations
scripts-data.js    The 71 illness scripts (Appendix A)
assets/            Cover image, author photo, and device illustrations
```

## Notes

- Lab values and clinical pathways are supplementary educational reference (flagged as such in the
  app); ranges vary by laboratory — always use your institution's reference values and follow local
  protocols and clinical judgment.
- Checklist progress and favorites are stored in your browser's local storage on each device.
