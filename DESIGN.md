---
name: CristalesGraf
description: Sistema de diseño para vidriería técnica y carpintería de aluminio en Lima
colors:
  primary: "#00529c"
  primary-dark: "#002d5a"
  primary-light: "#0066b8"
  accent-cyan: "#00b4d8"
  accent-cyan-light: "#e0f2fe"
  accent-action: "#25d366"
  accent-action-hover: "#16a34a"
  neutral-dark: "#0f172a"
  neutral-black: "#000000"
  neutral-text: "#0f172a"
  neutral-muted: "#64748b"
  neutral-border: "#cbd5e1"
  neutral-bg: "#f8fafc"
  surface-white: "#ffffff"
typography:
  display:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(2.5rem, 5vw, 3.5rem)"
    fontWeight: 700
    lineHeight: 1.08
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(1.85rem, 3.5vw, 2.5rem)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(1.35rem, 2.5vw, 1.75rem)"
    fontWeight: 700
    lineHeight: 1.25
  body:
    fontFamily: "IBM Plex Sans, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "0.75rem"
    fontWeight: 700
    letterSpacing: "0.05em"
rounded:
  sm: "2px"
  md: "4px"
  lg: "8px"
  full: "9999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  2xl: "48px"
components:
  button-whatsapp:
    backgroundColor: "{colors.accent-action}"
    textColor: "{colors.neutral-text}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface-white}"
    rounded: "{rounded.md}"
    padding: "10px 18px"
---

# Design System: CristalesGraf

## Overview

**Creative North Star: "La Ficha de Rectificación y Control Técnico"**

El lenguaje visual de CristalesGraf rechaza el catálogo comercial genérico de fotos de stock y degradados vacíos. Está inspirado en la honestidad del taller industrial de manufactura y en el cuaderno de obra del contratista en Lima: líneas de ensamble limpias, perfiles de aluminio extruido, cristal templado translúcido y la precisión milimétrica requerida antes del templado térmico bajo la Norma Técnica Peruana E.040.

La paleta cromática se deriva fielmente de la identidad corporativa plasmada en su logotipo oficial (`logo.png`): el **Azul Corporativo CristalesGraf** (`#00529c`), el destello **Cyan Cristal** (`#00b4d8`) de los paneles de vidrio en cascada, la sobriedad del negro/grafito arquitectónico (`#0f172a`) de los perfiles de aluminio, y el verde de conversión directa a WhatsApp (`#25d366`).

La experiencia prioriza la claridad técnica, la autoridad inmediata (+18 años en Los Olivos, respaldo de Corporación Limatambo) y la reducción total de fricción en la cotización mediante componentes interactivos que enrutan datos precalificados directamente a WhatsApp.

**Key Characteristics:**
- Autoridad sobria y técnica sobre fondos limpios de taller (`#f8fafc`).
- Contraste institucional contundente en Azul Corporativo (`#00529c`) y Cyan Cristal (`#00b4d8`) extraídos del logotipo oficial, con acentos de conversión en verde esmeralda WhatsApp (`#25d366`).
- Tipografía dual: geometría sólida para encabezados (`Space Grotesk`), lectura clara para cuerpo (`IBM Plex Sans`) y notación tabular para cotas y medidas (`IBM Plex Mono`).
- Contenedores limpios sin anidamientos innecesarios ni tarjetas dentro de tarjetas.

## Colors

Paleta arquitectónica y técnica derivada del logotipo oficial de CristalesGraf (`logo.png`), dominada por el Azul Corporativo CristalesGraf (`#00529c`), el Cyan Cristal translúcido (`#00b4d8`) y neutros de taller, con verde esmeralda reservado estrictamente para acciones de cotización y WhatsApp.

### Primary
- **Azul Corporativo CristalesGraf** (`#00529c`): Extraído de la tipografía y panel base del logotipo oficial. Estructura primaria de marca, encabezados, bordes principales de componentes técnicos y botones de navegación.
- **Azul Taller Profundo** (`#002d5a`): Fondos de pie de página y barras de autoridad superior.
- **Azul Interactivo / Hover** (`#0066b8`): Estado hover de enlaces y botones primarios.

