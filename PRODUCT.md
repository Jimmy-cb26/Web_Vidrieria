# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

HTML5 semántico + Tailwind CSS (v3.x) + Vanilla JavaScript (arquitectura multi-página estática Jamstack, optimizada para despliegue en Cloudflare Pages).

## Users

- **Propietarios y remodeladores residenciales (Lima):** Buscan renovar o instalar mamparas, puertas de ducha en cristal templado o ventanas acústicas; necesitan una cotización rápida, transparente y confiable, normalmente desde su smartphone con medidas tentativas en mano.
- **Contratistas generales, arquitectos y maestros de obra:** Requieren cotizar carpintería de aluminio y muros cortina/fachadas comerciales con especificaciones técnicas precisas (espesor de vidrio templado, perfilería pesada, cumplimiento normativo) y contacto directo e inmediato para visita o rectificación en obra.

## Product Purpose

Reemplazar la presencia web anterior de CristalesGraf por una plataforma comercial multi-página moderna, rápida (<1.5s en móvil) y blindada contra vulnerabilidades, diseñada para precalificar prospectos y convertir visitas en cotizaciones formales directas vía WhatsApp.

## Positioning

Vidriería técnica y carpintería de aluminio de referencia en Lima Norte (Los Olivos) con más de 18 años de trayectoria comprobada, respaldo de insumos certificados por Corporación Limatambo y cumplimiento estricto de la Norma Técnica Peruana de Vidrio E.040, combinando taller propio con un cotizador interactivo express que simplifica el pedido de presupuestos al instante.

## Operating Context

- Navegación predominantemente móvil (80% del tráfico estimado) por parte de usuarios en obra o en el hogar.
- Proceso de compra guiado por medidas iniciales (ancho x alto), selección de tipo de vidrio/espesor y confirmación de distrito para instalación en Lima y Callao.
- Cierre comercial y seguimiento de proyectos realizado a través de WhatsApp (`+51 989 086 972`) y atención presencial en taller en Los Olivos.

## Capabilities and Constraints

- **Capacidades:**
  - Arquitectura multi-página con 5 rutas principales: Inicio (`index.html`), Productos (`productos.html`), Proyectos (`proyectos.html`), Nosotros (`nosotros.html`) y Contacto (`contacto.html`).
  - Cotizador express que computa variables clave (categoría, espesor, dimensiones, distrito) y genera un enlace prellenado a WhatsApp sin intermediarios ni base de datos expuesta.
  - Catálogo segmentado (Residencial vs. Comercial/Proyectos) con especificaciones técnicas y botón de cotización por producto.
  - Portafolio de obras filtrable con visualizador modal/lightbox.
  - Formulario de contacto y cotización detallada con mapa interactivo centrado en sede Los Olivos.
- **Restricciones:**
  - Cero dependencias de CMS pesados o vulnerables (sin WordPress ni plugins desactualizados).
  - Rendimiento móvil estricto: Lighthouse >= 90, tiempo de carga < 1.5s sobre 4G.
  - Imágenes optimizadas con atributos `loading="lazy"`.
  - Canales oficiales: WhatsApp `+51 989 086 972`, teléfono fijo `(01) 533-1887`, sede en `Av. Tomás Valle 1102, Los Olivos, Lima`.

## Brand Commitments

- **Nombre comercial:** CristalesGraf.
- **Trayectoria:** Más de 18 años de experiencia (consistencia estricta en todo el sitio, eliminando discrepancias).
- **Tono y voz:** Profesional, técnico, honesto, ágil y enfocado en la seguridad estructural y acabados limpios.
- **Identidad institucional:** Taller formal con respaldo de Corporación Limatambo y cumplimiento normativo E.040.

## Evidence on Hand

- Documento de requerimientos base: [PRD-cristalesgraf.md](file:///d:/pra/Web_Vidrieria/PRD-cristalesgraf.md).
- Dirección física confirmada: Av. Tomás Valle 1102, Los Olivos, Lima.
- Teléfonos operativos: `(01) 533-1887` y `+51 989 086 972`.
- Proveedor de materia prima: Corporación Limatambo.
- *Ausencias explícitas:* No se deben fabricar testimonios irreales ni imágenes de proyectos ajenos sin etiquetar como demostración técnica o solicitar material real de taller al cliente.

## Product Principles

1. **Velocidad hacia WhatsApp:** Cada ruta y ficha de producto debe allanar el camino para que el cliente pase de la duda a una conversación de cotización estructurada en menos de 2 clics.
2. **Claridad técnica sin fricción:** Presentar especificaciones (espesores en mm, tipos de perfilería y normas) en lenguaje claro y accesible tanto para contratistas como para familias.
3. **Autoridad y confianza local:** Destacar la presencia física en Tomás Valle, la trayectoria de +18 años y el cumplimiento normativo para diferenciar a CristalesGraf de la informalidad del sector.
4. **Seguridad y ligereza Jamstack:** Mantener el código estático, limpio, accesible y libre de superficies de ataque.

## Accessibility & Inclusion

- Estructura HTML5 semántica y jerarquía de encabezados ordenada.
- Contraste accesible (mínimo WCAG AA para textos y botones de acción sobre fondos claros e industriales).
- Elementos táctiles y botones de acción (especialmente cotizador y CTA de WhatsApp) con áreas mínimas de toque de 44x44px optimizadas para dispositivos móviles.
