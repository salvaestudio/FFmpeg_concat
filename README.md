# FFmpeg_concat

script_todos   >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

Script para ejecutar FFmpeg y concatenar vídeos .mov o .mp4

Script para Windows que genera un vídeo a base de combinar varios vídeos y separarlos entre sí por 2s de negro.
Este script puede concatenar cualquier vídeo .mov o .mp4 que esté alojado en una carpeta "toFFmpeg"
En esa carpeta también tiene que haber un vídeo "00_black2s.mov" que es negro con audio silencio de 2s.
El resultado es un vídeo con el codec h264 .mp4 que aparecerá dentro de la carpeta del script cuando se ejecute.

Modo de uso:
- Los vídeos input pueden tener varios tamaños. Se ajustarán a 1920x1080 en el vídeo resultante.
- Los vídeos pueden ser .mov o .mp4
- Los vídeos pueden tener pista de audio o no. El codificador detectará cuáles tienen audio y cuáles no, y en caso de no tener pista de audio incluirá una pista de silencio.
- Todos los vídeos tienen que estar en la misma carpeta "toFFmpeg"
- Para indicar el orden de los vídeos hay que numerarlos. En el nombre que tengan conviene incluir número al principio: 01 nombre1, 02 nombre2...
- En esa carpeta "toFFmpeg" siempre tiene que estar un vídeo de negro llamado "00_black2s.mov"
- Al ejecutar el script, se genera una carpeta "intermedios" que es la que guarda temporalmente los vídeos codificados temporalmente. Al acabar el script se borrará automáticamente
- El resultado derá un archivo de vídeo "salida.mp4" alojado en la misma ruta de los vídeos input, en "toFFmpeg"

La estructura de carpeta del script es:



````
📁 Carpeta script
    . concat_ffmpeg_todo.bat  ← el script está aquí
    .📁 toFFmpeg
        .00_black2s.mov
        .01_video1.mov
        .02_video1.mp4
        
        ...

````

script_mov y script_mp4 >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>  

Lo mismo pero preparados SOLO para codificar en HD y SOLO .mov prores o SOLO .mp4
Por tanto en la carpeta "toFFmpeg" solo puede haber archivos del mismo tamaño, HD y solo .mov o solo .mp4 dependiendo del script que se use. 