### Secondary
- **Cyan Cristal / Celeste Luminoso** (`#00b4d8`): Extraído del panel superior de cristal del logotipo. Simboliza la refracción y pureza óptica del cristal templado de seguridad. Se utiliza en badges técnicos, acentos visuales y micro-detalles.
- **Hielo Cristal Translúcido** (`#e0f2fe`): Fondos sutiles de etiquetas de especificación y áreas de realce técnico.
- **Verde Esmeralda WhatsApp** (`#25d366`): Reservado para botones y enlaces de conversión directa a WhatsApp, confirmaciones de cotización y badges de taller activo.
- **Verde Esmeralda Hover** (`#16a34a`): Estado interactivo para botones de cotización.

### Neutral
- **Blanco Técnico** (`#f8fafc`): Fondo base de la aplicación y áreas de descanso visual.
- **Superficie Blanca** (`#ffffff`): Fondos de tarjetas principales, paneles de cotización y barra de navegación fija.
- **Pizarra Obra / Perfilería** (`#0f172a` y `#1e293b`): Extraído del subtítulo "VIDRIOS Y ALUMINIOS". Contraste complementario en especificaciones y textos de alta densidad.
- **Gris Borde** (`#cbd5e1`): Divisores estructurales y bordes de campos de formulario.
- **Gris Muted** (`#64748b`): Etiquetas secundarias y metadatos.

### Named Rules
**The WhatsApp Action Rule.** El verde `#25d366` solo se utiliza en elementos que inician o conducen a una conversación directa de cotización en WhatsApp; nunca se emplea como fondo decorativo general.

**The Contrast Rule.** Ningún texto de cuerpo o medición puede tener un ratio de contraste inferior a 4.5:1 frente a su superficie contenedora.

## Typography

**Display Font:** Space Grotesk (con fallback `sans-serif`)
**Body Font:** IBM Plex Sans (con fallback `sans-serif`)
**Label/Mono Font:** IBM Plex Mono (con fallback `monospace`)

**Character:** Encuentro entre la ingeniería técnica y la accesibilidad comercial: titulares asimétricos con carácter arquitectónico y cifras monoespaciadas para medidas de obra.

### Hierarchy
- **Display** (700, `clamp(2.5rem, 5vw, 3.5rem)`, 1.08): Título principal de autoridad en la cabecera.
- **Headline** (700, `clamp(1.85rem, 3.5vw, 2.5rem)`, 1.15): Títulos de sección principal (Soluciones, Proceso de Obra, Prueba Social).
- **Title** (700, `clamp(1.35rem, 2.5vw, 1.75rem)`, 1.25): Títulos de fichas de producto y paneles interactivos.
- **Body** (400/500, `1rem`, 1.6): Descripciones técnicas y párrafos comerciales con longitud máxima de 65–75 caracteres.
- **Label** (600/700, `0.75rem`, letter-spacing 0.05em, uppercase): Medidas en metros, especificaciones de espesor (6mm/8mm/10mm), códigos de norma y badges de estado.

### Named Rules
**The Tabular Measurement Rule.** Toda cota, dimensión (ancho x alto), espesor de vidrio o cifra numérica de obra se renderiza en `IBM Plex Mono` para garantizar alineación visual y legibilidad milimétrica.

## Layout

Modelo espacial estructurado en contenedor central con ancho máximo de 1280px (`max-w-7xl`) y espaciado lateral fluido (`px-4 sm:px-8`).
- Cuadrícula asimétrica de 12 columnas para la cabecera y el catálogo de soluciones (7:5 para jerarquía balanceada entre valor de marca y cotizador express).
- Ritmo vertical generoso con separaciones de 64px a 96px entre secciones principales y 24px entre elementos de formulario.
- Enfoque mobile-first estricto: controles táctiles con altura mínima de 44px para facilitar la interacción de contratistas y usuarios en campo.

