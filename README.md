# Convertidor de estudio de Nimbo

Este repositorio distribuye el **convertidor de audio** opcional que la app de escritorio Nimbo descarga desde Modo DJ y La cabina. La app lo descarga solo si la persona lo pide.

- **Contenido:** `ffmpeg.exe` sin modificar. Es FFmpeg `n9.0.2-39-g7adfbe40dc`, compilación estática win64 **LGPL** (versión 3 o posterior), tomada de [FFmpeg-Builds](https://github.com/FFmpeg-Builds/FFmpeg-Builds), publicación `autobuild-2026-10-31-12-59`.
- **Por qué existe:** el archivo original trae también ffprobe y ffplay, y pesa 161 MB. Aquí va solo `ffmpeg.exe`, comprimido, en unos 52 MB.
- **Integridad:** la app comprueba las huellas SHA-256 del zip y del programa antes de usarlo. Las huellas están en las notas de cada publicación.
- **Licencia:** `LICENSE.txt` (GNU LGPL). Código fuente correspondiente: https://git.ffmpeg.org/ffmpeg.git (`n9.0.2-39-g7adfbe40dc`) y las recetas de compilación de FFmpeg-Builds. FFmpeg es una marca de Fabrice Bellard. Más detalle en `FUENTE.txt`.
