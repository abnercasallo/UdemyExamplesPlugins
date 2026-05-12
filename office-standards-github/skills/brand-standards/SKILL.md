---
name: brand-standards
description: >
  Use this skill when the user asks "¿cuáles son las temáticas disponibles?", "muéstrame los colores",
  "¿qué fuentes debo usar?", "¿cuál tema va mejor con finanzas?", "ver guía de estilo",
  "brand guide", "estándares de diseño", "cuál es la paleta de colores", or any request
  to view, understand, or apply the visual identity rules of the office-standards plugin.
  Also use when the user needs to choose a theme before creating or editing a document.
metadata:
  version: "0.1.0"
---

# Brand Standards

Present and explain the four predefined visual themes available in the office-standards plugin. Help the user choose the right theme for their document and explain how to apply it consistently across PowerPoint, Word, and Excel.

## What to do

1. Load `references/brand-guide.md` to retrieve the full theme details and consistency rules.
2. Present the four themes with a brief description of their personality and best use case.
3. If the user asks to compare themes, show their primary and secondary colors side by side.
4. If the user asks which theme suits a specific purpose, recommend the appropriate one with a reason.
5. If the user wants to apply a theme, hand off to the `apply-theme` skill.

## Theme summary

| # | Theme                 | Primary     | Accent      | Best for                          |
|---|-----------------------|-------------|-------------|-----------------------------------|
| 1 | Corporativo Azul      | Navy #1B3A6B| Gold #C9A84C| Finance, executive, legal         |
| 2 | Oscuro Profesional    | Charcoal #2D2D2D | Electric Blue #4A9EFF | Sales, tech, pitches   |
| 3 | Claro Minimalista     | Teal #2D9C8C| Slate #4A5568| Reports, HR, operations           |
| 4 | Moderno Vivo          | Deep Purple #4B1A7D | Orange #FF6B35 | Marketing, creative campaigns |

## Consistency rules to communicate to the user

- Use the same theme number across all documents in a project (pptx + docx + xlsx must match).
- Primary color = headings, headers, title bars.
- Accent/secondary color = highlights, totals, call-to-action elements.
- Never mix primary and accent colors from different themes in the same document set.
- Font families should be consistent — if a font is not installed, use the designated fallback.

## Rules

- Always frame the brand standards as guidelines, not restrictions — the goal is consistency, not rigidity.
- If the user wants to add their own logo or custom colors on top of a theme, acknowledge this is fine and explain how it can coexist with the selected theme.
- When presenting themes, describe the visual feel in plain language, not just hex codes.
