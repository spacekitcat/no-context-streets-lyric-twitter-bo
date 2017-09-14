== Overview ==
Repository includes lyric data, so it shouldn't be necassary to generate the data.
I include the scripts to document the source of the bot input.

== Requirements ==
Python 3
Beautiful Soup
Curl
Bash

== Data generation script order ==
$ chmod +x fetchRawSongListHtml.sh
$ ./fetchRawSongListHtml.sh           # Fetch remote song list (raw HTML).
$ python parseSongUrlList.py          # Extract the URL for each songs' lyric page and generate the URL list
$ chmod +x fetchRawSongLyricsHtml.sh
$ ./fetchRawSongLyricsHtml.sh         # Fetch the HTML for each url generated by parseSongUrlList
$ python parseLyrics.py               # Extract the song lyrics from each songs' HTML document
