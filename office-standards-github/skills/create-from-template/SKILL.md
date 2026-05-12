---
name: create-from-template
description: >
  Use this skill when the user asks to "crear documento desde plantilla", "generar un reporte",
  "hacer una propuesta comercial", "crear un presupuesto", "armar un deck de marketing",
  "quiero una plantilla de finanzas", "crear documento de RRHH", "generar cotización",
  "plantilla de ventas", or any request to create a new Office document (pptx, docx, xlsx)
  based on a predefined domain template (finanzas, marketing, ventas, operaciones, RRHH).
metadata:
  version: "0.1.0"
---

# Create from Template

Generate a new, ready-to-use Office document based on a predefined domain template. Each template is pre-structured with the right sections, tables, and layouts for its purpose — the user only needs to fill in their specific data.

## Template domains

Load `references/templates.md` for the full structure of each template. The available domains and their documents are:

**Finanzas:**
- `reporte-financiero` (docx) — Estado de resultados mensual/trimestral con análisis de varianza
- `dashboard-presupuesto` (xlsx) — Presupuesto vs. real con fórmulas y gráficas
- `presentacion-ejecutiva` (pptx) — Deck de resultados financieros para dirección

**Marketing:**
- `brief-campana` (docx) — Brief completo de campaña con objetivos, audiencia y KPIs
- `dashboard-metricas` (xlsx) — Tracker de métricas de marketing con visualizaciones
- `deck-campana` (pptx) — Presentación de campaña lista para cliente o dirección

**Ventas:**
- `propuesta-comercial` (docx) — Propuesta de venta estructurada con alcance y condiciones
- `cotizacion-tracker` (xlsx) — Seguimiento de cotizaciones con estado y montos
- `deck-ventas` (pptx) — Deck de presentación de ventas / pitch comercial

**Operaciones / RRHH:**
- `manual-proceso` (docx) — Documentación de proceso con pasos, responsables y excepciones
- `tracker-rrhh` (xlsx) — Seguimiento de personal, vacaciones, evaluaciones
- `presentacion-onboarding` (pptx) — Deck de bienvenida/inducción para nuevos integrantes

## Process

1. Identify the domain (finanzas, marketing, ventas, operaciones/RRHH) and document type (docx, xlsx, pptx) from the user's request.
2. If both are unclear, ask the user to choose the domain first, then the document type.
3. Load `references/templates.md` to retrieve the exact structure for the requested template.
4. Ask which visual theme to apply (Corporativo Azul, Oscuro Profesional, Claro Minimalista, or Moderno Vivo). If not specified, recommend the most suitable theme for the domain.
5. Ask for any specific data to pre-populate (company name, period, amounts, names, etc.). If the user has no data yet, create the template with placeholder text.
6. Generate the document using the appropriate skill:
   - `.pptx` → invoke the `pptx` skill
   - `.docx` → invoke the `docx` skill
   - `.xlsx` → invoke the `xlsx` skill
7. Apply the chosen theme's colors, fonts, and styles as defined in `apply-theme/references/themes.md`.
8. Save the file to the workspace folder and offer to upload to Google Drive.

## Theme recommendations by domain

| Domain       | Recommended theme       | Reason                            |
|--------------|-------------------------|-----------------------------------|
| Finanzas     | Corporativo Azul        | Formal, trustworthy feel          |
| Marketing    | Moderno Vivo            | Bold, energetic, creative         |
| Ventas       | Oscuro Profesional      | Impactful, modern pitch feel      |
| RRHH / Ops   | Claro Minimalista       | Clear, friendly, easy to read     |

## Rules

- Always include a professional cover page or title section in every document.
- Pre-populate section headings and table structure; leave data cells with clear placeholder labels (e.g., `[Nombre del cliente]`, `[Monto Q1]`).
- For xlsx templates, include working Excel formulas (SUM, IF, VLOOKUP, etc.) wherever appropriate.
- Never generate dummy financial numbers that could be mistaken for real data — use clearly labeled placeholders.
- After generation, confirm what was created and offer to apply the same template to another document type.
