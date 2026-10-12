# Product Requirements Document (PRD)

**Proyecto:** Rediseño y Demo Web Multi-Página de Alto Rendimiento para CristalesGraf  
**Target:** Dueños, gerentes comerciales y contratistas de CristalesGraf (Lima, Perú)  
**Objetivo:** Reemplazar el sitio actual (vulnerable a inyecciones SEO, desestructurado y lento) por una plataforma comercial rápida, segura y orientada a la conversión de cotizaciones mediante WhatsApp.

---

## 1. Visión y Objetivos del Proyecto

* **Problema a resolver:** El sitio actual de CristalesGraf presenta inyección activa de spam/malware de apuestas (GGBet en vietnamita), menús duplicados, inconsistencias en años de trayectoria (15 vs. 18 años) y nula automatización para captar clientes con medidas en mano.
* **Propuesta de valor:** Sitio multi-página moderno, con diseño profesional en tonos industriales (azul marino, gris acero y acentos esmeralda/verde de cotización), blindado contra vulnerabilidades, con carga instantánea (<1.5s) y un cotizador interactivo que enruta leads precalificados a WhatsApp.
* **Métricas de éxito:**
  * 0 vulnerabilidades de inyección de código.
  * Score de rendimiento Lighthouse en móvil >= 90.
  * Tasa de clics al canal de cotización (WhatsApp) >= 15% de las sesiones activas.

---

## 2. Stack Tecnológico Recomendado

* **Frontend:** HTML5 semántico + Tailwind CSS (v3.x) + Vanilla JavaScript (o React / Astro para generación estática).
* **Iconografía:** Lucide Icons / Heroicons (SVG limpios, sin fuentes pesadas).
* **Despliegue:** Cloudflare Pages (Jamstack estático, SSL automático, protección DDoS y CDN global).
* **Integración Externa:** Generador dinámico de URL `https://wa.me/51989086972?text=...` y Google Maps Embed para la sede en Los Olivos.

---

## 3. Mapa de Navegación y Rutas

| Ruta | Nombre | Objetivo Primario |
| :--- | :--- | :--- |
| `/` o `index.html` | Inicio | Autoridad inmediata, propuesta de valor, calculadora rápida y prueba social. |
| `/productos` o `productos.html` | Soluciones y Productos | Catálogo segmentado (Residencial vs. Obras/Comercial) con botón de cotización por ítem. |
| `/proyectos` o `proyectos.html` | Proyectos / Obras | Portafolio visual filtrable que demuestra capacidad instalada en Lima. |
| `/nosotros` o `nosotros.html` | Nosotros | Consistencia de marca (18+ años), infraestructura de taller y respaldo de proveedores. |
| `/contacto` o `contacto.html` | Cotización y Contacto | Formulario guiado de cálculo, ubicación física en Tomás Valle y canales directos. |

---

## 4. Requisitos Funcionales por Página y Componentes

### 4.1. Componentes Globales (Persistentes)
* **Header / Barra de Navegación:**
  * Logo vectorizado o tipográfico de CristalesGraf + badge "Lima Norte / Cobertura Lima".
  * Menú de navegación con enlaces a las 5 rutas.
  * Botón CTA destacado: *"Cotizar Proyecto"* (abre modal o ancla al cotizador).
  * Menú hamburguesa responsive optimizado para móviles sin librerías pesadas.
* **Footer:**
  * Datos fiscales y dirección: *Av. Tomás Valle 1102, Los Olivos, Lima*.
  * Teléfonos directos: *(01) 533-1887* y *(+51) 989 086 972*.
  * Horarios de atención: *Lunes a Sábado: 8:00 am – 6:00 pm*.
  * Enlace al Libro de Reclamaciones (placeholder funcional).
  * Copyright dinámico: `Copyright © 2026 CristalesGraf. Todos los derechos reservados.`
* **Widget Flotante de WhatsApp:**
  * Icono fijo en la esquina inferior derecha con badge animado *"¿Cotizamos en 2 min?"*.

---

### 4.2. Página de Inicio (`index.html`)
* **Hero Section:**
  * Título H1: *"Especialistas en Vidrio Templado, Carpintería de Aluminio y Fachadas en Lima"*.
  * Subtítulo: *"Más de 18 años transformando espacios residenciales y comerciales con respaldo de Corporación Limatambo"*.
  * Acciones duales: Botón principal *"Cotizar por WhatsApp"* y secundario *"Ver Proyectos Ejecutados"*.
  * Tarjetas flotantes con métricas clave: `+18 Años`, `100% Vidrio Certificado`, `Lima y Callao`.
* **Grid de Soluciones:**
  * Tarjetas de acceso directo a Mamparas, Puertas de Ducha, Fachadas Integrales y Techos de Policarbonato.
