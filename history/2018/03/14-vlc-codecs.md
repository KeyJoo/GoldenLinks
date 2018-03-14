


`cd /usr/lib/vlc/plugins/codec`

https://gist.github.com/2bbac8ce506b31e5a37fff41118a947b


Через GUI VLC 2.2.2 вываливает ошибки
> Codec not supported:
> VLC could not decode the format "h264" (H264 - MPEG-4 AVC (part 10))

Запуская в терминале
`vlc video.mp4`

и уже можно смотреть видео со звуком, но вот ошибки:

```
➜  Vue.js_Dmitriy-Lavrik vlc Урок\ 1
VLC media player 2.2.2 Weatherwax (revision 2.2.2-0-g6259d80)
[000000000233c088] core libvlc: Running vlc with the default interface. Use 'cvlc' to use vlc without interface.
libdvdnav: Using dvdnav version 5.0.3
libdvdread: Couldn't find device name.
libdvdread:DVDOpenFilePath:findDVDFile /VIDEO_TS/VIDEO_TS.IFO failed
libdvdread:DVDOpenFilePath:findDVDFile /VIDEO_TS/VIDEO_TS.BUP failed
libdvdread: Can't open file VIDEO_TS.IFO.
libdvdnav: vm: failed to read VIDEO_TS.IFO
[00000000024234c8] core playlist: stopping playback
[00007fa5f8056368] vdpau_avcodec generic error: decoder profile not supported: 6
```