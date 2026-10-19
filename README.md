# Shin Megami Tensei: Strange Journey — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **español de España** de *Shin Megami Tensei: Strange Journey* (Nintendo DS, Atlus, 2010), que nunca salió en español. Se ha hecho sobre la **edición estadounidense en inglés**; no es una traducción directa del japonés.

El parche es un **XDELTA** que se aplica a tu propia copia del juego: aquí no se distribuye ninguna ROM.

## Estado

Versión **1.0**: guion completo, interfaz de texto y gráficos de interfaz.

| Parte | Alcance |
|---|---|
| Guion e interfaz de texto | **16.556 mensajes** traducidos: historia, misiones y registro de misiones, negociación con demonios, compendio, objetos, habilidades, menús y ayudas |
| Texto dentro de imágenes | **43 gráficos de interfaz**: botones del título, opciones, combate (estados, resultados, panel del enemigo), menú Demonica, estado, guardado, registro de misiones, fusión, visor, barra y leyenda del automapa, teclado de nombre |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »**, con la fuente original del juego (mismo trazo y contraste) |

La terminología es la de nuestra traducción de *[Strange Journey Redux](https://github.com/johanderohan/shin-megami-tensei-strange-journey-redux-traduccion-es)* (3DS): donde el inglés de la DS es idéntico se ha reutilizado esa traducción, adaptada a la pantalla de la DS; donde la DS dice otra cosa, se ha traducido lo que dice la DS. Se conservan los nombres de demonio y de hechizo de la saga (Jack Frost, Pixie, Agi, Dia…) y los logotipos.

### Comprobaciones y límites

- Todo el texto se ha reinsertado con validación automática de códigos de control, variables (incluido el tamaño de los búferes donde el juego escribe nombres), anchura en píxeles con la fuente real del juego y líneas por cuadro; los límites se midieron en el emulador. Una auditoría vuelve a leer la ROM construida y comprueba cada mensaje y gráfico.
- Traducción por lotes con biblia y glosario comunes, revisión editorial independiente de todos los lotes nuevos y pasadas de unificación.
- **Prueba jugable en emulador (DeSmuME):** tres rondas desde partida nueva (unas 6 horas de juego en total, con revisión de más de 7.000 capturas): apertura, nombre del protagonista, Red Sprite, test de personalidad, menús de la Demonica, registro de misiones, primera planta del Sector Antlia con combates, análisis, negociación y reclutamiento de demonios, Game Over y **guardado y carga reales**. Sin cuelgues. La memoria del juego se ha medido con los ficheros traducidos (sobra espacio).
- **Pendiente:** no se han jugado la fusión de demonios, los jefes ni los sectores posteriores a Antlia; falta una partida completa hasta los finales y la prueba en consola física o flashcart.
- Siguen en inglés: el aviso legal del arranque, los textos grabados en el vídeo de apertura, los créditos finales, algunas insignias pequeñas que no caben traducidas («NEW», «TIME», «GUN», «MAIN») y el rótulo «UNKNOWN» del panel del enemigo. Los mensajes internos de desarrollo que el juego no muestra se han dejado como estaban.
- **Si usas DeSmuME** y ves letras con trozos borrados, es un fallo de la caché de texturas del emulador que también afecta al juego original en inglés: activa la opción *Texture hack* (en RetroArch, `desmume_gfx_txthack`). Con esa opción el texto se ve completo.

La traducción y la revisión se han hecho con asistencia de modelos de IA; no se atribuye una revisión humana independiente.

## Descarga

En **[Releases](../../releases)**: `Shin.Megami.Tensei.Strange.Journey.ES.v1.0.xdelta`

- SHA-256 del parche: `4a97cfaea047a2ca2ec54c24e1e63ce2301edbebd6ba183c8e912ed80046158c`

## Versión necesaria

| Dato | Valor |
|---|---|
| Edición | Estados Unidos (USA), código `BMTE` |
| ROM usada en las pruebas | `Shin Megami Tensei - Strange Journey (USA).nds` |
| Tamaño | 134.217.728 bytes |
| MD5 | `47cfc1ef624ea3a43f1aa0a49d551d1a` |
| SHA-256 | `f4709745c10fca7024bd34dec4c0c6251a29088037aad596c8d52b63409a49ab` |

El parche exige **esta ROM exacta**. No es compatible con la edición japonesa ni con *Redux* (3DS).

## Cómo aplicar el parche

1. Comprueba que tu ROM tiene el tamaño y el MD5 de arriba:

   ```bash
   md5sum "Shin Megami Tensei - Strange Journey (USA).nds"                     # Linux
   md5 "Shin Megami Tensei - Strange Journey (USA).nds"                        # macOS
   CertUtil -hashfile "Shin Megami Tensei - Strange Journey (USA).nds" MD5     # Windows
   ```

2. Aplica el parche con [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases) (Windows, macOS y Linux, con ventanas) o con xdelta3:

   ```bash
   xdelta3 -d -s "Shin Megami Tensei - Strange Journey (USA).nds" Shin.Megami.Tensei.Strange.Journey.ES.v1.0.xdelta "Shin Megami Tensei - Strange Journey (ES).nds"
   ```

3. La ROM resultante ocupa **134.217.728 bytes**, MD5 `708038c4c680741b471128208e2f45c6` y SHA-256 `89dd0caf95e1e96d4a954c53a9052d3efa230bd9d95bdf140f3974ba56fbdb0c`.

Las partidas guardadas de la versión inglesa sirven. No cargues estados rápidos (*savestates*) creados con otra versión del juego o del parche.

## Cambios

### v1.0 — 2026-10-19

- Primera versión pública: guion, interfaz y gráficos de interfaz en castellano.

## Créditos y aviso

Proyecto de **johanderohan / Parches en Castellano**. Juego y materiales originales de **ATLUS**. Traducción de aficionados sin ánimo de lucro y sin relación oficial con Atlus ni con sus titulares.

Herramientas: utilidades propias de extracción y reinserción, DeSmuME (núcleo libretro) y xdelta3. Las letras castellanas son las de la propia fuente del juego.

El repositorio contiene solo este README; el parche está en Releases. No se publican ROMs, partidas ni el guion extraído. Si encuentras un problema, abre una incidencia indicando la versión del parche, el emulador o consola y una captura.
