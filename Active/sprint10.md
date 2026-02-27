# AGENT.md — Portfolio Implementation Specification

Version: 1.0
Owner: Dhruvi Malusare
Deployment Target: GitHub Pages
Architecture: Fully static site (no backend)
Agent Role: Deterministically implement this portfolio with ZERO deviation.

---

# 0. PRIMARY OBJECTIVE

Build a fully static, premium editorial-grade product portfolio website optimized for recruiter trust, startup hiring managers, and product leadership roles.

The output must:

* Be fully static HTML/CSS
* Deploy via GitHub Pages
* Require zero backend
* Require zero runtime dependencies
* Load in < 2 seconds
* Be editable via Markdown content files
* Follow the exact design system defined below

Agent MUST NOT improvise design decisions.

---

# 1. HARD CONSTRAINTS

These constraints override all other decisions.

## Forbidden

DO NOT implement:

* React
* Vue
* Angular
* Node server
* Express
* Databases
* Authentication
* CMS integration
* Analytics
* Animations libraries
* Tailwind
* Bootstrap
* UI frameworks
* Theme toggles
* Blog systems
* Comment systems

Site must be static HTML + CSS only.

---

## Allowed

HTML5
CSS3
Markdown (content source)
Optional: static pre-generation of HTML from markdown

NO runtime markdown parsing in browser.

---

# 2. FILE STRUCTURE (MANDATORY)

Agent MUST create exactly this structure:

```
/
index.html
work.html
about.html
contact.html

/projects/
wayfinding.html
thrive.html
researchgate.html

/assets/css/styles.css
/assets/images/

/content/projects/
wayfinding.md
thrive.md
researchgate.md

README.md
AGENT.md
```

FAIL if structure differs.

---

# 3. DESIGN SYSTEM (STRICT)

Agent MUST implement EXACTLY.

---

## 3.1 Color System

```
--color-background: #0F1115;
--color-surface: #161A20;
--color-text-primary: #FFFFFF;
--color-text-secondary: #9CA3AF;
--color-accent: #E5E7EB;
--color-border: #1F2933;
```

Background usage:

```
body background: #0F1115
cards background: #161A20
```

FAIL if additional accent colors introduced.

---

## 3.2 Gradient Rules (Strict)

Allowed locations ONLY:

Hero background:

```
linear-gradient(180deg, #0F1115 0%, #12151B 100%)
```

Hover states ONLY:

```
linear-gradient(90deg, #FFFFFF 0%, #9CA3AF 100%)
```

Forbidden:

* colorful gradients
* animated gradients
* gradient text

---

## 3.3 Typography System

Headings Font:

```
"Instrument Serif", "Playfair Display", Georgia, serif
```

Body Font:

```
Inter, system-ui, sans-serif
```

Agent MUST include Google Fonts import.

---

Typography scale (STRICT):

```
H1: 64px
H2: 40px
H3: 28px
Body: 18px
Caption: 14px
```

FAIL if inconsistent.

---

## 3.4 Spacing System (STRICT)

Allowed spacing ONLY:

```
8px
16px
24px
32px
48px
64px
96px
```

FAIL if any other spacing used.

---

## 3.5 Layout Grid

Desktop:

```
max-width: 1200px
margin-left/right: auto
padding-left/right: 80px
```

Tablet:

```
padding-left/right: 32px
```

Mobile:

```
padding-left/right: 16px
```

---

# 4. GLOBAL COMPONENTS

Agent MUST implement reusable components using HTML/CSS patterns.

---

## 4.1 Navbar

Structure:

Left:

```
Dhruvi Malusare
```

Right:

```
Work
About
Contact
```

Behavior:

Sticky top
Height: 64px

Scroll state:

```
background: rgba(15,17,21,0.8)
backdrop-filter: blur(10px)
```

---

## 4.2 Footer

Structure:

Left:

```
Dhruvi Malusare
```

Right:

```
drm23@njit.edu
LinkedIn (placeholder)
```

Background:

```
#0F1115
border-top: 1px solid #1F2933
```

---

