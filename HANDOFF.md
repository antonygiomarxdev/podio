# Handoff: podio, sesión 2 (2026-11-26)

Para la sesión que sigue. Leé esto entero antes de tocar nada.

## Qué es

Ranking abierto de devs de LATAM basado en actividad pública de GitHub. Solo aparece quien se anota con su propio PR. Se construye en vivo en TikTok con la comunidad. Es una actividad tranquila del stream: nadie está obligado a aportar (D-16).

- Repo: https://github.com/antonygiomarxdev/podio (público, MIT).
- Local: `C:\Users\anton\dev\podio`.
- Web destino: https://antonygiomarxdev.github.io/podio/ (Pages todavía no está activado).
- Texto para usuarios en español con voseo. Código y commits en inglés. La comunidad puede escribir issues y PRs en español o inglés (D-26).
- Commits sin líneas de atribución (D-11).

## Qué se hizo en esta sesión

Se definió el producto con Scriptorium (`docs/`), todo revisado por un reviewer independiente:

| Documento | Estado |
|---|---|
| `docs/PRODUCT.md` | Approved (2026-11-26) |
| `docs/requests/REQ-1..REQ-5` | Accepted |
| `docs/join/PRD.md` (9 requisitos) | Approved |
| `docs/ranking/PRD.md` (15 requisitos) | Approved (re-aprobado tras D-29) |
| `docs/community/PRD.md` (9 requisitos) | Approved |
| `docs/DECISIONS.md` | D-1..D-29 (D-21 reemplazada por D-28), L-1..L-7 |
| `docs/CROSS-CUTTING.md`, `GLOSSARY.md` | Hechos |
| `CONTRIBUTING.md` | En voseo, con tildes, con D-25 y D-26 |
| `README.md` | Actualizado con la cadena de producto y los límites |

Diseño (exploratorio; la UX formal va después de los FRD):

| Qué | Local | Artefacto (privado hasta que el dueño lo comparta) |
|---|---|---|
| Página de producto para la comunidad | `docs/site-producto/index.html` | https://claude.ai/artifact/JSuJJAQy1WKK6UfgdXAzd8 |
| Propuestas de UI A/B/C (eligieron **C, Mezcla**, D-27) | `docs/propuestas-ui/index.html` | https://claude.ai/artifact/QMHp5jDbVbkE1MSQ82FDxZ |
| Design system (dirección C, colores viejos) | `docs/design-system/project/` | https://claude.ai/artifact/Vy859pHrivpwuhvCBqsavr |
| Mockups, 8 pantallas | `docs/mockups/project/` | https://claude.ai/artifact/25h3AZ1uTmzfGfYJ5xHkQh |
| Paletas con identidad latina A/B/C | `docs/propuestas-color/index.html` | https://claude.ai/artifact/Ct8iF1submuWavABxaDzgS |

Para republicar un artefacto desde otra sesión: Artifact `read` con su URL, después `publish` con `url`. El design system y los mockups son artefactos con tipo: leé su `SKILL.md` con `read` antes de editar.

## Decisiones de esta sesión que más pesan

- Objetivos en orden: comunidad en vivo, vitrina, competencia (D-8). Metas orientativas (D-13, D-16).
- Anti-trampa fuera de v1, pero los límites se dicen en la página (D-9, principio 5).
- Un ranking LATAM con filtro que lista los 20 países; país sin miembros muestra invitación (D-10, D-29).
- Categoría por defecto: contribuciones del año (D-12). País autodeclarado, no se verifica (D-17).
- PRs a otros repos: cualquier repo público que no sea de tu cuenta personal, organizaciones incluidas (D-23). Estrellas: repos propios públicos, sin forks, hasta 100 (L-4).
- Racha actual: desde hoy, o desde ayer si hoy no hay contribución (L-5).
- Empates: arriba quien llegó primero al valor; si sigue, quien se anotó antes (D-28, L-7). Valor 0 se muestra al final (D-22).
- UI: celular primero (D-18), podio literal 2-1-3 (D-19), fila con avatar, nombre, @usuario, bandera, valor y resumen de las otras categorías (D-20), dirección C (D-27).
- Los colores de D-6 (lima y ámbar de antonygiomarx.dev) están **reabiertos**: el dueño pidió identidad latina sin estereotipos.

## Qué sigue, en este orden

1. **Elegir paleta** (tarea abierta del lead). El dueño y la comunidad eligen entre A Añil y jade, B Cacao y grana, C Caribe y grana (o una mezcla). Registrarla como decisión que reemplaza los colores de D-6. Después: aplicarla al design system, a los mockups y a `site/style.css`, y re-revisar contraste.
2. **FRDs** (`/scriptorium:frd`), una función a la vez, empezando por join. Después los UX docs de ranking (absorben D-18..D-20, D-27, D-29) y el TP (`/scriptorium:tp`).
3. **Código existente (sin commitear a propósito, ver abajo).** Arreglos pendientes del handoff anterior, como specs de fix sobre los FRDs (L-1):
   - `scripts/rank.mjs:54` lee `member.login`; el formato es `github`. Ajustar `rank.test.mjs`.
   - `scripts/rank.mjs:58`: agregar `is:public` a la búsqueda de PRs. Con token personal dio 1.618 PRs, inflado por repos privados.
   - `rank.mjs` no implementa todavía D-28 (desempate por quién llegó primero), D-22 ni D-29; `site/app.js` lista solo países con miembros (D-29).
   - El TP decide cómo saber cuándo se llegó a un valor; para estrellas cuesta muchas llamadas (fecha de cada estrella).
   - Confirmar que no quedó trabajo duplicado en `validate.mjs`, sus tests y `validate.yml`.
   - Tildes en los textos de `site/`. Abrir `site/index.html` con datos reales a ancho de celular.
   - Review independiente del código: `node --test`, `validate.mjs`, `rank.mjs`, e intentar saltarse la regla de consentimiento.
4. Primer push del código, activar Pages (Settings → Pages → Source: GitHub Actions, lo hace el dueño), correr `pages.yml` a mano.
5. Issues `good first issue` para el live: categoría nueva, badge para el README, modo claro, filtro por país en la URL, un PR de prueba de alguien del chat.

## Qué está en el repo y qué no

- **Subido:** `docs/`, `.scriptorium/` (sin `local`, que es una ruta de esta máquina), `README.md`, `CONTRIBUTING.md`, `HANDOFF.md`.
- **Sin subir a propósito:** `scripts/`, `site/`, `members/`, `.github/`. Tienen los bugs de arriba y el handoff anterior pedía arreglarlos antes del primer commit. Además, subir `.github/` dispara `pages.yml` en cada push a `main`.

## Cómo se trabajó

- Equipo de agentes (puppeteering): researcher, builder, designer y reviewer en Sonnet; el lead verifica cada reporte y re-corre los checks.
- Checks de docs: `bun "C:/Users/anton/dev/scriptorium/scripts/lint-docs.ts" .`, `check.ts prd docs/<slice>/PRD.md <ID>`, `check.ts summary <doc>`. Un cambio en un documento aprobado pide `check.ts approve <doc>` con el OK del dueño.
- Node local v24: `node --test` (sin carpeta) corre todos los tests; `node --test scripts/` falla en Node 24.

## Contexto del live

- El dueño transmite en TikTok LIVE vertical. La sesión de Claude se ve en pantalla: **no imprimas emails, tokens ni rutas de proyectos de trabajo**.
- Página de votación de ideas: https://claude.ai/artifact/GKmDR6vJR37ibU6c8prYPg (privada hasta que el dueño la comparta).
