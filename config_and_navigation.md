# Config changes

## 1. `_config.yml`: replace or merge these keys

```yaml
title: "Christopher Kuetsinya"
description: "PhD Candidate in Statistics, Bowling Green State University"
url: "https://chriskuets.github.io"

author:
  name: "Christopher Kuetsinya"
  avatar: "/assets/images/Headshot.jpeg"
  bio: "PhD Candidate in Statistics, Bowling Green State University"
  location: "Bowling Green, Ohio"
  links:
    - label: "CV"
      icon: "fas fa-fw fa-file-pdf"
      url: "/assets/files/Kuetsinya_CV.pdf"
    - label: "Email"
      icon: "fas fa-fw fa-envelope"
      url: "mailto:ckuetsinya@gmail.com"
    - label: "Google Scholar"
      icon: "fas fa-fw fa-graduation-cap"
      url: "https://scholar.google.com/"   # replace with your profile URL, or delete these 3 lines
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/chriskuets"

footer:
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope"
      url: "mailto:ckuetsinya@gmail.com"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/chriskuets"

atom_feed:
  hide: true    # removes the "Feed" link from the footer

plugins:
  - jekyll-include-cache
  - jekyll-redirect-from   # sends old /home/ links to the root page
```

`jekyll-redirect-from` is supported on GitHub Pages. If you use a Gemfile, also add `gem "jekyll-redirect-from"`.

## 2. `_data/navigation.yml`

```yaml
main:
  - title: "Research"
    url: /research/
  - title: "Publications"
    url: /publications/
  - title: "Teaching"
    url: /teaching/
  - title: "CV"
    url: /assets/files/Kuetsinya_CV.pdf
```

The site name in the header already links home, so the separate "Home" item is no longer needed.

## 3. Files to add or remove

- **Delete** the old `/home/` page (often `_pages/home.md` or `about.md`). `index.md` now covers it and redirects `/home/`.
- **Upload** `assets/files/Kuetsinya_CV.pdf` and `assets/files/Kuetsinya_Teaching_Statement.pdf`. The pages link to both.
- **Place** `research.md`, `publications.md`, and `teaching.md` in `_pages/` (or wherever your current pages live). Each one has its own `permalink`, so the folder doesn't matter.
