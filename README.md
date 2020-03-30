# Mediacommands for Linux Servers
The Following Commands can be used to download Videos and other media to Linux Servers. The use of these Commands are for educational purposes only!

## Download YouTube-Playlist as MP3
```
youtube-dl --ignore-errors --format bestaudio --extract-audio --audio-format mp3 --audio-quality 160K --output "%(title)s.%(ext)s" --yes-playlist '<YouTube playlist URL>'
```

## Download YouTube-Playlist as MP4
```
youtube-dl -cit <playlist_url>
```


## Download MediathekViewWeb-m3u8-Stream as MP4
```
echo "Enter m3u8 link:";read link;echo "Enter output filename:";read filename;ffmpeg -i "$link" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 $filename.mp4
```

## Generate Video-File using Image and Audio Files in FFMPEG
```
ffmpeg -i image.jpg -i audio.mp3 -c:v libx264 -tune stillimage -c:a copy out.mp4
```
