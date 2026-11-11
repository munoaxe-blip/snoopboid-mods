# snoopboid-mods

Lista pública de mods del pack de Project Zomboid (Build 42) que usa la app **SNOOPBOID MANAGMENT PROJECT**.

Solo contiene datos públicos: nombres de mods y sus IDs de Steam Workshop. La app la lee al arrancar
(una única petición HTTPS a `mods.json`, sin enviar ningún dato) y avisa si hay novedades.

Colección de Steam: https://steamcommunity.com/sharedfiles/filedetails/?id=3837337178

## Cómo actualizar la lista

1. Edita `mods.json` (en GitHub: abre el archivo → icono del lápiz).
2. Añade, quita o cambia mods. Cada mod lleva:
   - `nombre`, `workshopId` (solo números), `categoria`
   - `tipo`: `"nucleo"` (obligatorio para jugar) u `"opcional"`
   - `esCritico` (`true`/`false`) y `notas` (texto libre)
   - opcionales: `modIds` (qué variantes activar en el servidor), `arregloTemporal`
3. **Sube `lista_version` en 1** y cambia `actualizado` a la fecha de hoy. Sin eso la app no detecta el cambio.
4. Guarda (Commit changes). Actualiza también la colección de Steam para que coincida.
5. Si sacas una versión nueva de la app, cambia `app_version_ultima` (y `app_version_minima` si la vieja ya no sirve).

La app comprueba el formato: si algo está mal escrito, sigue usando la última lista buena.
