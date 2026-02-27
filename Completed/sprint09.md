# agents.md — Portfolio Design System and Implementation Specification

## Purpose

This document defines the strict visual, structural, and implementation rules for the portfolio website. All coding agents must follow these specifications exactly. Do not introduce stylistic deviations, new design systems, or unapproved visual changes.

This system prioritizes clarity, elegance, and recruiter conversion.

---

# Global Design System

## Color System

Primary background colors:

```
Header background: #000000
Footer background: #FFFFFF
Main background: #FFFFFF
```

Primary text colors:

```
Primary text on black: #FFFFFF
Secondary text on black: #A1A1A1

Primary text on white: #000000
Secondary text on white: #525252
```

Button colors:

```
Primary button background: #FFFFFF
Primary button text: #000000
Primary button hover background: #E5E5E5
```

Divider colors:

```
Divider on black: #333333
Divider on white: #E5E5E5
```

No other colors are permitted.

---

# Typography System

## Font Families

Primary serif font (headings and name):

```
Playfair Display, serif
```

Primary sans-serif font (body and navigation):

```
Inter, system-ui, sans-serif
```

Font imports must include:

```
https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Playfair+Display:ital,wght@0,400;0,500;1,400&display=swap
```

---

## Font Hierarchy

Name / Identity:

```
Font: Playfair Display
Style: italic
Size: 20px header
Size: 36px footer
Weight: 400
```

Navigation:

```
Font: Inter
Size: 16px
Weight: 400
```

Body text:

```
Font: Inter
Size: 16px
Weight: 400
```

---

# Header Specification

## Layout

Header must include:

Left:

```
Dhruvi Malusare (serif, italic)
```

Right:

```
Resume
Work
Contact (button style)
```

## Header Visual Rules

Background:

```
#000000
```

Text colors:

```
Primary: #FFFFFF
Secondary: #A1A1A1
```

Contact button:

```
Background: #FFFFFF
Text: #000000
Border radius: 6px
Padding: 10px 18px
```

Spacing:

```
Horizontal padding: 40px
Vertical padding: 20px
```

Layout structure must use flexbox:

```
display: flex
justify-content: space-between
align-items: center
```

Header must remain fixed height based on padding.

Do not center logo.

Do not add shadows.

Do not add borders.

---

# Footer Specification

## Layout

Footer must include:

Left side:

```
Dhruvi Malusare (serif italic)
LinkedIn icon or link below
```

Right side:

Vertical navigation list:

```
Home
Work
Resume
Contact
```

Divider between left and right sections:

Vertical line.

---

## Footer Visual Rules

Background:

```
#FFFFFF
```

Text color:

```
#000000
```

Secondary text color:

```
#525252
```

Divider color:

```
#E5E5E5
```

Spacing:

```
Padding top and bottom: 80px
Padding left and right: 40px
```

Divider width:

```
1px
```

Divider height:

```
120px minimum
```

Layout must use flexbox.

---

# Layout Grid

Global horizontal spacing:

```
40px left and right padding
```

Maximum content width:

```
1200px
```

Center content container horizontally.

---

# Interaction Rules

Allowed hover effects:

Navigation links:

```
opacity 
```
