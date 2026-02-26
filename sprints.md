Below is a **sprint plan optimized for fast execution (1–3 hours per sprint)**. Each sprint produces a working, testable increment. Follow in order. Do not skip.

---

# Portfolio Implementation — Sprint Plan

Total sprints: **7**
Total estimated time: **10–14 hours**

Each sprint ends in a **deployable, verifiable state**.

---

# Sprint 1 — Repository + Deployment Foundation

## Goal

Create repository, file structure, and deploy a blank site via GitHub Pages.

## Tasks

1. Create GitHub repository
2. Clone repo locally
3. Create required folders:

```
/assets/css/
/assets/images/
/content/projects/
```

4. Create files:

```
index.html
work.html
about.html
styles.css
README.md
```

5. Add basic HTML boilerplate to index.html:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Dhruvi Malusare Portfolio</title>
  <link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
  <h1>Portfolio</h1>
</body>
</html>
```

6. Commit and push

7. Enable GitHub Pages:
   Settings → Pages → Deploy from main branch

---

## Files touched

New:

```
index.html
work.html
about.html
assets/css/styles.css
README.md
```

---

## Acceptance Criteria

PASS if:

* Repo exists on GitHub
* GitHub Pages URL loads successfully
* index.html displays text “Portfolio”

FAIL if:

* 404 error
* Blank page
* CSS fails to load

---

## Verification Steps

Visit:

```
https://yourusername.github.io/repo-name
```

Confirm visible text.

---

## What NOT to do

DO NOT:

* Install frameworks
* Add animations
* Add fonts yet
* Add styling beyond basic

Goal is deployment only.

---

# Sprint 2 — Design System Foundation (Grid, Typography, Colors)

## Goal

Implement strict design system in CSS.

---

## Tasks

In styles.css, implement:

Typography:

```css
body {
  font-family: Inter, system-ui, sans-serif;
  background: #0F1115;
  color: #FFFFFF;
  font-size: 18px;
}
```

Container:

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 80px;
}
```

Headings:

```css
h1 { font-size: 64px; }
h2 { font-size: 40px; }
h3 { font-size: 28px; }
```

Spacing utility:

```css
.section {
  margin-top: 96px;
}
```

---

## Files touched

```
assets/css/styles.css
```

---

## Acceptance Criteria

PASS if:

* Background is dark
* Text is readable
* Layout centered

FAIL if:

* White background
* Inconsistent margins

---

## Verification Steps

Open homepage and visually confirm.

---

## What NOT to do

DO NOT:

* Add color variations
* Add multiple fonts
* Add responsive yet

---

# Sprint 3 — Navigation + Global Layout

## Goal

Add navbar and reusable layout structure.

---

## Tasks

Add navbar to all pages:

```html
<nav class="container">
  <a href="index.html">Home</a>
  <a href="work.html">Work</a>
  <a href="about.html">About</a>
</nav>
```

Wrap content in:

```html
<div class="container">
```

Add footer:

```html
<footer>
  <p>Email: your@email.com</p>
</footer>
```

---

## Files touched

```
index.html
work.html
about.html
```

---

## Acceptance Criteria

PASS if:

* Navbar visible on all pages
* Links work

FAIL if broken links

---

## Verification Steps

Click each nav link.

---

## What NOT to do

DO NOT:

* Add dropdowns
* Add animations
* Add icons

---

# Sprint 4 — Homepage Content Structure

## Goal

Build homepage credibility structure.

---

## Tasks

Add Hero:

```
Name
Role statement
CTA button
```

Add Featured Projects section:

Placeholder cards:

```
Project title
Impact metric
Link
```

Add About preview.

---

## Files touched

```
index.html
```

---

## Acceptance Criteria

PASS if homepage shows:

* Hero
* 3 project placeholders
* About preview

---

## Verification Steps

Reload homepage.

---

## What NOT to do

DO NOT:

* Add real projects yet
* Add styling complexity

---

# Sprint 5 — Project Content Model

## Goal

Create markdown project files.

---

## Tasks

Create:

```
content/projects/project1.md
```

Example:

```
title: Example Project
role: UX Designer
timeline: 4 weeks
impactMetric: +30% task success
```

Add content sections.

---

## Files touched

```
content/projects/
```

---

## Acceptance Criteria

PASS if markdown exists.

---

## Verification Steps

Open files locally.

---

## What NOT to do

DO NOT:

* Add more than 2 projects yet

---

# Sprint 6 — Work Page Project Listing

## Goal

Display project list on Work page.

---

## Tasks

Add project cards manually in work.html.

Each card:

```
Title
Metric
Link
```

---

## Files touched

```
work.html
```

---

## Acceptance Criteria

PASS if projects visible.

---

## Verification Steps

Visit /work.html

---

## What NOT to do

DO NOT:

* Automate parsing yet

Manual first.

---

# Sprint 7 — Case Study Page Template

## Goal

Create reusable case study layout.

---

## Tasks

Create:

```
project-example.html
```

Structure:

Executive summary
Problem
Research
Solution
Impact
Reflection

---

## Files touched

```
project-example.html
```

---

## Acceptance Criteria

PASS if page exists and readable.

---

## Verification Steps

Open in browser.

---

## What NOT to do

DO NOT:

* Overdesign
* Add animation

---

# Final Verification Checklist

Site must have:

* Working deployment
* Home page
* Work page
* Case study page
* About page
* Navigation working
* Fast load speed

---

# Result After Sprint 7

You will have:

Fully deployed
Recruiter-ready foundation
Easily expandable portfolio