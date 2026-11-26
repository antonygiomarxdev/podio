Tira de pestañas para cambiar de categoría, con una sola seleccionada, bajo el encabezado de la página (dirección C, "Mezcla").

Quien consume provee: la lista de categorías (etiqueta en español) y cuál está activa. La primera vista es "Contribuciones del año".

- Contenedor `role="tablist"` con `aria-label="Categoría"`; cada botón `role="tab"` con `aria-selected`.
- Una sola línea que se desliza en horizontal dentro de su propio contenedor (`overflow-x: auto`), sin partirse en filas; cada botón con `white-space: nowrap`.
- Botón: `surface`, texto `muted` a 0.85rem, borde de 1px en `border`, radio `radius-sm`, relleno de 6px por 10px, 6px entre pestañas. La seleccionada va en `accent` con texto `on-accent` y peso 600.
- Encabezado: "Podio" en `accent-text` a 1.75rem (clase `pd-hd`) y a la derecha la etiqueta "top · 12 meses" en JetBrains Mono, `muted`, 0.75rem (`pd-meta`).