## Elevation & Depth

El sistema es plano por defecto con profundidad tonal sutil y honesta. Se descartan sombras pesadas, halos de color decorativos y sombras duras neobrutalistas.

### Shadow Vocabulary
- **Card Depth** (`box-shadow: 0 4px 6px -1px rgba(0, 82, 156, 0.08)`): Aplicado exclusivamente al contenedor del Cotizador Express para despegarlo ligeramente del fondo.
- **Floating Action** (`box-shadow: 0 10px 15px -3px rgba(37, 211, 102, 0.3)`): Resplandor suave reservado para el widget flotante inferior de WhatsApp.

### Named Rules
**The Flat Structure Rule.** La delimitación entre secciones y módulos se logra mediante bordes nítidos de 1px a 2px (`#cbd5e1`, `#00529c`) y alternancia de fondos neutros, nunca mediante apilamiento de sombras.

## Shapes

- Esquinas de radio pequeño y técnico (`2px` a `4px`) que evocan los biseles y cortes de vidrio templado.
- Botones de acción y campos de entrada con `border-radius: 4px`.
- Botón flotante y badges circulares con `rounded-full` para destacar sobre la ortogonalidad general.
- Bordes exteriores sólidos de 2px en componentes primarios (Ficha Técnica).

## Components

### Buttons
- **Shape:** Radio de 4px (`rounded`).
- **Primary WhatsApp:** Fondo `#25d366`, texto `#0f172a`, tipografía `IBM Plex Mono` 14px bold, padding `12px 24px`, hover `#16a34a`.
- **Secondary Taller:** Fondo `#00529c`, texto `#ffffff`, padding `10px 18px`, hover `#0066b8`.

### Inputs / Fields
- **Style:** Altura de 44px, borde `1px solid #cbd5e1`, fondo `#f8fafc`, radio de 3px.
- **Focus:** Contorno nítido de 2px en `#00529c` con desplazamiento de 2px (`outline-offset: 2px`).

### Cards / Containers
- **Corner Style:** Radio de 4px.
- **Background:** `#ffffff`.
- **Border:** `2px solid #00529c` para el cotizador principal; `1px solid #cbd5e1` para fichas de catálogo.
- **Padding:** 24px en móvil, 28px–32px en escritorio.
- **Regla de Oro:** Prohibido anidar tarjetas con fondo y borde dentro de otra tarjeta.

### Navigation
- Barra fija con `backdrop-blur` sobre fondo `rgba(255, 255, 255, 0.95)`, enlaces con indicador activo en borde inferior de 2px `#00529c`. Menú móvil colapsable accesible.

### Cotizador Express (Signature Component)
- Panel unificado de 4 pasos técnicos: Solución, Espesor de cristal, Medidas (m) y Distrito.
- Vista previa en tiempo real del mensaje compilado.
- Botón directo que genera la URL prellenada para `wa.me/51989086972`.

## Do's and Don'ts

### Do:
- **Do** expresar consistentemente la trayectoria de CristalesGraf como "+18 años de experiencia".
- **Do** indicar el cumplimiento de la Norma Técnica Peruana de Vidrio E.040 y el respaldo de Corporación Limatambo.
- **Do** usar `IBM Plex Mono` para medidas en metros, espesores en milímetros y números de teléfono.
- **Do** mantener todas las áreas de toque interactivas por encima de 44x44px.

### Don't:
- **Don't** reintroducir fondos con patrones de cuadrículas o gradientes artificiales no justificados.
- **Don't** anidar tarjetas dentro de tarjetas; usar líneas divisorias o espaciado tipográfico.
- **Don't** usar el verde de WhatsApp `#25d366` para elementos decorativos sin acción a chat.
- **Don't** usar emojis o glifos Unicode genéricos en lugar de iconos vectoriales SVG limpios.
