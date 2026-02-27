Sprint 2 — Design System Foundation (Grid, Typography, Colors)
Goal
Implement strict design system in CSS.

Tasks
In styles.css, implement:
Typography:
body {
  font-family: Inter, system-ui, sans-serif;
  background: #0F1115;
  color: #FFFFFF;
  font-size: 18px;
}

Container:
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 80px;
}

Headings:
h1 { font-size: 64px; }
h2 { font-size: 40px; }
h3 { font-size: 28px; }

Spacing utility:
.section {
  margin-top: 96px;
}


Files touched
assets/css/styles.css


Acceptance Criteria
PASS if:
Background is dark
Text is readable
Layout centered
FAIL if:
White background
Inconsistent margins

Verification Steps
Open homepage and visually confirm.

What NOT to do
DO NOT:
Add color variations
Add multiple fonts
Add responsive yet