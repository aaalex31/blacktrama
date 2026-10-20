# Blacktrama — sitio web

Sitio estático. Sube **todo el contenido de esta carpeta** a la raíz de tu hosting (Netlify, Vercel, GitHub Pages, cPanel, etc.). No requiere build.

## Estructura
```
index.html        Home
trabajos.html     Todos los trabajos (vista Proyectos / Lista: trabajos.html?v=lista)
proyecto.html     Case study (proyecto.html?p=clinica-sonrisa)
contacto.html     Formulario de contacto
js/support.js     Runtime que monta cada página (no editar)
assets/           Video del cielo (sky.webm) y su poster
```

## Notas
- Cada página lleva su propio markup, estilos inline y lógica dentro del mismo HTML (bloque `<script data-dc-script>`).
- Librerías por CDN: Google Fonts (Mona Sans, IBM Plex Mono), Phosphor Icons, Lenis.
- Las páginas deben servirse desde un servidor (http/https). Abrir con doble clic (file://) puede bloquear el video o el runtime.
- Los formularios no envían aún: conectar a un servicio (Formspree, Netlify Forms, backend propio) en `index.html` y `contacto.html`.
- Transiciones entre páginas: desactivadas. Para activarlas, cambiar `const PAGE_TRANSITIONS = false` a `true` en cada HTML.
- Imágenes: placeholders grises; reemplazar por imágenes reales.
