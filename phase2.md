# Portfolio Implementation Specification
Version: 1.0
Owner: Dhruvi Malusare
Purpose: Build and deploy a static, recruiter-trust-optimized UX/Product portfolio.
Deployment Target: GitHub Pages
Architecture: Static site (no backend)

---------------------------------------------------------------------

# 1. System Overview

The system is a static portfolio website consisting of 4 pages:

1. Home
2. Work Index
3. Case Study Template
4. About

Optional:
5. Contact

The system must:

- Load in < 2 seconds on broadband
- Require no backend
- Deploy via GitHub Pages automatically on push to main branch
- Be editable via Markdown content files
- Follow strict grid, typography, and spacing rules

---------------------------------------------------------------------

# 2. Non-Goals (Scope Control)

The following MUST NOT be implemented:

- No CMS integration
- No backend server
- No authentication
- No user accounts
- No blog system
- No commenting system
- No animation libraries
- No database
- No dynamic rendering (SSR)
- No React, Vue, or frontend frameworks required
- No dark/light toggle
- No theme switching
- No analytics integration required for v1

This prevents scope creep.

---------------------------------------------------------------------

# 3. Technology Requirements

Required Stack:

- HTML5
- CSS3
- Markdown for content
- Git
- GitHub Pages deployment

Optional build tool allowed but NOT required:
- Astro

Forbidden dependencies:
- Node server runtime in production
- Backend frameworks

Output must be fully static.

---------------------------------------------------------------------

# 4. File Structure (Required)

Repository root must contain:

/
index.html
about.html
work.html
/contact.html (optional)

assets/
assets/css/styles.css
assets/images/

content/
content/projects/
content/projects/project-slug.md

README.md

---------------------------------------------------------------------

# 5. Content Model (Project)

Each project MUST exist as:

content/projects/project-slug.md

Required frontmatter:

---
title: string
subtitle: string
role: string
timeline: string
platform: string
summary: string
problem: string
solution: string
impactMetric: string
thumbnail: string
order: number
---

Required body sections:

## Problem
## Research
## Decisions
## Solution
## Impact
## Reflection

ACCEPTANCE CRITERIA:

FAIL if any field missing  
FAIL if Impact section empty  
PASS if all fields present  

---------------------------------------------------------------------

# 6. Design System Requirements

---------------------------------------------------------------------

Grid

Desktop:
- 12 column grid
- Max width: 1200px
- Margin: 80px left/right
- Gutter: 24px

Tablet:
- 8 column grid

Mobile:
- 4 column grid

Test Criteria:
PASS if layout aligns consistently
FAIL if inconsistent margins

---------------------------------------------------------------------

Spacing Scale (Strict)

Allowed spacing values ONLY:

8px
16px
24px
32px
48px
64px
96px

FAIL if any other spacing used

---------------------------------------------------------------------

Typography

Font stack:

Primary:
Inter, system-ui, sans-serif

Required sizes:

H1: 64px
H2: 40px
H3: 28px
Body: 18px
Caption: 14px

FAIL if inconsistent typography scale used

---------------------------------------------------------------------

Colors

Background: #0F1115
Surface: #161A20
Primary text: #FFFFFF
Secondary text: #9CA3AF
Accent: #3B82F6

FAIL if more than 1 accent color used

---------------------------------------------------------------------

# 7. Page Specifications

---------------------------------------------------------------------

7.1 Home Page (/index.html)

Required sections (in order):

1. Hero Section
Must include:
- Name
- Role statement
- CTA link to Work page

Acceptance Criteria:
PASS if visible above fold
FAIL if missing CTA

---

2. Credibility Strip

Must include minimum 3 metrics:

Example:
- Projects completed
- Usability tests conducted
- Tools used

Acceptance Criteria:
PASS if 3+ credibility items present

---

3. Featured Projects

Must display exactly 3 projects

Each must include:

- Title
- Thumbnail
- Impact metric
- Link to case study

FAIL if fewer than 3 shown

---

4. About Preview

Must include:

- Short bio
- Link to About page

PASS if link functional

---

5. Footer

Must include:

- Email
- LinkedIn link

PASS if links valid

---------------------------------------------------------------------

7.2 Work Page (/work.html)

Must display ALL projects from content/projects/

Each project must show:

- Thumbnail
- Title
- Impact metric
- Link

Acceptance Criteria:

PASS if all projects displayed  
FAIL if missing any project  

---------------------------------------------------------------------

7.3 Case Study Page

Generated from project markdown.

Required sections:

Executive Summary
Problem
Research
Decisions
Solution
Impact
Reflection

Acceptance Criteria:

PASS if all sections visible  
FAIL if any section missing  

---------------------------------------------------------------------

7.4 About Page (/about.html)

Required content:

- Name
- Role
- Bio paragraph (minimum 100 words)
- Skills list
- Resume link

Acceptance Criteria:

PASS if resume link works  
FAIL if resume missing  

---------------------------------------------------------------------

7.5 Contact Page (/contact.html) Optional

Must include:

- Email link (mailto:)

PASS if mailto opens email client  

---------------------------------------------------------------------

# 8. Navigation Requirements

Navbar must include:

- Home
- Work
- About
- Contact (optional)

Acceptance Criteria:

PASS if navigation visible on all pages  
PASS if links functional  

---------------------------------------------------------------------

# 9. Performance Requirements

Measured via Lighthouse:

Performance score ≥ 90

Page load ≤ 2 seconds

Image size ≤ 500kb each

FAIL if performance score < 80

---------------------------------------------------------------------

# 10. Deployment Specification

Deployment Platform:
GitHub Pages

Deployment Steps:

Step 1:
Initialize git repository

PASS if repository created

---

Step 2:
Push to GitHub main branch

PASS if code visible on GitHub

---

Step 3:
Enable GitHub Pages

Settings → Pages → Deploy from branch main

PASS if public URL generated

---

Step 4:
Verify deployment

PASS if site loads successfully  
FAIL if 404 error  

---

Step 5:
Verify updates deploy

Modify text → push commit

PASS if changes visible within 2 minutes  

---------------------------------------------------------------------

# 11. Accessibility Requirements

Minimum requirements:

- All images must include alt text
- Contrast ratio must meet WCAG AA

PASS if alt text present  
FAIL if missing alt text  

---------------------------------------------------------------------

# 12. Responsiveness Requirements

Must function at widths:

320px
768px
1024px
1440px

PASS if layout intact  
FAIL if overflow or broken layout  

---------------------------------------------------------------------

# 13. Completion Criteria (Definition of Done)

The implementation is complete ONLY if:

- All pages exist
- All acceptance criteria pass
- Site deploys via GitHub Pages
- Site loads < 2 seconds
- All project content renders correctly

---------------------------------------------------------------------

# END SPEC