# ACCD-IND671-VIS4

Course content for **IND-671 Visualization 4 (Vis Com 4)** — Graduate Industrial Design,
ArtCenter College of Design. Instructor: Jules Moretti.

This repo is the source of truth for Canvas page content. It is **not term-specific** —
the content here is the current version of the course, improved each year. Past terms
live in git history rather than in duplicated folders.

## Structure

```
content/
  week-01-.../
    reading.html      → Canvas page: "(Reading)"
    in-class.html     → Canvas page: "(In-Class Exercises)"
    assignment.html   → Canvas assignment
  _template/          → starting points for new weeks
syllabus/             → exported syllabus PDF per term
feedback/             → end-of-term feedback and the decisions it drove
```

## How the HTML files work

Each `.html` file is a **fragment**, not a full document — no `<html>`, `<head>`, or
`<body>` wrapper. Canvas pages expect body content only.

To publish: open the file, copy everything below the comment header, and paste it into
the Canvas HTML editor (the `</>` button in the rich content editor).

The comment header at the top of each file names the Canvas page it maps to. It is
stripped by Canvas on save, so it is safe to leave in.

## Yearly workflow

1. **Before the term** — read `feedback/` from last term, update the affected weeks,
   update the syllabus.
2. **During the term** — edit content in place as things change. Commit as you go so the
   reason for each change is captured in the message.
3. **After the term** — write `feedback/<TERM>-feedback.md`, then tag the commit:
   `git tag 26FA && git push --tags`. That gives you a permanent snapshot of exactly what
   was taught, without duplicating files.

## Naming conventions

- Week folders: `week-NN-short-kebab-case-title`
- Files: `reading.html`, `in-class.html`, `assignment.html`
- Extra material for a week goes in that week's folder with a descriptive name

## Related repos

- [ACCD-Fritzing-Parts](https://github.com/julesmoretti/ACCD-Fritzing-Parts) — Arduino
  component parts and Fritzing diagrams used in the second half of the term.
