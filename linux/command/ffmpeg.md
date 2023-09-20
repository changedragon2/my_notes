1. flac 转 mp3 并指定码率320kbps
```shell
ffmpeg -i <input.flac> -acodec -b:a 320k <output.mp3>
```