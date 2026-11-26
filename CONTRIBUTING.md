# Cómo participar

Podés escribir tus issues y pull requests en español o en inglés. El código y los commits van en inglés.

## Sumate en 3 pasos

1. **Hacé fork** de este repositorio.
2. **Agregá tu archivo** `members/<tu-usuario-de-github>.json` con este contenido:
   ```json
   {
     "github": "tu-usuario",
     "country": "NI"
   }
   ```
   `country` es el código ISO de 2 letras de tu país. Países permitidos: AR BO BR CL CO CR CU DO EC GT HN MX NI PA PE PR PY SV UY VE.
3. **Abrí un Pull Request.** Una validación automática revisa el formato.

Reglas:

- El nombre del archivo tiene que ser igual a tu usuario de GitHub.
- Solo podés agregar o cambiar **tu propio** archivo: nadie agrega a otra persona sin su consentimiento.
- Solo se permiten las claves `github` y `country`.

Para probar en local: `node --test && node scripts/validate.mjs` (Node 20+).

<a id="proponer-una-categoria-nueva"></a>

## Proponer una categoría nueva

Abrí un issue con el título `Categoría: <nombre>` e incluí:

- qué se mide y cómo se calcula (fuente de datos pública de GitHub),
- por qué es justa para participantes de distintos tamaños,
- un ejemplo con al menos un usuario real.

La categoría se acepta cuando hay acuerdo en el issue y se implementa en un PR aparte.

## Proponer un país nuevo

Abrí un issue e incluí:

- el código del país (ISO de 2 letras),
- el nombre del país,
- por qué debería estar en la lista.

## Proponer un cambio en la página

Abrí un issue o un pull request e incluí:

- qué cambia,
- por qué,
- que la página sigue funcionando en el celular.
