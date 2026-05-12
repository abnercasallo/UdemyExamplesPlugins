---
name: apply-theme
description: >
  Use this skill when the user asks to "apply a theme", "cambiar el tema", "aplicar temática",
  "darle estilo a este documento", "hacer consistente el diseño", "aplicar colores corporativos",
  or any request to apply a visual standard or style to a PowerPoint, Word, or Excel file.
  Also triggers when the user says "quiero que mis documentos se vean iguales" or
  "aplicar la paleta de colores" to one or more documents.
metadata:
  version: "0.1.0"
---

# Apply Theme

Apply one of the four predefined visual themes to a PowerPoint (.pptx), Word (.docx), or Excel (.xlsx) document to ensure consistent branding across all office files.

## Available themes

Load `references/themes.md` to see the full color palettes, font specifications, and usage rules for each theme. The four themes are:

1. **Corporativo Azul** — Navy + White + Gold. Formal, trustworthy. Ideal for finance and executive presentations.
2. **Oscuro Profesional** — Charcoal + Off-white + Electric Blue. Modern, high-contrast. Ideal for tech and sales decks.
3. **Claro Minimalista** — White + Light Gray + Teal. Clean, open. Ideal for reports and operational documents.
4. **Moderno Vivo** — Deep Purple + Orange + White. Bold, energetic. Ideal for marketing and creative campaigns.

## Process

1. If no theme is specified, show the user the four options with their color descriptions and ask which one to use.
2. Identify the document type from the file extension or the user's description (.pptx / .docx / .xlsx).
3. Apply the theme using the appropriate skill:
   - For `.pptx` files: invoke the `pptx` skill with the theme's color and font specifications.
   - For `.docx` files: invoke the `docx` skill with the theme's heading colors, body font, and accent style.
   - For `.xlsx` files: invoke the `xlsx` skill with the theme's header fill color, accent color, and font.
4. If the user provides a file, read it first to understand its current structure before applying the theme.
5. Preserve all existing content — only change colors, fonts, and decorative elements.
6. Confirm with the user once the themed file is ready and offer to save it to Google Drive if they want.

## Output

Save the themed document to the user's workspace folder. Offer to:
- Save to Google Drive using available Drive tools.
- Apply the same theme to additional documents.

## Rules

- Never alter the content, data, or structure of the document — only visual styling.
- When applying to multiple documents at once, apply the exact same theme variant to all of them.
- If the file uses a company logo or custom colors not in the theme, ask the user whether to replace or preserve them.
