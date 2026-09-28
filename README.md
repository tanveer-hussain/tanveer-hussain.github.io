# tanveer-hussain.github.io

Personal academic website of Dr Tanveer Hussain, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme (MIT licence).

## Publish it (one-time, ~10 minutes)

1. **Create the repo.** On GitHub (signed in as `tanveer-hussain`) click **New repository**, name it exactly
   `tanveer-hussain.github.io`, set it **Public**, and do **not** add a README/licence.
2. **Push these files.** Either
   - **GitHub Desktop:** File → Add local repository → choose this folder → Publish/Push to the repo above; or
   - **Terminal:**
     ```bash
     cd tanveer-hussain.github.io
     git remote add origin https://github.com/tanveer-hussain/tanveer-hussain.github.io.git
     git push -u origin main
     ```
   (Don't use the web "upload files" button — it skips the hidden `.github/` folder that builds the site.)
3. **Allow the build to publish.** Repo → **Settings → Actions → General → Workflow permissions** →
   select **Read and write permissions** → Save.
4. **Wait for the build.** The **Actions** tab runs *Deploy site* (~3–5 min). If it ran before step 3 and failed,
   click it → **Re-run jobs**.
5. **Turn on Pages.** **Settings → Pages → Build and deployment → Source: Deploy from a branch** →
   Branch **gh-pages** / **(root)** → Save. After a minute the site is live at
   **https://tanveer-hussain.github.io**.

## Where to edit things

| What | File |
| --- | --- |
| Name, site description, SEO keywords | `_config.yml` (top section) |
| Bio, affiliation line, research interests | `_pages/about.md` |
| Profile photo | replace `assets/img/prof_pic.jpg` (square, ~600 px) |
| Email / Scholar / ORCID / GitHub / LinkedIn icons | `_data/socials.yml` |
| Publications | `_bibliography/papers.bib` |
| Teaching | `_pages/teaching.md` |
| KHAT-AI page | `_pages/khat-ai.md` |
| News items on the home page | `_news/*.md` (one small file per item) |
| Code/repositories page | `_data/repositories.yml` |
| CV PDF | put it at `assets/pdf/cv.pdf` and uncomment `cv_pdf` in `_data/socials.yml` |

Every push to `main` rebuilds the site automatically. You can edit any file directly on github.com (pencil icon) — no local setup needed.

### Adding all your publications from Google Scholar
Scholar profile → tick the papers → **Export → BibTeX** → paste into `_bibliography/papers.bib`.
Optional extras per entry: `selected = {true}` (show on home page), `abbr = {CVPR}` (venue badge),
`code = {https://github.com/...}`, `arxiv = {2204.06788}`, `pdf = {paper.pdf}` (file in `assets/pdf/`).

### Previewing locally (optional)
Install Docker, then run `docker compose up` in this folder and open http://localhost:8080 (see `docs/INSTALL.md` for details).
