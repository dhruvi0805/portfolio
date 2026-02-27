Sprint 1 — Repository + Deployment Foundation
Goal
Create repository, file structure, and deploy a blank site via GitHub Pages.
Tasks
Create GitHub repository
Clone repo locally
Create required folders:
/assets/css/
/assets/images/
/content/projects/

Create files:
index.html
work.html
about.html
styles.css
README.md

Add basic HTML boilerplate to index.html:
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

Commit and push
Enable GitHub Pages:
Settings → Pages → Deploy from main branch

Files touched
New:
index.html
work.html
about.html
assets/css/styles.css
README.md


Acceptance Criteria
PASS if:
Repo exists on GitHub
GitHub Pages URL loads successfully
index.html displays text “Portfolio”
FAIL if:
404 error
Blank page
CSS fails to load

Verification Steps
Visit:
https://yourusername.github.io/repo-name

Confirm visible text.

What NOT to do
DO NOT:
Install frameworks
Add animations
Add fonts yet
Add styling beyond basic
Goal is deployment only.