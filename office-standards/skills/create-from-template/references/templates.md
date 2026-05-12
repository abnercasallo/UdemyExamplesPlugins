# Template Reference — Office Standards

Detailed structure for each domain template. Use this reference when generating a document from template.

---

## FINANZAS

### reporte-financiero (docx)

**Purpose**: Monthly or quarterly financial results report for internal or executive distribution.

**Sections:**
1. Cover page — Company name, period (e.g., "Reporte Financiero Q1 2026"), prepared by, date
2. Resumen ejecutivo — 3–5 bullet points of key financial highlights
3. Estado de resultados — Table: Ingresos, Costo de ventas, Utilidad bruta, Gastos operativos, EBITDA, Utilidad neta. Columns: Período actual, Período anterior, Variación ($), Variación (%)
4. Análisis de varianza — Narrative explanation of major variances (>5%)
5. Ingresos por segmento — Table or chart breaking down revenue by product/service/region
6. Gastos por categoría — Table of opex breakdown
7. Flujo de caja — Summary: Actividades de operación, inversión, financiamiento, Caja neta
8. Indicadores clave (KPIs) — ROE, ROA, Margen bruto, Margen EBITDA, Razón corriente
9. Próximos pasos — Actions and owners for the next period

**Placeholder labels**: `[Nombre empresa]`, `[Período]`, `[Preparado por]`, `[Moneda]`, `[Monto]`

---

### dashboard-presupuesto (xlsx)

**Purpose**: Budget vs. actuals tracker with monthly breakdown and automated variance calculations.

**Sheets:**
1. **Resumen** — Dashboard with KPI cards (total budget, total actuals, variance %, burn rate) and summary chart
2. **Presupuesto vs Real** — Rows: expense/revenue categories. Columns: Presupuesto Ene–Dic, Real Ene–Dic, Variación $, Variación %, Semáforo (formula-driven: green ≤5%, yellow 5–15%, red >15%)
3. **Gastos detalle** — Transaction-level log: Fecha, Categoría, Descripción, Monto, Mes
4. **Ingresos detalle** — Revenue transaction log: Fecha, Fuente, Descripción, Monto, Mes
5. **Gráficas** — Bar chart (budget vs actual by month), pie chart (spend by category), line chart (cumulative actuals vs budget)

**Key formulas to include:**
- Variación $: `=Real - Presupuesto`
- Variación %: `=IF(Presupuesto=0,"N/A",(Real-Presupuesto)/ABS(Presupuesto))`
- Semáforo: `=IF(ABS(Var%)<=5%,"🟢",IF(ABS(Var%)<=15%,"🟡","🔴"))`
- Totals: `=SUM(range)` for all numeric columns
- YTD actuals: `=SUMIF(month_col,"<="&current_month, amount_col)`

---

### presentacion-ejecutiva (pptx)

**Purpose**: Financial results deck for board or senior leadership (8–12 slides).

**Slide structure:**
1. Cover — Title, period, company name, logo placeholder
2. Agenda — 4–5 topics listed
3. Resumen ejecutivo — 3 key callout boxes (Revenue, EBITDA, Net Income) with vs. prior period arrows
4. Ingresos — Bar chart by month, table with actuals vs. budget
5. Márgenes — Line chart of gross margin and EBITDA margin trend
6. Gastos — Waterfall chart or stacked bar of opex breakdown
7. Flujo de caja — 3-column layout: Operational / Investment / Financing cash flow
8. KPIs en semáforo — Grid of 6–8 KPIs with green/yellow/red status
9. Outlook — Forward-looking narrative + key risks
10. Próximos pasos — Action items table with Owner and Due Date columns
11. Appendix cover (optional)

---

## MARKETING

### brief-campana (docx)

**Purpose**: Full campaign brief document to align team and stakeholders before execution.

**Sections:**
1. Cover page — Campaign name, brand, date, brief owner
2. Contexto y antecedentes — Why this campaign? What problem does it solve?
3. Objetivos — Business objective, marketing objective, communication objective (SMART format)
4. Audiencia objetivo — Primary and secondary audience, persona description, behaviors
5. Mensaje central — Single-minded proposition, reason to believe, tone of voice
6. Canales y medios — Table: Channel, Format, Budget %, Dates, KPI
7. KPIs y métricas — Reach, Impressions, CTR, Conversions, CAC, ROAS
8. Calendario — Timeline table: Phase, Activities, Start, End, Owner
9. Presupuesto — Budget summary table by channel
10. Aprobaciones — Signature table: Role, Name, Date

