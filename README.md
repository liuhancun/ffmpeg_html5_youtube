# ffmpeg_html5_youtube
use ffmpeg to convert to format which complies youtube and html5

```sh
$ for f in /x/Anime/\[RAW\]\ Majokko\ Meg-chan/*.avi; do
  fileName="${f##*/}"
  mp4File="${fileName/%.*}.mp4"
  ffmpeg -i "$f" -codec:v libx264 -crf 21 -bf 2 -flags +cgop \
  -pix_fmt yuv420p -codec:a aac -strict -2 -b:a 384k -r:a 48000\
  -movflags faststart "$mp4File"
done
```

<video src="https://drive.google.com/file/d/0B_PUgQ5zTghuZ3NZRFkwN2l2Wnc/view"></video>
<video src="https://drive.google.com/file/d/0B_PUgQ5zTghuZ3NZRFkwN2l2Wnc/view?usp=sharing"></video>
<iframe src="https://drive.google.com/file/d/0B_PUgQ5zTghuZ3NZRFkwN2l2Wnc/preview" width="640" height="480"></iframe>
