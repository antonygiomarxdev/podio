El podio de los tres primeros: tarjetas compactas escalonadas con posición, avatar, nombre con bandera, @usuario, valor y un resumen de las otras categorías (dirección C, "Mezcla").

Quien consume provee: tres personas ya ordenadas (avatar de GitHub circular de 36px; nombre; @usuario; país; valor formateado; resumen etiquetado "racha · máx · PRs · ★"). Si hay menos de tres, los lugares libres se muestran como tarjetas vacías con "Lugar libre".

- Lista ordenada `ol` en tres columnas; el orden visual es 2.º, 1.º, 3.º (`order`), pero el DOM va 1, 2, 3.
- Cada tarjeta: `surface`, borde de 1px en `border`, borde superior de 3px, radio `radius-md`. La del 1.º lleva el borde superior y el del avatar en `accent-text` y más relleno inferior (22px), así queda más alta.
- Posición en `amber`, valor en `accent-text` con `value` a 1.05rem, resumen en `muted` y JetBrains Mono a 0.75rem, siempre con etiquetas: "racha 14d · máx 61d" y "PRs 22 · ★ 340" en dos líneas.
- Si hay tres personas o menos, la lista (`RankRow`) no se muestra.
