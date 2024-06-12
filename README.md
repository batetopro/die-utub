# die-utub

How to download videos and songs from YouTube?

## Setup

You need a python installed on the system.

Then create a virtual environment.

> python -m venv .venv

Activate the virtual environment.

On Linux:
> source .venv/bin/activate

On Windows:
> .venv/Scripts/activate.bat

Install the requirements:

> pip install -r requirements.txt

Prepare the downloads directory

> mkdir utub

> cd utub

## Download a mp3

To download a video from YouTube use this command: 

> yt-dlp --format bestaudio --extract-audio --audio-format mp3 --audio-quality 160K VIDEO_URL

Replace VIDEO_URL with the url of the video you want to download.

## Download a playlist and save it as mp3s

To download a playlist from YouTube use this command:

>  yt-dlp --ignore-errors --format bestaudio --extract-audio --audio-format mp3 --audio-quality 160K --output "%(playlist_index)s. %(title)s.%(ext)s" --yes-playlist PLAYLIST_URL

Replace PLAYLIST_URL with the url of the playlist you want to extract.

For more options about the format of the saved files, follow this [link](https://github.com/ytdl-org/youtube-dl#output-template).
