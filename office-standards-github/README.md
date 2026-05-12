# Office Standards Plugin

Gestiona un estándar visual unificado para todos tus documentos de Office. Aplica temáticas consistentes entre PowerPoint, Word y Excel, y genera documentos desde plantillas por dominio (finanzas, marketing, ventas, RRHH).

---

## Componentes

### Skills

| Skill               | Descripción                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| `apply-theme`       | Aplica una de las cuatro temáticas predefinidas a cualquier documento (pptx, docx, xlsx) |
| `create-from-template` | Genera documentos nuevos desde plantillas por dominio con la temática elegida |
| `brand-standards`   | Muestra y explica las temáticas disponibles, sus colores, fuentes y reglas de uso |

### Agente

| Agente                     | Descripción                                                                           |
|----------------------------|---------------------------------------------------------------------------------------|
| `document-package-builder` | Genera un paquete completo de tres documentos (pptx + docx + xlsx) con temática uniforme |

---

## Temáticas disponibles

| # | Nombre              | Primario          | Acento            | Mejor para                        |
|---|---------------------|-------------------|-------------------|-----------------------------------|
| 1 | Corporativo Azul    | Navy `#1B3A6B`    | Gold `#C9A84C`    | Finanzas, ejecutivo, legal        |
| 2 | Oscuro Profesional  | Charcoal `#2D2D2D`| Blue `#4A9EFF`    | Ventas, tech, pitches             |
| 3 | Claro Minimalista   | Teal `#2D9C8C`    | Slate `#4A5568`   | Reportes, RRHH, operaciones       |
| 4 | Moderno Vivo        | Purple `#4B1A7D`  | Orange `#FF6B35`  | Marketing, campañas creativas     |

---

## Plantillas disponibles

### Finanzas
- Reporte financiero (docx)
- Dashboard de presupuesto (xlsx)
- Presentación ejecutiva (pptx)

### Marketing
- Brief de campaña (docx)
- Dashboard de métricas (xlsx)
- Deck de campaña (pptx)

### Ventas
- Propuesta comercial (docx)
- Tracker de cotizaciones (xlsx)
- Deck de ventas (pptx)

### Operaciones / RRHH
- Manual de proceso (docx)
- Tracker de RRHH (xlsx)
- Presentación de onboarding (pptx)

---

## Configuración

### Google Drive y Gmail

Este plugin usa los conectores de Google Workspace y Gmail ya configurados en Cowork. Para que las skills puedan guardar documentos en Drive y enviarlos por Gmail, asegúrate de tener ambos conectores activos en la configuración de Cowork.

No se requieren variables de entorno adicionales — la autenticación se gestiona a través de los conectores de Cowork.

---

## Cómo usar

### Aplicar una temática a un documento existente
> "Aplica el tema Corporativo Azul a este archivo"
> "Quiero que este PowerPoint tenga el tema Moderno Vivo"
> "Cambia los colores de este Excel para que sea consistente con mis otros documentos"

### Crear un documento desde plantilla
> "Crea una propuesta comercial para un cliente nuevo"
> "Genera el dashboard de presupuesto para Q2 2026"
> "Necesito un deck de marketing para la campaña de verano"

### Ver las temáticas disponibles
> "Muéstrame las temáticas disponibles"
> "¿Cuál tema va mejor para una presentación de finanzas?"
> "¿Cuáles son los colores del tema Claro Minimalista?"

### Generar un paquete completo
> "Necesito los tres documentos para la revisión trimestral"
> "Arma el paquete completo de ventas con el mismo estilo"
> "Genera la presentación, el reporte y el Excel para el proyecto, todo igual"

---

## Personalización

Para agregar tus propios colores o logo sobre una de las temáticas, simplemente díselo a Claude al momento de generar o aplicar el tema. Las temáticas son una base — siempre puedes extenderlas con tu identidad de marca.
