1. flac 转 mp3 并指定码率320kbps
```shell
ffmpeg -i <input.flac> -acodec -b:a 320k <output.mp3>
```
2. flac to mp3
```shell
ffmpeg -i <input.flac> -acodec libmp3lame <output.mp3>
```
3. get music cover
```shell
ffmpeg -i <input.flac> -an -vf scale=500:500 <output.png>
```

### Image
jpg to png(SQ)
```shell
ffmpeg -i input.jpg -compression_level 0 output.png
```