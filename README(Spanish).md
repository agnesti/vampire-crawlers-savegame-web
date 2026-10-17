[English version](README.md)

Página web para ver y editar el archivo de guardado (`SaveProfile0.save`) de **Vampire Crawlers**. Se abre en el navegador, no hay que instalar nada y **el archivo no se sube a ningún servidor**: todo ocurre en tu equipo.

**Usar ahora:** https://agnesti.github.io/vampire-crawlers-savegame-web/

## Qué puede hacer

- **Resumen** del guardado: monedas, grupo, personajes, tiempo jugado, estado y progreso.
- **Monedas:** existen en dos secciones del archivo (`ProfileSaveData` y `ProgressionSaveData`) y el juego usa la de progresión, así que la página cambia ambas a la vez.
- **Personajes:** lista de los 21 conocidos; toca uno para marcarlo como comprado o quitarlo.
- **Mazmorras:** cuáles has visitado, cuál está seleccionada y, de forma *experimental*, el logro `Unlock_*` de cada una.
- Modos de partida, tutoriales, reliquias y mejoras permanentes (activación y nivel).
- **JSON completo** con buscador (las coincidencias se resaltan y la vista se desplaza hasta ellas) y accesos directos a cada sección, para edición manual.
- **Comparar:** sube dos guardados y mira qué cambió entre ellos (logros, personajes, cartas, gemas, métricas…).
- **Restablecer:** vuelve a los valores del archivo que subiste si tocas algo por error.
- Aviso cuando el guardado es de una **partida en curso**.
- **Hacer checksum:** calcula el checksum real y descarga el archivo con el mismo formato que usa el juego. Se activa en cuanto cambias algo.
- Descargar una **copia del original** antes de reemplazarlo.

Los campos numéricos solo aceptan dígitos y muestran el teclado numérico en el móvil.

## Cómo usarlo

1. Haz una copia de seguridad de tu guardado.
2. Abre la página, pulsa **Seleccionar archivo** y elige `SaveProfile0.save`.
3. Cambia lo que quieras en **Resumen** o en **JSON completo**.
4. Pulsa **Hacer checksum**. Se descargará el archivo con el mismo nombre.
5. Copia ese archivo a la carpeta de guardados, reemplazando el original.

## Sobre el checksum

El campo `Checksum` es el SHA-1, en base64, del bloque `Data` escrito con sangría de 2 espacios y saltos de línea de Windows. Al cargar un archivo, la página comprueba si el checksum que trae coincide con ese cálculo (lo indica junto al nombre). Si no coincide, al exportar deja el campo vacío, que el juego también acepta. La página conserva el formato original del archivo (saltos de línea y números como `24.0`) para que el resultado sea idéntico al que genera el juego.

## Dónde está el guardado

- **Windows (Steam):** `%USERPROFILE%\AppData\LocalLow\Nosebleed Interactive\Vampire Crawlers\Save\SaveProfile0.save`
- **macOS:** `/Users/<usuario>/Library/Application Support/com.poncle.vampirecrawlers/Save/SaveProfile0.save`

Más rutas en [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Vampire_Crawlers:_The_Turbo_Wildcard_from_Vampire_Survivors#Save_game_data_location).

## Avisos

- Usa la herramienta bajo tu propia responsabilidad y guarda siempre una copia del original.
- Edita guardados tomados desde el menú principal. Con una partida en curso el juego puede sobrescribir los cambios.
- Si Steam avisa de un conflicto de sincronización en la nube, conserva el archivo local (el más reciente).
- No pongas las monedas en el máximo (2147483647): es el límite de un entero de 32 bits y puede desbordarse. Un número como 999999 deja margen.
- El juego acepta niveles de mejora por encima del máximo normal, pero su efecto se limita en partida. Por ejemplo, *Might* muestra un valor mayor en el menú principal, pero el daño se quedó en 1000 % en las mazmorras (se alcanza con el nivel 49 en la prueba del autor).
- Comprar personajes o desbloquear mazmorras a mano no está comprobado en todos los casos. Prueba primero en una copia.
- Probado con guardados de las versiones `0.22.0` y `0.30.0`. Si una actualización cambia el formato, algo puede dejar de funcionar.

## Créditos

- Basado en la idea y el hallazgo del [editor de Kartones](https://github.com/Kartones/vampire-crawlers-savegame-editor), que a su vez cita [este artículo](https://www.neonlightsmedia.com/blog/vampire-crawlers-save-transfer-game-pass-steam): el campo `Checksum` puede quedar vacío.
- Iconos de personajes y moneda: [Vampire Survivors Wiki](https://vampire.survivors.wiki/w/Crawlers:Wiki), bajo licencia [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/). Se cargan desde la wiki; sin conexión se muestra una letra.
- Proyecto de fans, **sin relación con poncle ni Nosebleed Interactive**. Vampire Crawlers y Vampire Survivors pertenecen a sus propietarios.
