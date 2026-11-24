# Convertidor de estudio de Nimbo

Este repositorio distribuye el **convertidor de audio** opcional que la app de escritorio Nimbo descarga desde Modo DJ y La cabina. La app lo descarga solo si la persona lo pide.

## Publicaciones

| Publicación | Estado | Contenido |
|---|---|---|
| `convertidor-n9.0.2-lgpl-2` | **Vigente** | FFmpeg `n9.0.2-62-gac1c6e003f` (commit `ac1c6e003f9e298536363e716750abc0c8f25b37`), compilación estática win64 **LGPL** (versión 3 o posterior) de [FFmpeg-Builds](https://github.com/FFmpeg-Builds/FFmpeg-Builds), publicación `autobuild-2026-11-23-12-43`, sin modificar. |
| `convertidor-n9.0.2-lgpl-1` | **Retirada** | Se retiró porque esa compilación de terceros incluía libzvbi, que contiene código GPL-2.0 solo (incompatible con una compilación LGPL v3). No la uses. |

## Qué lleva la publicación `-lgpl-2`

- **Zip** `nimbo-convertidor-n9.0.2-lgpl-win64-2.zip`, con:
  - `ffmpeg.exe` (sin modificar, sin ffprobe ni ffplay: pesa unos 56 MB comprimido en lugar de 170),
  - `LICENSE.txt` (GNU LGPL v3),
  - `COPYING.GPLv3.txt` (GNU GPL v3, que la LGPL v3 incorpora por referencia),
  - `FUENTE.txt` (de dónde sale el programa, commits completos y enlaces al código fuente),
  - `THIRD-PARTY-NOTICES.txt` (avisos y licencias de las bibliotecas que van dentro de `ffmpeg.exe`).
- **Código fuente correspondiente**, como archivos de la misma publicación:
  - `ffmpeg-ac1c6e003f-src.tar.xz`: FFmpeg en ese commit,
  - `ffmpeg-builds-b9ebe81-src.tar.xz`: las recetas de compilación de FFmpeg-Builds (con `patches/`),
  - `deps-src.tar.xz`: el código de las bibliotecas incluidas, cada una en el commit que fijan las recetas (sin submódulos; ver `FUENTE.txt`).
- **Integridad:** la app comprueba las huellas SHA-256 del zip y del programa antes de usarlo. Las huellas están en las notas de la publicación.

## Licencia y código fuente

`ffmpeg.exe` es FFmpeg bajo la **GNU LGPL v3 o posterior** (sin `--enable-gpl` ni `--enable-nonfree`). Los textos están en `LICENSE.txt` y `COPYING.GPLv3.txt`; las licencias de las bibliotecas incluidas, en `THIRD-PARTY-NOTICES.txt`. De dónde sale el programa y dónde está su código fuente: `FUENTE.txt`. FFmpeg es una marca de Fabrice Bellard; Nimbo no está respaldado por el proyecto FFmpeg.

Esta es información técnica de licencias, no asesoría legal.
