Una fila densa del ranking desde la posición 4: posición, avatar, nombre con bandera y @usuario, resumen de las otras categorías y valor (dirección C, "Mezcla").

Quien consume provee: la posición, el avatar de GitHub (circular, 36px), el nombre, el @usuario, el código de país para la bandera emoji, el valor de la categoría elegida ya formateado con `Intl.NumberFormat('es')` y el resumen de las otras cuatro categorías.

- Cada fila es un `li` de una `ol` con `start="4"`: grilla de 24px (posición) · 36px (avatar) · nombre · valor. Relleno vertical de 8px (`space-3`), sin fondo propio y con borde inferior de 1px en `border`.
- Posición en `amber` con `position`; valor en `accent-text` con `value-row`, a la derecha.
- Nombre en peso 600, `@usuario` en `muted` a 0.8rem y debajo el resumen en JetBrains Mono a 0.75rem (nunca menos de 12px): "racha 5d · máx 40d · PRs 12 · ★ 155".
- Asigná los datos como texto, nunca como HTML.