* **Calculadora / Cotizador Express (Feature Core):**
  * Selectores:
    * Categoría: Mampara / Puerta de Ducha / Ventana / Fachada.
    * Espesor de vidrio: 6mm / 8mm / 10mm Templado.
    * Inputs de medidas aproximadas: Ancho (m) x Alto (m).
    * Distrito de instalación en Lima.
  * Acción: Botón *"Calcular y Enviar a WhatsApp"*, que genera automáticamente la URL con el mensaje precompilado:
    > `Hola CristalesGraf, quiero cotizar [Producto] de [Ancho]m x [Alto]m en vidrio templado de [Espesor] para el distrito de [Distrito]. ¿Cuál sería el costo estimado?`
* **Logotipos de Respaldo Técnico:**
  * Sección en escala de grises con marcas de materias primas y perfilería (Corporación Limatambo, marcas líderes de herrajes).
* **Testimonios y Reseñas:**
  * 3 testimonios breves con 5 estrellas que enfaticen puntualidad, precisión en el corte y acabados limpios.

---

### 4.3. Catálogo de Soluciones (`productos.html`)
* **Sistema de Filtro por Pestañas:**
  * Pestaña 1: **Línea Residencial** (Mamparas corredizas, puertas de ducha en acero inoxidable, ventanas acústicas y barandas).
  * Pestaña 2: **Línea Comercial / Proyectos** (Muros cortina, frentes de tienda, puertas batientes y divisiones de oficina).
* **Estructura de cada Ficha de Producto:**
  * Imagen representativa en alta definición con etiqueta `alt` descriptiva.
  * Título y descripción técnica breve (tipo de perfiles, accesorios, resistencia).
  * Especificaciones sugeridas en tags o píldoras (ej. `Templado 8mm/10mm`, `Aluminio anodizado/negro`, `Garantía 1 año`).
  * Botón de acción: *"Cotizar este modelo con mis medidas"*.

---

### 4.4. Portafolio de Proyectos (`proyectos.html`)
* **Filtros por tipo de obra:** `Todos`, `Residencial`, `Comercial`, `Fachadas`.
* **Tarjetas de Obra Terminada:**
  * Nombre del proyecto (ej. *"Edificio Multifamiliar - San Borja"*, *"Local Comercial - Los Olivos"*).
  * Especificaciones de la instalación (ej. *"Muro Cortina en cristal templado 10mm con perfilería pesada"*).
  * Modal visual o lightbox ligero para expandir las fotografías de la obra.

---

### 4.5. Nosotros y Respaldo (`nosotros.html`)
* **Historia y Trayectoria:** Reseña corporativa consolidada (18+ años de operaciones).
* **Ventajas Competitivas:**
  * Medición técnica en obra sin costo adicional en Lima Norte.
  * Cortes y mecanizados precisos con maquinaria especializada.
  * Cumplimiento estricto de la Norma Técnica Peruana de Vidrio E.040.
* **Fotos del Taller / Equipo:** Imágenes que transmitan seriedad técnica, seguridad y capacidad de producción.

---

### 4.6. Contacto y Cotización Formal (`contacto.html`)
* **Formulario Completo:**
  * Campos obligatorios: Nombre completo, Teléfono/WhatsApp, Correo, Distrito.
  * Campos del requerimiento: Tipo de producto, Medidas tentativas, Estado de obra (En planos / En casco / Por remodelar).
  * Textarea para notas adicionales.
* **Integración Geográfica:**
  * Mapa embebido interactivo centrado en Av. Tomás Valle 1102, Los Olivos.
  * Botón para abrir ruta directa en Google Maps o Waze.

---

## 5. Requisitos No Funcionales (NFR)

1. **Rendimiento:** Carga inicial bajo 1.5 segundos en redes 4G móviles. Uso estricto de imágenes en formato `.webp` con atributos `loading="lazy"`.
2. **Seguridad Absoluta:**
   * Cero uso de CMS vulnerables o plugins desatendidos.
   * Sin base de datos expuesta; todo el tráfico dinámico viaja a través de enlaces directos o endpoints serverless ligeros.
3. **SEO Local y Limpieza de Reputación:**
   * Meta tags OpenGraph y Twitter Cards configuradas.
   * Schema `LocalBusiness` con dirección de Los Olivos, geo-coordenadas, horario y teléfonos.
   * Supresión total de palabras clave residuales vinculadas a juegos de azar o casino.
4. **Diseño Responsive:** Mobile-first absoluto. El 80% del tráfico de vidriería en Lima llega desde smartphones buscando soluciones en obra o taller.

---

## 6. Criterios de Aceptación para la Demo

* [ ] El sitio navega de forma fluida entre las 5 páginas sin enlaces rotos ni textos en inglés/vietnamita.
* [ ] La calculadora de cotización genera un enlace a WhatsApp válido que abre el chat con el número `+51 989 086 972` y el texto completado con las medidas elegidas.
* [ ] Todas las referencias a la trayectoria de la empresa mencionan consistentemente "más de 18 años".
* [ ] El diseño visual utiliza una paleta moderna derivada de su logotipo (fondos claros, grises técnicos, Azul Corporativo `#00529c`, Cyan Cristal `#00b4d8` y verde WhatsApp `#25d366` para llamados a la acción).
* [ ] El código está listo para subirse directamente a un repositorio y desplegarse en Cloudflare Pages en un solo comando.