# Editor de savegame para Vampire Crawlers

[English version](README.English.md)

Página web para ver y editar el archivo de guardado (`SaveProfile0.save`) de **Vampire Crawlers**. Se abre en el navegador, no hay que instalar nada y **el archivo no se sube a ningún servidor**: todo ocurre en tu equipo.

**Usar ahora:** https://agnesti.github.io/vampire-crawlers-savegame-web/

## Qué puede hacer

- Mostrar un resumen del guardado: monedas, grupo, personajes comprados, tiempo jugado y progreso.
- Cambiar las **monedas**. Existen en dos secciones del archivo (`ProfileSaveData` y `ProgressionSaveData`) y el juego usa la de progresión, así que la página cambia ambas a la vez.
- Activar o desactivar modos de partida, tutoriales, reliquias y mejoras permanentes, y cambiar el nivel de estas últimas.
- Ver y editar el **JSON completo**, con buscador y accesos directos a cada sección.
- **Hacer checksum**: vacía el campo `Checksum` (el juego lo acepta así) y descarga el archivo listo para usar.
- Descargar una **copia del original** antes de reemplazarlo.

## Cómo usarlo

1. Haz una copia de seguridad de tu guardado.
2. Abre la página, pulsa **Seleccionar archivo** y elige `SaveProfile0.save`.
3. Cambia lo que quieras en la pestaña **Resumen** o en **JSON completo**.
4. Pulsa **Hacer checksum**. Se descargará el archivo con el mismo nombre.
5. Copia ese archivo a la carpeta de guardados, reemplazando el original.

## Dónde está el guardado

- **Windows (Steam):** `%USERPROFILE%\AppData\LocalLow\Nosebleed Interactive\Vampire Crawlers\Save\SaveProfile0.save`
- **macOS:** `/Users/<usuario>/Library/Application Support/com.poncle.vampirecrawlers/Save/SaveProfile0.save`
- **Android:** /storage/emulated/0/Android/data/com.poncle.vampirecrawlers/files/Save/SaveProfile0.save

Más rutas en [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Vampire_Crawlers:_The_Turbo_Wildcard_from_Vampire_Survivors#Save_game_data_location).

## Avisos

- Usa la herramienta bajo tu propia responsabilidad y guarda siempre una copia del original.
- Si Steam avisa de un conflicto de sincronización en la nube, conserva el archivo local (el más reciente).
- No pongas en las monedas el valor máximo (2147483647): es el límite de un entero de 32 bits y puede desbordarse al ganar más. Un número como 999999 deja margen.
- Probado con guardados de la versión `0.30.0` del sistema de guardado. Si el juego se actualiza y cambia el formato, algo puede dejar de funcionar.

## Créditos

- Basado en la idea y el hallazgo del [editor de Kartones](https://github.com/Kartones/vampire-crawlers-savegame-editor), que a su vez cita [este artículo](https://www.neonlightsmedia.com/blog/vampire-crawlers-save-transfer-game-pass-steam): el campo `Checksum` puede quedar vacío.
- Iconos de personajes y moneda: [Vampire Survivors Wiki](https://vampire.survivors.wiki/w/Crawlers:Wiki), bajo licencia [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/). Se cargan desde la wiki; sin conexión se muestra una letra.
- Proyecto de fans, **sin relación con poncle ni Nosebleed Interactive**. Vampire Crawlers y Vampire Survivors pertenecen a sus propietarios.
