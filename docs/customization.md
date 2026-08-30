# Customization checklist

## Identity

Edit `config.yml` and replace:

- `Arvel Scholar`
- `hello@example.org`
- `https://example.org`
- the sample biography and social-profile URLs

Search the repository for `Arvel Scholar` and `example.org` before publishing.

## Languages

English content lives in `content/en/`; French content lives in `content/fr/`. Keep both trees structurally similar so navigation remains predictable. For a single-language site, remove the unwanted language block from `config.yml` and its content directory.

## Sections

- `papers`: journal articles, chapters, preprints, and working papers
- `projects`: ongoing and completed research initiatives
- `questions`: exploratory notes organized around open questions
- `resources`: datasets, software, reading lists, and teaching material
- `writing`: essays, updates, field notes, and announcements

Menus are configured independently for each language in `config.yml`.

## Branding

Replace:

- `static/assets/favicon-books.png`
- `static/assets/social-preview.png` (recommended size: 1200 × 630 pixels)

A page-level `cover.image` is used for its social preview when available; otherwise the global image from `params.images` is used.

## Before publishing

1. Search for placeholder names and URLs.
2. Build the production site with `hugo`.
3. Check both languages, search, navigation, and social metadata.
4. Review the generated `public/` directory for unexpected personal files.

