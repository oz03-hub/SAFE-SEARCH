# SAFE-SEARCH @ ECIR 2027 — workshop website

Single-page Jekyll site, built natively by GitHub Pages (no Actions needed).

## Editing content

All content is in YAML — no HTML editing needed.

| What | File |
|---|---|
| Title, venue, date, hero buttons, contact email, nav menu | `_config.yml` |
| About text + highlighted question | `_data/about.yml` |
| Topics of interest | `_data/topics.yml` |
| Call for papers (types, notes) | `_data/cfp.yml` |
| Submission page (`/submit/`): rules, Google Form link | `_data/submission.yml` (`form_url`) |
| Important dates | `_data/dates.yml` |
| Program / schedule | `_data/schedule.yml` |
| Keynote speakers | `_data/speakers.yml` |
| Accepted papers | `_data/papers.yml` (shows "TBA" while empty) |
| Organizers | `_data/organizers.yml` |
| Program committee | `_data/committee.yml` (section hidden while empty) |
| Colors | top of `assets/css/style.css` (`--accent` etc.) |
| Section order | `index.html` |

Text fields in about/topics/cfp notes accept Markdown (`**bold**`, `[link](url)`).

**Photos:** drop an image in `assets/img/organizers/` (or `assets/img/speakers/`),
then set `photo: filename.jpg` on that person. Square images look best. Without a photo, initials are shown.

**New nav item:** add a section include to `index.html` with an `id`, then add `{ label: ..., id: ... }` to `nav` in `_config.yml`.

## Deploy (GitHub Pages)

1. Push this folder to a GitHub repo.
2. Repo → Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.
3. If the URL is `https://USER.github.io/REPO/`, set `baseurl: "/REPO"` in `_config.yml`.
   For `https://USER.github.io/` or a custom domain, leave `baseurl: ""`.

## Local preview (optional)

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```
