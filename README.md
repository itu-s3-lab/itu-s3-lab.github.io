# IT:U S³ Lab website

Source of [itu-s3-lab.github.io](https://itu-s3-lab.github.io), the website of the Smart Sensing and Systems Lab (S³ Lab) at IT:U.

Built with [Hugo](https://gohugo.io) and a small custom theme (no external theme to update).
Every push to `main` rebuilds and publishes the site automatically via GitHub Actions.

---

## Quick reference

| I want to…                  | Edit / run                                                        |
|-----------------------------|-------------------------------------------------------------------|
| Add a news post             | `hugo new content news/2026-12-15-my-title.md`                    |
| Write the monthly recap     | `hugo new content news/2026-12-recap.md --kind recap`             |
| Add or update a team member | `data/team.yaml` + photo in `static/images/team/`                 |
| Add a publication           | `data/publications.yaml`                                          |
| Change research areas       | `data/research.yaml`                                              |
| Change home page texts      | `content/_index.md`                                               |
| Change contacts, menu, version | `hugo.toml`                                                    |
| Change colors or fonts      | `assets/css/main.css` (tokens at the top)                         |

No local installation is needed for small edits: you can edit any file directly on GitHub (pencil icon → *Commit changes*) and the site updates in about a minute.

---

## Working locally

**Requirements:** [Git](https://git-scm.com) and [Hugo](https://gohugo.io/installation/) (extended edition, v0.169 or newer).

```bash
git clone https://github.com/itu-s3-lab/itu-s3-lab.github.io.git
cd itu-s3-lab.github.io
hugo server -D        # preview at http://localhost:1313 (-D also shows drafts)
```

The preview reloads automatically when you save a file. Stop it with `Ctrl+C`.

To publish:

```bash
git pull              # get the latest changes from the others first
git add -A
git commit -m "News: short description"
git push
```

Check the **Actions** tab on GitHub: when the run is green, the site is live.

---

## News and monthly recaps

News live in `content/news/`, one Markdown file per post.

```bash
hugo new content news/2026-12-15-best-paper-award.md
```

This creates the file from `archetypes/news.md`. Fill in `title`, `summary`, write the text, then set `draft: false`.
Optional cover image: put it in `static/images/news/` and set `image: "images/news/my-photo.jpg"`.

Monthly recaps use their own template:

```bash
hugo new content news/2026-12-recap.md --kind recap
```

A recap has `recap: true` and three short `highlights` (papers, people, events): the latest recap is shown as the dark card on the home page.

---

## Team

Each member is an entry in `data/team.yaml`:

```yaml
- name: "Jane Doe"
  role: "PhD Student"
  group: "PhD Students"          # one of the groups in data/team_groups.yaml
  image: "images/team/jane-doe.jpg"
  bio: |
    Short biography, Markdown allowed.
  links:
    email: "jane.doe@it-u.at"
    scholar: "GOOGLE_SCHOLAR_ID"
    orcid: "0000-0000-0000-0000"
    github: "janedoe"
```

Photos: square, about 480×480 px, in `static/images/team/`.
To move someone to the alumni, change `group` to `"Alumni"`.

---

## Publications

Add entries to `data/publications.yaml` (see the example at the top of the file).
They are grouped by year on `/publications/`; entries with `selected: true` also appear on the home page (latest 3).
While the list is empty, the page links to Google Scholar and the home section is hidden.

---

## Releases

The website version is set in `hugo.toml` (`params.version`) and shown in the footer.
When you publish a notable change, bump it and create a matching release on GitHub (*Releases → Draft a new release*, tag `vX.Y`).

| Version | Description |
|---------|-------------|
| v1.0    | New Hugo website, new logo |
| v0.5    | Previous Jekyll site (Petridish theme) |

---

## Project structure

```
archetypes/        templates for new news and recaps
assets/css/        styles (main.css) and self-hosted font definitions
content/           pages and news (Markdown)
data/              team, publications, research areas (YAML)
layouts/           HTML templates of the custom theme
static/            images, fonts, favicon (copied as they are)
.github/workflows/ automatic build and deploy to GitHub Pages
hugo.toml          site configuration
```

Fonts (Inter, Space Grotesk, JetBrains Mono, SIL Open Font License) are self-hosted: the site makes no requests to Google or other third parties.

## License

Code: MIT (see `LICENSE.md`). Content: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