---

### dashboard-metricas (xlsx)

**Purpose**: Marketing metrics tracker across channels with automated performance summary.

**Sheets:**
1. **Resumen** — KPI summary cards: Alcance total, Impresiones, CTR promedio, Conversiones, CAC, ROAS. Mini-charts per KPI.
2. **Métricas por canal** — Rows: channels (Social, Email, SEM, Display, Influencer). Columns: Inversión, Alcance, Impresiones, Clics, CTR, Conversiones, CPC, CAC, ROAS
3. **Redes sociales** — Daily/weekly metrics: Fecha, Plataforma, Publicaciones, Alcance orgánico, Alcance pagado, Engagement, Seguidores nuevos
4. **Email marketing** — Campaña, Fecha envío, Lista, Enviados, Abiertos, Tasa apertura, Clics, Tasa clic, Bajas
5. **Gráficas** — Channel comparison bar chart, conversion funnel, ROAS by channel

**Key formulas:**
- CTR: `=Clics/Impresiones`
- CAC: `=Inversión/Conversiones`
- ROAS: `=Ingresos_atribuidos/Inversión`
- Tasa apertura: `=Abiertos/Enviados`

---

### deck-campana (pptx)

**Purpose**: Campaign presentation for client approval or internal kickoff (10–14 slides).

**Slide structure:**
1. Cover — Campaign name, brand logo, tagline placeholder
2. El reto — Problem/opportunity statement (full-bleed visual slide)
3. Objetivo — 1 clear campaign objective in large type
4. Audiencia — Persona card(s) with demographic + psychographic snapshot
5. Concepto creativo — Big idea + 3 pillars of the concept
6. Mensaje clave — Single-minded proposition in bold type
7. Estrategia de canales — Channel mix diagram or table
8. Plan de contenidos — Content calendar grid (month view)
9. Presupuesto — Donut chart of budget by channel
10. Cronograma — Gantt-style timeline
11. KPIs y medición — Metrics dashboard mockup
12. Próximos pasos — 3–5 action items with owners
13. Thank you / Questions slide

---

## VENTAS

### propuesta-comercial (docx)

**Purpose**: Formal sales proposal sent to a prospect or client.

**Sections:**
1. Cover page — "Propuesta Comercial", client name, prepared by, date, validity period
2. Carta de presentación — Brief, personalized introductory letter
3. Entendimiento del cliente — Summary of the client's challenge/need
4. Nuestra propuesta — Solution description (what, how, why us)
5. Alcance del proyecto — Detailed scope of work table: Fase, Actividades, Entregables, Duración
6. Metodología — Process overview (diagram or numbered steps)
7. Equipo — Team members table: Rol, Nombre, Experiencia
8. Casos de éxito — 2–3 client references or case summaries
9. Inversión — Pricing table: Concepto, Cantidad, Precio unitario, Total. Subtotal, IVA, Total.
10. Condiciones comerciales — Payment terms, validity, deliverable timelines
11. Próximos pasos — Acceptance process and contact
12. Firma y aceptación — Signature block

---

### cotizacion-tracker (xlsx)

**Purpose**: Pipeline and quotation tracker to manage all open commercial opportunities.

**Sheets:**
1. **Pipeline** — Oportunidad, Cliente, Contacto, Monto estimado, Etapa (Prospecto/Propuesta/Negociación/Cerrado/Perdido), Probabilidad %, Monto ponderado, Fecha estimada cierre, Próximo paso, Owner
2. **Cotizaciones** — Cotización #, Cliente, Fecha, Vigencia, Concepto, Subtotal, IVA, Total, Estado (Enviada/Aceptada/Rechazada/Vencida)
3. **Resumen pipeline** — Summary cards: Total pipeline, Ponderado, Cotizaciones enviadas, Tasa de cierre %. Chart: pipeline by stage.
4. **Seguimiento** — Log of follow-up activities: Fecha, Cliente, Tipo de contacto, Resultado, Próximo paso, Fecha próximo contacto

**Key formulas:**
- Monto ponderado: `=Monto * Probabilidad/100`
- Tasa de cierre: `=COUNTIF(etapa,"Cerrado")/COUNTA(etapa)`
- Pipeline total: `=SUMIF(etapa,"<>Perdido",monto)`