# 5. PAGE IMPLEMENTATION

Agent MUST implement ALL pages.

---

# 5.1 Home Page — index.html

Sections in EXACT order:

---

Hero Section

Must include:

```
H1: Dhruvi Malusare

Body:
I'm an aspiring Product Manager with a background in User Experience Design, Product Design, 3D Design & Animation and a strong interest in Data Analytics

CTA Button:
View Work → /work.html
```

Hero height:

```
min-height: 80vh
```

Gradient background applied.

---

Credibility Strip

3 items placeholders:

```
X Projects Completed
X User Interviews Conducted
X Usability Tests Run
```

---

Featured Projects Section

Must show EXACTLY 3 projects:

Order:

1. Wayfinding
2. Thrive
3. Researchgate

Each card must include:

```
Project title
Thumbnail placeholder
Impact metric placeholder
Link → project page
```

---

About Preview Section

Placeholder paragraph.

Link:

```
Read More → /about.html
```

---

Footer

Required.

---

# 5.2 Work Page — work.html

Must show ALL projects.

Each item includes:

```
Title
Thumbnail placeholder
Impact metric placeholder
Link
```

Order must match project order.

---

# 5.3 Project Pages

Must create:

```
/projects/wayfinding.html
/projects/thrive.html
/projects/researchgate.html
```

Template structure:

```
Project Title
Subtitle placeholder

Role placeholder
Timeline placeholder
Platform placeholder

Executive Summary

Problem
Research
Decisions
Solution
Impact
Reflection
```

Use clean vertical reading layout.

---

# 5.4 About Page — about.html

Must include:

```
Dhruvi Malusare

Role statement

Bio placeholder paragraph (100+ words)

Skills:

Product Management
UX Design
Product Design
Data Analytics
3D Design & Animation

Resume link placeholder
```

---

# 5.5 Contact Page — contact.html

Must include:

```
Email:
drm23@njit.edu

LinkedIn placeholder
```

---

# 6. CSS IMPLEMENTATION REQUIREMENTS

Agent MUST implement single stylesheet:

```
/assets/css/styles.css
```

Must include:

Typography system
Layout system
Navbar
Footer
Cards
Buttons
Responsive rules

---

# 7. RESPONSIVENESS REQUIREMENTS

Must function correctly at:

```
320px
768px
1024px
1440px
```

No overflow allowed.

---

# 8. PERFORMANCE REQUIREMENTS

Lighthouse minimum scores:

```
Performance ≥ 90
Accessibility ≥ 95
Best Practices ≥ 95
SEO ≥ 95
```

Page load:

```
< 2 seconds
```

---

# 9. ACCESSIBILITY REQUIREMENTS

Agent MUST ensure:

All images include alt text
Proper semantic HTML used

Use:

```
<header>
<nav>
<main>
<section>
<footer>
```

---

# 10. DEPLOYMENT REQUIREMENTS

Agent MUST ensure compatibility with GitHub Pages.

Deployment steps:

```
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin <repo>
git push -u origin main
```

Enable GitHub Pages:

Settings → Pages → Deploy from main branch.

---

# 11. ACCEPTANCE CRITERIA

Implementation is COMPLETE only if:

All required pages exist
All pages load without errors
All navigation links function
CSS applied correctly
Site loads under 2 seconds
No console errors
Deploys successfully on GitHub Pages

FAIL otherwise.

---

# 12. DESIGN PHILOSOPHY (CRITICAL)

Visual tone MUST communicate:

Premium
Minimal
Editorial
Analytical
Product-focused
Startup-ready

Must resemble:

Apple
Stripe
Linear
Notion

Must NOT resemble:

student portfolios
templates
Dribbble-heavy visuals

---

# 13. EXECUTION ORDER (MANDATORY)

Agent MUST execute in this exact order:

1. Create folder structure
2. Create styles.css
3. Create navbar + footer
4. Create index.html
5. Create work.html
6. Create project pages
7. Create about.html
8. Create contact.html
9. Validate responsiveness
10. Validate performance

---

# END OF SPECIFICATION
