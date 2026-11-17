# molin-han.github.io

Personal academic website of Molin Han, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme (MIT licence, see `LICENSE`).

## Where things live

| What | File |
| --- | --- |
| Name, site URL, favicon, theme options | `_config.yml` |
| Home page (bio, photo, address) | `_pages/about.md` |
| Profile photo | `assets/img/prof_pic.jpg` (currently a placeholder: replace it with your photo, same file name) |
| Email, ORCID, GitHub, LinkedIn icons | `_data/socials.yml` |
| News on the home page | `_news/*.md` (one file per item) |
| Publications | `_bibliography/papers.bib` (`selected={true}` puts a paper on the home page) |
| Research projects | `_projects/*.md`, thumbnails in `assets/img/projects/` |
| Talks | `_pages/talks.md` |
| Teaching | `_pages/teaching.md` |
| CV page | `_data/cv.yml` (RenderCV format) and the PDF at `assets/pdf/Molin_Han_CV.pdf` |

The PDF CV is the full two-page CV with the phone number removed for the public site.

## Publish on GitHub Pages

1. Create a new, empty **public** repository named exactly `Molin-Han.github.io` (no README or licence, so the first push goes through cleanly).
2. Push this folder to its `main` branch:

   ```bash
   cd molin-han.github.io
   git init -b main
   git add .
   git commit -m "Personal website based on al-folio"
   git remote add origin https://github.com/Molin-Han/Molin-Han.github.io.git
   git push -u origin main
   ```

3. In the repository: **Settings → Actions → General → Workflow permissions**, select **Read and write permissions**.
4. The **Deploy site** workflow runs on every push to `main` and builds the site into a `gh-pages` branch. When the first run has finished (see the **Actions** tab), go to **Settings → Pages** and set the source branch to `gh-pages` (not `main`).
5. The site is then live at <https://molin-han.github.io>.

If you publish under a different repository name, set `baseurl: /<repository-name>` in `_config.yml`.

## Preview locally

With Docker (then open <http://localhost:8080>):

```bash
docker compose pull
docker compose up
```

or with Ruby and Bundler (then open <http://localhost:4000>):

```bash
bundle install
bundle exec jekyll serve
```

## Workflows

Only two GitHub Actions workflows are kept: `deploy.yml` (build and publish) and `upgrade-check.yml` (checks that the configuration still matches the al-folio v1 contract). The template's maintenance workflows were removed because they only make sense in the upstream repository.

For anything else, see the al-folio documentation in `docs/` (start with `docs/CUSTOMIZE.md`).
