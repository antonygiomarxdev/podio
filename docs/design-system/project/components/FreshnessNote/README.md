Nota al pie del ranking con la fecha del último cálculo, qué cuenta la categoría activa y su límite conocido (dirección C, "Mezcla").

Quien consume provee: la fecha de generación (con `toLocaleString('es')`), la descripción de lo que mide la categoría y, si lo tiene, el límite. UC-6.

- Clase `pd-note pd-fresh`: texto en `muted` a 0.8rem, borde superior de 1px en `border`, 16px de margen arriba y 12px de relleno.
- Lleva el prefijo de consola `// ` en `amber` y JetBrains Mono (lo pone la hoja de estilos, no lo escribas en el texto).
- La fecha en `text`, peso 600. Decí el límite tal cual: "se puede inflar con commits automáticos".
- Si no hay fecha, no muestres la línea de actualización.
