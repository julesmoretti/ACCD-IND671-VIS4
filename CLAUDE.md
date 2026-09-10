# CLAUDE.md

Context for Claude Code working in this repository.

## What this repo is

Canvas page content for **IND-671 Visualization 4 (Vis Com 4)** — Graduate Industrial
Design, ArtCenter College of Design. Instructor: Jules Moretti.

The content here is **evergreen**, not term-specific. It represents the current version
of the course and is improved each year in place. Past terms are captured with git tags
(`git tag 26FA`), never by duplicating folders. Do not create term-named directories.

## Structure

```
content/
  week-NN-short-kebab-case-title/
    reading.html      → Canvas page "(Reading)"
    in-class.html     → Canvas page "(In-Class Exercises)"
    assignment.html   → Canvas assignment
  _template/          → starting points for new weeks
syllabus/             → exported syllabus PDF per term
feedback/             → end-of-term feedback and the decisions it drove
```

Weeks 1–3 are populated. Weeks 4–14 are scaffolded with `.gitkeep` and need content.

## HTML conventions

These files are **fragments**, not documents. Never add `<html>`, `<head>`, `<body>`, or
`<!DOCTYPE>` — Canvas pages accept body content only, and a wrapper breaks the paste.

Every file opens with a two-line comment header naming the Canvas page it maps to:

```html
<!-- Canvas page: Week 3 - JavaScript Basics & Interactive Elements (Reading) -->
<!-- Paste the contents of this file into the Canvas HTML editor. -->
```

Keep to plain semantic HTML: `h3`/`h4` headings, `ul`/`ol`, `pre><code` for code blocks,
`strong`/`em`, and links with `target="_blank" rel="noopener"`. Use `&lt;` and `&gt;` for
code samples that contain markup.

## When importing from a Canvas export (.imscc)

A Canvas export is a zip. Pages arrive with accumulated cruft that must be stripped:

- **ChatGPT paste artifacts** — `<div class="dark bg-gray-950 ...">`, `hljs-*` spans,
  `contain-inline-size`, `border-token-border-medium`
- **YuJa artifacts** — `<span class="textLayer--absolute" dir="ltr" role="presentation">`
- **Inline syntax-highlighting** — `<span style="color: #bb0066;">` wrappers around code;
  replace the whole block with a clean `<pre><code>`
- **Empty spacers** — `<p>&nbsp;</p>`
- **Meaningless list nesting** — `<ol><ol><ol>` with `list-style-type: none`; flatten it
- Canvas rewrites internal links to `$CANVAS_COURSE_REFERENCE$` or `$IMS-CC-FILEBASE$`.
  Flag these rather than guessing the target.

Preserve the author's wording. Fix mechanical errors (typos, stale repo names, version
pins, platform mismatches) but do not rewrite pedagogy or restructure lessons.

## Known issues to watch for

- Course materials once referenced the old repo `ACCD_VIS4-24FA`. Current repo is
  `ACCD-IND671-VIS4`.
- Prefer "latest Current release" over pinned version numbers (Node, Arduino IDE) — they
  go stale every year.
- SSH instructions should use `ed25519` consistently on both Mac and Windows.
- Week 1's Windows section still reads "bind your mac computer" — needs fixing.

## Working style

- Report what you found before making sweeping changes; ask before restructuring.
- Commit in logical units with descriptive messages, not one giant commit.
- This repo lives in a OneDrive folder. If git reports lock or permission errors, pause
  OneDrive sync rather than retrying.