---

### deck-ventas (pptx)

**Purpose**: Commercial pitch deck for prospect meetings or demos (8–12 slides).

**Slide structure:**
1. Cover — Company name, tagline, logo
2. El problema que resolvemos — Pain point (visual, 1 sentence)
3. Nuestra solución — What we do in 3 bullets or icons
4. Cómo funciona — 3–4 step process (icons + short descriptions)
5. Propuesta de valor — 3 differentiators vs. competition
6. Casos de éxito — 2 client results with metrics
7. Clientes y alianzas — Logo grid of key clients/partners
8. Planes y precios — Pricing table (3 tiers recommended)
9. El equipo — Headshots + titles
10. Garantía / compromiso — Risk-reversal statement
11. Próximos pasos — 3 simple steps to get started + CTA
12. Contacto — Contact info, social handles

---

## OPERACIONES / RRHH

### manual-proceso (docx)

**Purpose**: Internal process documentation for operations, compliance, or training.

**Sections:**
1. Cover page — Process name, version, owner, effective date, approved by
2. Objetivo del proceso — Purpose and scope
3. Alcance — What is included and excluded
4. Definiciones — Glossary of key terms
5. Responsables — RACI matrix: Actividad, Responsable, Aprobador, Consultado, Informado
6. Descripción del proceso — Step-by-step: Paso #, Actividad, Descripción, Responsable, Herramienta/Sistema, Tiempo estimado
7. Diagrama de flujo — Flow diagram placeholder (describe steps; Claude can generate using shapes)
8. Excepciones y escalamiento — What to do when the process can't be followed as documented
9. Métricas de desempeño — KPIs to measure process effectiveness
10. Control de cambios — Version history table: Versión, Fecha, Autor, Cambios realizados

---

### tracker-rrhh (xlsx)

**Purpose**: HR management tracker for headcount, vacations, evaluations, and key dates.

**Sheets:**
1. **Directorio** — ID, Nombre completo, Puesto, Área, Gerente, Tipo contrato, Fecha ingreso, Antigüedad (formula), Email, Extensión, Estado (Activo/Baja)
2. **Vacaciones** — Empleado, Días disponibles, Días tomados, Días restantes (formula), Solicitudes pendientes, Próximas vacaciones fecha
3. **Evaluaciones** — Empleado, Período evaluación, Fecha evaluación, Evaluador, Calificación (1–5), Comentarios, Plan de desarrollo, Fecha próxima revisión
4. **Fechas clave** — Tipo (cumpleaños/aniversario/vencimiento contrato/renovación), Empleado, Fecha, Días para el evento (formula), Acción requerida
5. **Resumen RRHH** — KPI cards: Total headcount, Nuevos este mes, Bajas este mes, Ausentismo %, Días vacaciones pendientes. Chart: headcount by área.

**Key formulas:**
- Antigüedad: `=DATEDIF(fecha_ingreso,TODAY(),"Y")&" años, "&DATEDIF(fecha_ingreso,TODAY(),"YM")&" meses"`
- Días restantes vacaciones: `=Disponibles - Tomados`
- Días para evento: `=DATE(YEAR(TODAY()),MONTH(fecha),DAY(fecha)) - TODAY()`

---

### presentacion-onboarding (pptx)

**Purpose**: Welcome and induction deck for new team members (10–15 slides).

**Slide structure:**
1. Cover — "Bienvenido/a a [Empresa]", new hire name (optional), start date
2. Nuestra historia — Founded, mission, key milestones timeline
3. Misión, visión y valores — 3-column layout with icons
4. Estructura organizacional — Org chart
5. Tu equipo — Team member cards with photos placeholder, name, and role
6. Tu rol — Job title, key responsibilities, success metrics for first 90 days
7. Primeras semanas — 30/60/90 day plan table
8. Herramientas y sistemas — Tools you'll use (icons + brief description)
9. Procesos clave — Top 3–5 processes the new hire needs to know
10. Beneficios — Benefits summary (vacation days, health, perks, etc.)
11. Cultura y eventos — Team rituals, recurring events, communication norms
12. Recursos y contactos clave — Who to contact for IT, HR, Finance, etc.
13. Preguntas frecuentes — FAQ (top 5–8 questions)
14. Próximos pasos — Checklist for first week
15. ¡Bienvenido/a al equipo! — Closing slide with team photo placeholder
