# AGENTS.md — CristalesGraf Web

Guía de arquitectura, estándares de código, reglas de negocio y sistema de diseño para agentes autónomos y desarrolladores trabajando en la plataforma web de **CristalesGraf**.

---

## 1. Visión y Propósito del Proyecto

CristalesGraf es una vidriería técnica y taller formal de carpintería de aluminio en Lima Norte (Los Olivos), con más de 18 años de trayectoria y respaldo de materia prima certificada por Corporación Limatambo.

El objetivo de esta web es convertir visitas en cotizaciones precalificadas y directas a través de WhatsApp (`+51 989 086 972`), eliminando la fricción de cotización mediante herramientas interactivas (Cotizador Express en portada) y fichas de producto orientadas a obra.

---

## 2. Stack Tecnológico y Arquitectura

- **Arquitectura:** Sitio estático multi-página (Jamstack), ligero, seguro y optimizado para despliegue en CDN (Cloudflare Pages / GitHub Pages).
- **Frontend Stack:**
  - **HTML5 semántico:** Estructura limpia y accesible (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`).
  - **Tailwind CSS (v3 CDN):** Configuración unificada embebida en `<script>` en cada página.
  - **Vanilla JavaScript:** Funcionalidad modular e interactiva sin dependencias pesadas ni frameworks de terceros.
- **Rutas Principales (5 páginas):**
  1. `index.html`: Portada institucional con el **Cotizador Express** como protagonista central.
  2. `productos.html`: Catálogo técnico categorizado (Línea Residencial vs. Comercial y Obras) con modal de cotización.
  3. `proyectos.html`: Portafolio técnico de obras ejecutadas con especificaciones y filtro interactivo.
  4. `nosotros.html`: Historia del taller (+18 años), maquinaria, control de calidad y certificación E.040.
  5. `contacto.html`: Sede física (Av. Tomás Valle 1102), mapa interactivo, formulario de obra y canales directos.

---

## 3. Identidad de Marca y Reglas de Negocio (Inviolables)

Cualquier cambio de texto, diseño o funcionalidad debe cumplir estrictamente estas directrices:

1. **Trayectoria:** Mencionar consistentemente **"+18 años de experiencia"** (o "más de 18 años de trayectoria formal"). Nunca contradecir esta cifra.
2. **Sede Física:** `Av. Tomás Valle 1102, Los Olivos, Lima, Perú`.
3. **RUC Oficial:** `10416805821`.
4. **Teléfonos Oficiales:**
   - WhatsApp Obra: `+51 989 086 972` (enlaces a `https://wa.me/51989086972?text=...`)
   - Central Fija: `(01) 533-1887`
5. **Proveedor Certificado:** `Corporación Limatambo` (cristal templado de seguridad).
6. **Normativa Técnica:** `Norma Técnica Peruana de Vidrio E.040` (RNE Vidrio).
7. **Tono y Voz:** Técnico, confiable, ágil y honesto. Evitar testimonios fabricados o claims comerciales exagerados.

---

## 4. Sistema de Diseño (Design System)

La identidad visual está normada en [DESIGN.md](DESIGN.md) y derivada fielmente del logotipo oficial ([logo.png](logo.png)).

### 4.1. Paleta de Colores

| Token Tailwind | Hex | Rol y Aplicación |
|---|---|---|
| `brand-navy` | `#00529c` | **Azul Corporativo Primario** (extraído de "cristales GRAF" en `logo.png`). Botones primarios, encabezados, bordes activos y selección. |
| `brand-navy-dark` | `#002d5a` | **Azul Profundo Taller**. Barras de autoridad, cabeceras de contraste y fondos de footer. |
| `brand-navy-light` | `#0066b8` | **Azul Interactivo / Hover**. Estados `:hover` de botones y enlaces institucionales. |
| `brand-cyan` | `#00b4d8` | **Cyan Cristal Luminoso** (extraído del panel superior de cristal en `logo.png`). Badges técnicos, micro-detalles y brillo vítreo. |
| `brand-cyan-light` | `#e0f2fe` | **Hielo Translúcido**. Fondos sutiles de etiquetas de espesores y paneles técnicos. |
| `brand-slate` | `#1e293b` | **Pizarra Industrial / Perfilería**. Marcos, perfiles de aluminio y contraste de alta lectura. |
| `brand-surface` | `#f8fafc` | **Blanco Técnico Taller**. Superficie de fondo limpia de la aplicación. |
| `brand-border` | `#cbd5e1` | **Gris Bisel / Borde**. Bordes nítidos de vidrio y perfilería de aluminio. |
| `brand-whatsapp` | `#25d366` | **Verde WhatsApp**. Reservado **estrictamente** para botones y enlaces de cotización a chat. Hover: `#16a34a`. |

### 4.2. Tipografía

- **Display & Headings:** `Space Grotesk` (700) con espaciado ajustado (`letter-spacing: -0.02em` a `-0.03em`).
- **Cuerpo de Texto:** `IBM Plex Sans` (400, 500, 600) para descripciones y lectura técnica clara.
- **Cotas, Medidas y Cifras:** `IBM Plex Mono` (monospace tabular) para medidas en metros (`m`), espesores (`mm`), teléfonos y códigos de norma.

### 4.3. Reglas de Oro del Diseño (Design Rules)

- **The WhatsApp Action Rule:** El verde `#25d366` se reserva con exclusividad para componentes que abren un chat de cotización en WhatsApp. Prohibido usarlo como adorno genérico o fondo general.
- **The Tabular Measurement Rule:** Toda medida numérica, cota o espesor se renderiza en fuente monoespaciada (`IBM Plex Mono`).
- **The Contrast Rule:** Ningún texto tendrá un ratio de contraste menor a 4.5:1 (WCAG AA).
- **The Flat Structure Rule:** La profundidad se define con bordes nítidos de 1px a 2px (`#cbd5e1`, `#00529c`) y alternancia de fondos neutros; nunca anidar tarjetas dentro de tarjetas ni usar sombras pesadas desalineadas.

---

## 5. Convenciones de Código y Mantenimiento

1. **Configuración de Tailwind:** Debe mantenerse sincronizada e idéntica en los bloques `<script>` de todas las páginas HTML (`index.html`, `productos.html`, `proyectos.html`, `nosotros.html`, `contacto.html`).
2. **Estilos de Superficies de Navegador:** Cada página debe incluir en su etiqueta `<style>` los estilos para:
   - `::selection { background-color: #00529c; color: #f8fafc; }`
   - Scrollbar personalizada con hover en `#00529c`.
   - Foco accesible en campos de entrada (`outline: 2px solid #00529c; outline-offset: 2px;`).
3. **Imágenes y Multimedia:**
   - Usar siempre atributos `loading="lazy"` y `alt` descriptivos en imágenes de catálogo o proyectos.
   - Preservar el logotipo corporativo [logo.png](logo.png) en la barra de navegación superior.
4. **Áreas Táctiles Móviles:** Todos los botones, enlaces interactivos y campos de formulario deben contar con una altura mínima de `44px` para compatibilidad móvil en obra.
5. **Control de Versiones y GitHub (Regla Inviolable):** Queda **estrictamente prohibido** ejecutar `git push` o subir cualquier cambio al repositorio remoto de GitHub a menos que el usuario lo autorice o solicite de forma explícita y directa. Todo trabajo se mantendrá local en el entorno de desarrollo.

---

## 6. Procedimientos de Verificación

Antes de concluir cualquier cambio de interfaz:
- Ejecutar el detector de consistencia de diseño de Impeccable:
  ```powershell
  cmd /c ".agent\skills\impeccable\scripts\impeccable.cmd detect --json index.html productos.html proyectos.html nosotros.html contacto.html"
  ```
- Confirmar que el resultado sea `[]` (cero infracciones / exit code 0).
- Verificar que los enlaces a WhatsApp generen URLs válidas con codificación correcta de parámetros (`wa.me/51989086972?text=...`).
