Sistema de diseño de la web de podio: un ranking abierto de devs de Latinoamérica con su actividad pública en GitHub. Se arma a partir de `site/style.css`, `site/index.html` y `site/app.js`.

## Contenido

**Voz.** Español con voseo, directa y cercana: "Sumate al podio", "Hacé fork", "¿Querés otra categoría?", "¡Sé la primera persona!". Se habla de vos a vos, sin jerga corporativa. Todo lo que lee una visita va en español; el código, los commits y los issues van en inglés.

**Los límites se dicen.** Donde un número se puede inflar, la página lo dice en vez de esconderlo. Usá `FreshnessNote` para mostrar cuándo se calculó y qué cuenta cada categoría, con su límite conocido ("Las rachas y las contribuciones del año se pueden inflar con commits automáticos").

**Se construye en abierto.** Las categorías y los países se proponen con PRs. Los textos invitan a sumarse, nunca a mirar de afuera.

**Textos reales** para usar tal cual: "Los desarrolladores de Latinoamérica que más aportan en GitHub.", "Contribuciones del año", "Racha actual", "Racha más larga", "PRs a otros repos", "Estrellas", "Datos de ejemplo: aún no hay ranking real.", "Aún no hay nadie aquí. ¡Sé la primera persona!".

Sin emoji decorativo. Sin exclamaciones salvo la invitación a ser la primera persona.

## Fundamentos visuales

- **Tema principal oscuro**, con un tema claro (`light`) para el modo claro. Los dos cumplen 4.5:1 en todo el texto.
- **Fondo** `bg`, **tarjetas y controles** `surface`, **texto** `text`, **secundario** `muted`. Nunca `muted` sobre otro fondo que `bg` o `surface`.
- **Lima** es la marca. Como relleno (`accent`, con texto `on-accent`) va en la pestaña seleccionada y en el botón de llamada. Como texto o contorno (título, valores, borde del primer puesto) usá `accent-text`, que en el tema claro es un verde más oscuro para llegar a contraste.
- **Ámbar** (`amber`) marca posiciones, el aviso de datos de ejemplo y el anillo de foco.
- **Plano**: sin sombras ni degradados. Los bordes son de 1px en `border`. Radios: `radius-sm` en pestañas, selector y aviso; `radius-md` en tarjetas del podio y botón; `radius-full` en avatares.
- **Tipografía**: `Instrument Sans` para texto, `JetBrains Mono` en negrita para posiciones y valores. Ambas se cargan desde Google Fonts, no hay archivos de fuente en este sistema.
- **Espaciado**: pasos de `space-1` (4px) a `space-8` (40px). Ancho máximo de la página 860px con 16px de margen lateral.
- **Foco**: anillo sólido de 2px en `amber`, desplazado 2px, sobre botones, selector y enlaces.
- **Fidelidad**: el borde `border` oscuro del sitio (1.4:1) no llega a 3:1; se mantiene exacto y por eso ningún control depende solo del borde.
- **Dirección C, "Mezcla"** (D-27): texto en Instrument Sans y números en JetBrains Mono; un toque de consola sin llegar a terminal. Primero el celular (400px, D-18).
- **Layout**: una columna. Encabezado con "Podio" en `accent-text` y a la derecha "top · 12 meses" en mono; tira de categorías que se desliza; filtro de país. Podio escalonado 2.º, 1.º, 3.º (D-19) con tarjetas compactas de borde superior de 3px, lima en el 1.º. Después la lista desde el 4.º con filas densas de 8px de relleno: posición, avatar de 36px, nombre con bandera y @usuario, resumen de las otras categorías en mono pequeño y el valor (D-20). Al pie, la nota de frescura con el prefijo `// `.

## Iconografía

No hay logo: "Podio" se escribe en texto, `hero-title`, en `accent-text`. No se dibuja ninguna marca. No hay set de íconos; las banderas de cada país son emoji, armadas desde el código ISO de dos letras con indicadores regionales (`flag(cc)` en `site/app.js`; por ejemplo NI se ve como bandera de Nicaragua). Los avatares son la foto de GitHub de cada persona, circular, y los provee quien consume el componente.

## Componentes

`RankRow`, `CategoryTabs`, `CountryFilter`, `Podium`, `FreshnessNote`, `DraftBadge`. Cada uno tiene su guía y su vista previa; los estilos viven en `components/bundle.css`.
