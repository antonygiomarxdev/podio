# podio

Un ranking abierto de devs de Latinoamérica, armado con su actividad pública en GitHub. Solo aparece quien se anota.

**Ver el podio:** https://antonygiomarxdev.github.io/podio/

## Por qué

podio pregunta primero y cuenta más que commits. Se distingue en tres cosas:

- **Te anotás vos.** Nadie aparece sin abrir su propio PR.
- **Varias formas de destacar.** Más que commits: contribuciones del año, rachas, PRs aceptados en proyectos ajenos y estrellas.
- **Lo construye la comunidad.** Las categorías, los países y la web se proponen y se agregan con PRs.

## Categorías

Cada una es un ranking aparte, calculado sobre los últimos 12 meses:

| Categoría | Qué mide |
|---|---|
| Contribuciones del año | Total de contribuciones en tu calendario de GitHub |
| Racha actual | Días seguidos contribuyendo, hasta hoy |
| Racha más larga | Tu mejor racha del año |
| PRs a otros repos | Pull requests tuyos aceptados en cualquier repositorio público que no sea de tu cuenta personal, incluidas las organizaciones a las que pertenecés (D-23) |
| Estrellas | Estrellas de tus repositorios públicos propios (sin forks, hasta 100 repos) |

Si dos personas empatan en una categoría, queda arriba quien llegó primero a ese valor; si siguen empatadas, quien se anotó antes (D-28).

¿Querés otra categoría? Mirá [cómo proponerla](CONTRIBUTING.md#proponer-una-categoria-nueva).

## Límites

Las rachas y las contribuciones del año se pueden inflar con commits automáticos. En esta versión lo aceptamos y lo decimos acá. Lo mismo pasa con otras dos categorías: los PRs a otros repos se pueden inflar con organizaciones que controlás vos, y las estrellas con amigos o con cuentas extra. Si se te ocurre una categoría más difícil de inflar, proponela por [CONTRIBUTING.md](CONTRIBUTING.md).

## Sumate en 3 pasos

1. Hacé fork de este repositorio.
2. Agregá el archivo `members/<tu-usuario>.json`:
   ```json
   { "github": "tu-usuario", "country": "NI" }
   ```
   `country` es el código de dos letras de tu país (AR, BO, BR, CL, CO, CR, CU, DO, EC, GT, HN, MX, NI, PA, PE, PR, PY, SV, UY, VE).
3. Abrí un Pull Request. Un check automático lo valida; cuando se acepta, aparecés en el podio al día siguiente.

Los detalles están en [CONTRIBUTING.md](CONTRIBUTING.md).

## Solo aparece quien lo pide

Un PR solo puede agregar o cambiar **el archivo de quien lo abre**. La validación rechaza cualquier PR que toque el archivo de otra persona. Para salir del podio, borrá tu archivo con un PR.

## Cómo funciona

- Todos los días a las 06:00 UTC, y en cada cambio a `main`, un workflow de GitHub Actions:
  1. valida `members/` con `scripts/validate.mjs`;
  2. consulta la API GraphQL de GitHub con `scripts/rank.mjs` y genera `site/data/ranking.json`;
  3. publica `site/` en GitHub Pages.
- Solo se usan **datos públicos**.
- La web es HTML, CSS y JavaScript sin frameworks ni build.

## Cómo está definido

El producto está definido en `docs/` con Scriptorium:

- [`docs/PRODUCT.md`](docs/PRODUCT.md): el producto, aprobado.
- [`docs/requests/`](docs/requests/): los pedidos, aceptados.
- [`docs/join/`](docs/join/), [`docs/ranking/`](docs/ranking/) y [`docs/community/`](docs/community/): los PRDs de cada parte, aprobados.
- [`docs/DECISIONS.md`](docs/DECISIONS.md): las decisiones tomadas.

Diseño:

- La dirección visual elegida es la C, "Mezcla" (D-27).
- El sistema de diseño está en [`docs/design-system/`](docs/design-system/) y los mockups en [`docs/mockups/`](docs/mockups/).
- Las propuestas están en [`docs/propuestas-ui/`](docs/propuestas-ui/) y [`docs/propuestas-color/`](docs/propuestas-color/).
- La paleta de colores todavía se está eligiendo con la comunidad: no está decidida.

## Desarrollo local

Requiere Node 20 o superior.

```sh
node --test                                         # tests
node scripts/validate.mjs                           # valida members/
GITHUB_TOKEN=$(gh auth token) node scripts/rank.mjs # genera site/data/ranking.json
npx serve site                                      # abre la web en local
```

## Licencia

MIT. Ver [LICENSE](LICENSE).
