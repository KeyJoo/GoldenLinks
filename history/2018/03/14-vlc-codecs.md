Нет возможности просмотра видео через VLC-плеер
================================================

1. OS - Linux Mint 18.3 Cinnamon
2. RAM 4 Gb
3. До этого видео из этой папки смотрел, было всё хорошо


Полез искать ответы на форумах
- https://bbs.archlinux.org/viewtopic.php?id=171859
- https://github.com/Stremio/stremio-bugs/issues/9


## Run VLC in Linux Mint 18.3 at GUI (Nemo 3.6.5)

Через GUI VLC 2.2.2 вываливает ошибки
> Codec not supported:
> VLC could not decode the format "h264" (H264 - MPEG-4 AVC (part 10))


## Run VLC in terminal

Запуская в терминале
`vlc video.mp4`

и уже можно смотреть видео со звуком, но вот ошибки:

```
➜  Vue.js_Dmitriy-Lavrik vlc Урок\ 1
VLC media player 2.2.2 Weatherwax (revision 2.2.2-0-g6259d80)
[000000000233c088] core - libvlc: Running vlc with the default interface. Use 'cvlc' to use vlc without interface.
- libdvdnav: Using dvdnav version 5.0.3
- libdvdread: Couldn't find device name.
- libdvdread:DVDOpenFilePath:findDVDFile /VIDEO_TS/VIDEO_TS.IFO failed
- libdvdread:DVDOpenFilePath:findDVDFile /VIDEO_TS/VIDEO_TS.BUP failed
- libdvdread: Can't open file VIDEO_TS.IFO.
- libdvdnav: vm: failed to read VIDEO_TS.IFO
[00000000024234c8] core playlist: stopping playback
[00007fa5f8056368] vdpau_avcodec generic error: decoder profile not supported: 6
```


## List of VLC-codecs

`cd /usr/- lib/vlc/plugins/codec`

https://gist.github.com/2bbac8ce506b31e5a37fff41118a947b

- liba52_plugin.so
- libadpcm_plugin.so
- libaes3_plugin.so
- libaraw_plugin.so
- libavcodec_plugin.so
- libcc_plugin.so
- libcdg_plugin.so
- libcrystalhd_plugin.so
- libcvdsub_plugin.so
- libddummy_plugin.so
- libdts_plugin.so
- libdvbsub_plugin.so
- libedummy_plugin.so
- libfaad_plugin.so
- libflac_plugin.so
- libg711_plugin.so
- libhwdummy_plugin.so
- libjpeg_plugin.so
- libkate_plugin.so
- lib- libass_plugin.so
- lib- libmpeg2_plugin.so
- liblpcm_plugin.so
- libmpeg_audio_plugin.so
- libomxil_plugin.so
- libopus_plugin.so
- libpng_plugin.so
- librawvideo_plugin.so
- libschroedinger_plugin.so
- libscte27_plugin.so
- libsdl_image_plugin.so
- libshine_plugin.so
- libspeex_plugin.so
- libspudec_plugin.so
- libstl_plugin.so
- libsubsdec_plugin.so
- libsubstx3g_plugin.so
- libsubsusf_plugin.so
- libsvcdsub_plugin.so
- libsvgdec_plugin.so
- libt140_plugin.so
- libtheora_plugin.so
- libtwolame_plugin.so
- libuleaddvaudio_plugin.so
- libvaapi_drm_plugin.so
- libvaapi_x11_plugin.so
- libvorbis_plugin.so
- libx264_plugin.so
- libx265_plugin.so
- libxwd_plugin.so

23:34
`sudo apt-get install ffmpeg`

```
➜  Урок 3 vlc vue-3.mp4 
VLC media player 2.2.2 Weatherwax (revision 2.2.2-0-g6259d80)
[000000000091d088] core libvlc: Running vlc with the default interface. Use 'cvlc' to use vlc without interface.
[00007f9004056038] vdpau_avcodec generic error: decoder profile not supported: 6

```


