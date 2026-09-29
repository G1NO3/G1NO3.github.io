# Jiyi Wang — research website

Personal academic website for robot learning, embodied AI, and NeuroAI, built with Hugo Blox and deployed to GitHub Pages.

## Local preview

Use **Hugo Extended 0.136.5** (the version pinned in `.github/workflows/publish.yaml`) and Go 1.19 or newer:

```sh
hugo server
```

For a production build:

```sh
hugo --minify
```

The deployment workflow builds and publishes the site when changes are pushed to `main`.

## Content and layout

- `content/authors/admin/_index.md`: biography, education, experience, and skills.
- `layouts/landing/research-home.html`: homepage layout (bio, videos, compact publications, and contact).
- `content/publication/*/index.md`: publication metadata and research overviews.
- `layouts/partials/research/`: shared publication and author presentation.
- `layouts/publication/`: publication archive and detail pages.
- `assets/css/custom.css`: responsive styles, dark mode, and print styling.
- `static/uploads/resume.pdf`: downloadable CV, updated from `ref/CV (7).pdf`.
- `content/_index.md`: editable homepage bio, research description, headings, contact line, and robot demo details.
- `static/videos/`: web-ready robot demonstrations and extracted poster frames. Originals remain in `ref/`.
- `config/_default/menus.yaml`: navigation.

Set `featured: true` on a publication to show it on the homepage. Its `weight` controls the order. Add verified `url_pdf`, `url_code`, and `links` fields to expose paper and code resources. Complete author lists use `admin` for Jiyi Wang, which highlights the name automatically.

Template blog posts, teaching examples, events, and example projects remain in the repository as drafts and are excluded from production builds.

## Robot demonstration videos

The homepage's `robot_demos` entries are rendered below the current robotics project. Each video has a poster, native playback controls, an inline mobile player, and a direct MP4 link. Playback starts muted on user interaction; `preload="none"` avoids downloading the videos on initial page load.

The MP4s in `static/videos/` are H.264/YUV420p encodes at the original 1906 × 1080 resolution, with original audio retained and MP4 fast-start enabled. JPEG posters are extracted from the recordings. Update the media files and corresponding `content/_index.md` entries together when replacing a demonstration.

## Publication metadata to complete

The two NeurIPS 2026 papers are marked accepted based on the author's confirmation and current CV. The supplied PDFs are anonymous review versions. Their research descriptions are included, but those files are not published as downloadable manuscripts.

The author confirmed the complete author lists for both papers on September 28, 2026. Both pages now display all authors in order, highlight Jiyi Wang, and provide downloadable BibTeX citations:

- `content/publication/wang-2026-motor-motifs/index.md`
- `content/publication/wang-2026-dales-principle/index.md`

The citations are synchronized with `publications.bib` and marked accepted. Public paper/code links and final proceedings metadata remain to be added when available. The two older preprints have been removed from the website and bibliography; their source pages and citations are preserved in `ignore/preprints/` outside the published content tree.

All three publication pages use the same structure: a teaser figure, a short overview, method, experimental findings, and research connection. Each teaser is extracted from Figure 1 of the corresponding manuscript. Edit its `teaser.image`, `teaser.alt`, and `teaser.caption` fields in the publication's `index.md`; the image lives in that paper's folder.

The ICML 2025 record includes the supplied SWIRL PDF (`content/publication/ke-2025-inverse/paper.pdf`) and links to the official PMLR proceedings and public code. Quantitative robotics results and technical skills follow the supplied CV. Human-motion transfer is described as a research interest, not an existing experimental result.

The `ref/` source folder and generated build outputs are ignored by Git.
