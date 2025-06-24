# FFmpeg_concat
Script para ejecutar FFmpeg y concatenar vídeos .mov o .mp4

Script para Windows que genera un vídeo a base de combinar varios vídeos y separarlos entre sí por 2s de negro.
Este script puede concatenar cualquier vídeo .mov o .mp4 que haya en una carpeta "toFFmpeg"
En esa carpeta también tiene que haber un vídeo "00_black2s.mov" que es negro con audio silencio de 2s.
El resultado es un vídeo con el codec h264 .mp4 que aparecerá dentro de la carpeta del script cuando se ejecute.

Modo de uso:
- Todos los vídeos tienen que tener el mismo tamaño.
- Los vídeos pueden ser .mov o .mp4
- Todos los vídeos tienen que tener pista de audio aunque sea silencio.
- Todos los vídeos tienen que estar en la misma carpeta "toFFmpeg"
- Para indicar el orden de los vídeos hay que numerarlos. En el nombre que tengan conviene incluir número al principio: 01 nombre1, 02 nombre2...
- En esa carpeta "toFFmpeg" siempre tiene que estar un vídeo de negro llamado "00_black2s.mov"

La estructura de carpeta del script es:

📁 Carpeta script
│
├── concat_ffmpeg_todo.bat  ← el script está aquí
└── 📁 toFFmpeg
    ├── 00_black2s.mov
    ├── 01_video1.mov
    ├── 02_video1.mp4
    └── ...

