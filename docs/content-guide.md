# Content guide

Content uses TOML front matter between `+++` markers. The included fictional files are copyable examples.

## Paper metadata

```toml
+++
title = "Article title"
date = 2026-01-15
draft = false
summary = "One-sentence summary."
authors = ["Arvel Scholar", "Sam Researcher"]
status = "Published"
publication_type = "Journal article"
publication = "Journal name"
volume = 12
issue = 1
pages = "1–15"
tags = ["topic"]
citation = "Formatted citation"

[[links]]
label = "Publisher page"
url = "https://example.org/article"
+++
```

Add the abstract or description below the closing `+++`.

## Post cover image

```toml
[cover]
image = "/assets/images/example-cover.jpg"
alt = "Accessible description of the image"
hiddenInSingle = true
```

Store the referenced file under `static/assets/images/`. The cover is used for social sharing; pages without a cover use the global social preview.

## Drafts

Set `draft = true` while editing. Preview drafts with:

```bash
hugo serve --buildDrafts
```
