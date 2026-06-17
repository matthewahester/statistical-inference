# statistical-inference

Public-facing Quarto **course-materials site** for an undergraduate
**Statistical Inference** course, assembled by Matt Hester. Sibling to
the main site [matthewhester.com](https://matthewhester.com); intended
to live at `/statistical-inference/` under that domain.

This is **assembled undergraduate course material** — synthesized lesson
notes, hands-on R/Quarto simulation labs, and curated references. It is a
durable public resource site, **not** a record of a currently scheduled
section, and **not** an LMS.

## Status

Assembled from a course-material build (2026-06). Topic flow, notes,
labs, and resources are in place. Dates, weights, and final policies are
not sealed and are authoritative in the LMS whenever the course runs.
Treat the site as a coherent draft, not a final release.

## What this site holds

- **Notes** — the weekly instructional spine (15 weeks, four parts): the
  inferential problem, sampling distributions and simulation, estimators
  and standard errors, bias/variance/MSE, likelihood and maximum
  likelihood, confidence intervals, hypothesis tests and p-values, error
  rates and power, the bootstrap, randomization/permutation tests,
  Bayesian inference, and comparing inferential frameworks.
- **Labs** — four reproducible R + Quarto labs (simulating sampling
  distributions, likelihood/MLE curves, bootstrap intervals, Bayesian
  updating by simulation).
- **Resources** — a notation glossary, a one-page inference reference
  laying the four frameworks side by side, and R/Quarto setup.

The notes are the course's **own synthesis**, grounded in (not copied
from) open sources: MIT OpenCourseWare 18.05 (CC BY-NC-SA 4.0),
*ModernDive* 2nd ed. (CC BY-NC-SA 4.0), and *Introduction to Modern
Statistics* 2nd ed. (CC BY-SA 3.0), attributed conservatively. All
example data are synthetic with seeds set.

## What does not go in this repo

Anything private to a graded offering: answer keys, assessment items,
rubrics, point values, due dates, student data, or any directory from
the private course build (`_state/`, `assessment_shadow/`,
`source_text/`, `run_reports/`, `accessibility/`). See
[`CLAUDE.md`](CLAUDE.md) for the full list. The operational, graded side
of any live offering lives in **Blackboard (the LMS)**, which is
authoritative.

## Local development

```bash
quarto render     # build to _site/
quarto preview    # live preview
```

R chunks in the notes and labs are written as **static, non-executed**
teaching code (` ```r ` fences), so the site renders **fully with plain
`quarto render` — no R installation required**.

## Layout

```
statistical-inference/
├── _quarto.yml              # site config, navbar, sidebar, render allow-list
├── index.qmd                # landing page (hero + overview)
├── syllabus.qmd             # public course overview
├── schedule.qmd             # week-by-week topic map
├── notes/                   # weekly instructional notes + index
├── labs/                    # reproducible R/Quarto simulation labs + index
├── resources/               # glossary, inference reference, setup + index
├── assets/                  # hero.png + icon.png (course identity art)
├── styles.css               # course-family palette
├── CLAUDE.md                # privacy + editing rules
└── README.md                # this file
```

No CI and no deploy pipeline in this repo. The combined site is
assembled and deployed by the hub repo (`matthewhester-site`). Local
builds only here; commits are deliberate and user-driven.
