# Quick-Audio-Denoise
Note to self on how to denoise audio from mp4

## How to:
 1. `ffmpeg.exe -i .\Sara_vid.mp4 -ab 160k -ac 2 -ar 44100 -vn audio.wav`
 2. `python denoise.py`
 3. `ffmpeg -i .\Sara_vid.mp4 -i filtered.wav -c:v copy -map 0:v:0 -map 1:a:0 new.mp4`
