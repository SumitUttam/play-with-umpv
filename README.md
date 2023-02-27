# Play with MPV
Chrome extension and python server that allows you to play videos in webpages with MPV instead.  
Works on [hundreds of sites](https://rg3.github.io/youtube-dl/supportedsites.html) thanks to youtube-dl,
and even torrents if you install [peerflix](https://github.com/mafintosh/peerflix).

## Changes in this Fork
This fork uses [umpv command](https://github.com/mpv-player/mpv/blob/master/TOOLS/umpv)
By using umpv any video opened is queued in the mpv window already running from umpv.

### Planned Changes
Setting up a config file or args to switch between using mpv or umpv command.
Working on a fork of umpv that allows passing args to mpv.

## Installation
1. Install [MPV](https://mpv.io/installation/)
2. Install [python 2 or 3](https://www.python.org/downloads/) and [pip](https://pip.pypa.io/en/stable/installing/)
3. Install [chrome extension](https://chrome.google.com/webstore/detail/play-with-mpv/hahklcmnfgffdlchjigehabfbiigleji)
4. Run `pip install git+git://https://github.com/SumitUttam/play-with-umpv --user`
5. Start server by running `play-with-umpv` (or use the Linux _free desktop_ shortcut)

(optional) Install [fair-use](https://chrome.google.com/webstore/detail/fair-use-download/fhokdginneihphnneihijgbhbdoehjaj) extension.  
(optional) Install [peerflix](https://github.com/mafintosh/peerflix) to stream torrents.  
(optional) Install [mkchromecast](http://mkchromecast.com/) `pip install git+git://github.com/muammar/mkchromecast --user`
and [extension](https://chrome.google.com/webstore/detail/edeepcccaejnnodlpmcoackkdgaijakg).  
(recommended) Install yt-dlp instead of youtube-dl for better performance. 
## Usage
Right-click [this link](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and select "Play with MPV".
MPV should popup and start playing the video. (Ctrl+Space also works)

![screenshot](https://github.com/thann/play-with-mpv/raw/master/screenshot.png)

## Autostart
- Linux: `cp {/usr,~/.local}/share/applications/thann.play-with-mpv.desktop ~/.config/autostart`
- MacOS: [instructions](https://stackoverflow.com/questions/29338066/mac-osx-execute-a-python-script-at-startup)
- Windows [instructions](https://stackoverflow.com/questions/4438020/how-to-start-a-python-file-while-windows-starts)

## Protips
MPV is [highly configurable](https://mpv.io/manual/stable/), this is just how I like to use it.

To start in the corner, have no border, and stay on top: edit `~/.config/mpv/mpv.conf`
```
ontop=yes
border=no
window-scale=0.4
geometry=100%:100%
```

In order to resize the window without borders, add keybinds: edit `~/.config/mpv/input.conf`
```
` cycle border
ALT+UP add window-scale 0.05
ALT+DOWN add window-scale -0.05
```
