# CMJM Lab Website — Claude Project Instructions

## Project Overview
You are helping maintain and develop the **CMJM Lab** (Computational Multidata Junction in Medicine) website. The lab is led by **Dr. Mei-Ju May Chen**, Assistant Professor at the Smart Medicine and Health Informatics Master's Program, International College, National Taiwan University.

**Repo:** https://github.com/CMJM-Lab/cmjm-lab.github.io
**Live site:** https://cmjm-lab.github.io/
**Tech stack:** Hugo + GitHub Pages (deployed via GitHub Actions)

---

## Brand & Design System

### Color Palette (from lab summary graphic)
| Token         | Hex       | Usage                                      |
|---------------|-----------|---------------------------------------------|
| Teal          | `#2d9fa1` | Primary brand — nav, links, tags, avatars   |
| Teal Dark     | `#1f7e80` | Hover states, dark accents                  |
| Teal Light    | `#e8f6f6` | Card backgrounds, badges                    |
| Orange        | `#e8852f` | Accent — stats, position cards, highlights  |
| Orange Light  | `#fdf0e6` | Accent backgrounds                          |
| Red           | `#d42027` | CMJM logo letters only (C, M, J, M)        |
| Dark          | `#2c2c2c` | Navbar, footer background                   |
| Body BG       | `#f7f8f9` | Page background                             |

### Typography
- Font: System UI stack (`'Segoe UI', system-ui, -apple-system, sans-serif`)
- Body text: `#2c2c2c`
- Muted text: `#6c757d`

### Design Principles
- Clean, modern academic style
- Teal is the dominant color; orange is the secondary accent
- Red is ONLY used for the C, M, J, M letters in the lab name
- Dark navbar and footer (not white)
- Cards with subtle borders, hover shadows
- Responsive (mobile-first)

---

## Sitemap & Page Structure

```
/                  → Home (hero, stats, research highlights, latest news)
/research/         → Research areas (Biomarker, AI, Bioinformatics Tools)
/people/           → Current team (PI featured card + grid for students/staff)
/alumni/           → Former members & where they are now
/publications/     → From BibTeX, filterable by year/category
/software/         → Tools: GFF3toolkit, DrBioRight, TCPA
/news/             → News archive with detail pages
/join/             → Open positions (postdoc, PhD, MS, RA)
/contact/          → Email, affiliation, map
```

---

## Content Management Guide

### Adding a New Team Member
Create a file in `content/people/`:
```markdown
---
title: "Full Name"
role: "Master's Student"  # or PhD Student, Postdoc, Research Assistant
image: "/img/people/filename.jpg"
intro: "Brief research description"
links:
  - title: "GitHub"
    url: "https://github.com/username"
  - title: "Google Scholar"
    url: "https://scholar.google.com/..."
weight: 10  # lower = appears first
---
```

### Adding a News Item
Create a file in `content/news/`:
```markdown
---
title: "News Title"
date: 2025-12-03
---
Full news content here with markdown formatting.
```

### Adding a Publication
Add a BibTeX entry to `data/publications.bib`. The site auto-renders it.

### Moving a Member to Alumni
Move their `.md` file from `content/people/` to `content/alumni/` and optionally add a `current_position` field.

---

## Lab Information

- **Lab full name:** Computational Multidata Junction in Medicine (CMJM) Lab
- **PI:** Dr. Mei-Ju May Chen (陳玫如)
- **Affiliation:** Assistant Professor, Smart Medicine and Health Informatics Master's Program, International College, National Taiwan University
- **Yushan Young Fellow:** 2024–2029 (5-year)
- **Contact:** mjmchen@g.ntu.edu.tw
- **Primary language:** English (international lab)

### Research Areas
1. **Biomarker Identification** — SIRPα, immunotherapy, tumor microenvironment (Cancer Cell 2022)
2. **AI-Driven Biomedical Analytics** — DrBioRight NLP platform (Cancer Cell 2021)
3. **Bioinformatics Tool Development** — GFF3toolkit, TCPA v3.0
4. **Multi-omics Data Analysis** — DNA, RNA, epigenetics, proteomics
5. **Single-cell & Spatial Transcriptomics**
6. **ceRNA Networks & Immuno-oncology**

### Tools Developed
- **GFF3toolkit** — Genome annotation QC (75+ GitHub stars, top 8%)
- **DrBioRight** — AI biomedical analysis platform (Cancer Cell 2021)
- **TCPA v3.0** — Pan-cancer proteomic data platform (MCP 2019)

---

## Development Notes

### Hugo Theme
The site uses a custom Hugo theme built from scratch (not a pre-built theme) to match the lab's specific design requirements.

### Building Locally
```bash
hugo server -D    # development with drafts
hugo              # production build (outputs to public/)
```

### Deployment
GitHub Actions automatically builds and deploys on push to `main`. The workflow file is at `.github/workflows/hugo.yml`.

### Key Directories
```
content/       → All page content (Markdown + YAML frontmatter)
layouts/       → Hugo templates (HTML)
static/img/    → Images (people photos, research graphics)
assets/css/    → Stylesheets
data/          → publications.bib and other data files
```
