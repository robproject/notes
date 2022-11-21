---
id: 3l5r4y1yy4pctfifqwgwqd8
title: Youtube Downloader
desc: ''
updated: 1666808985257
created: 1637554443589
---

youtube-dl -x --audio-format mp3 


### Playlist old way
source venv/bin/activate
cd playlist
youtube-dl --rm-cache-dir
youtube-dl --playlist-start 989 -x -v --audio-format mp3 PLrZnjECO5SND228JDgd4cmjFXXLPwNE96

### Playlist
https://stackoverflow.com/a/47093424
```
PLAYLIST='PLAYLIST_ID'
PLAYLIST_LENGTH='number of songs in playlist'
source venv/bin/activate
cd playlist
for (( i=0; i<$PLAYLIST_LENGTH; i+=100 )); do
	youtube-dl -ciw --extract-audio --audio-format mp3 --playlist-start $i --playlist-end $(($i+99)) --restrict-filenames $PLAYLIST &
done
```