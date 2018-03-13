## Hardware video acceleration

To play video using the GPU (Intel HD Graphics) resources you need to use the Intel&reg; [Video Acceleration API (VA-API)](https://en.wikipedia.org/wiki/Video_Acceleration_API) and a software that exploits this specific API.

**VA-API** is a specification and open source library to provide both hardware accelerated video encoding and decoding, developed by Intel.  
Without using VA-API all the encoding and decoding processes are in charge of the CPU.

### Verifying VA-API

Verify the settings for VA-API by running `vainfo`.

```bash
$ vainfo
libva info: VA-API version 0.39.2
libva info: va_getDriverName() returns 0
libva info: Trying to open /usr/lib/x86_64-linux-gnu/dri/i965_drv_video.so
libva info: Found init function __vaDriverInit_0_39
libva info: va_openDriver() returns 0
vainfo: VA-API version: 0.39 (libva 1.7.1)
vainfo: Driver version: Intel i965 driver for Intel(R) CherryView - 1.7.1
vainfo: Supported profile and entrypoints
      VAProfileMPEG2Simple            :	VAEntrypointVLD
      VAProfileMPEG2Simple            :	VAEntrypointEncSlice
      VAProfileMPEG2Main              :	VAEntrypointVLD
      VAProfileMPEG2Main              :	VAEntrypointEncSlice
      VAProfileH264ConstrainedBaseline:	VAEntrypointVLD
      VAProfileH264ConstrainedBaseline:	VAEntrypointEncSlice
      VAProfileH264Main               :	VAEntrypointVLD
      VAProfileH264Main               :	VAEntrypointEncSlice
      VAProfileH264High               :	VAEntrypointVLD
      VAProfileH264High               :	VAEntrypointEncSlice
      VAProfileH264MultiviewHigh      :	VAEntrypointVLD
      VAProfileH264MultiviewHigh      :	VAEntrypointEncSlice
      VAProfileH264StereoHigh         :	VAEntrypointVLD
      VAProfileH264StereoHigh         :	VAEntrypointEncSlice
      VAProfileVC1Simple              :	VAEntrypointVLD
      VAProfileVC1Main                :	VAEntrypointVLD
      VAProfileVC1Advanced            :	VAEntrypointVLD
      VAProfileNone                   :	VAEntrypointVideoProc
      VAProfileJPEGBaseline           :	VAEntrypointVLD
      VAProfileJPEGBaseline           :	VAEntrypointEncPicture
      VAProfileVP8Version0_3          :	VAEntrypointVLD
      VAProfileVP8Version0_3          :	VAEntrypointEncSlice
      VAProfileHEVCMain               :	VAEntrypointVLD

```

### Play Videos with Hardware video acceleration

You need to use a software that use VA-API.

For example you can install GStreamer with the VA-API Plugin (gstreamer-vaapi).  

```bash
sudo apt install gstreamer1.0 gstreamer1.0-vaapi
```
and play a video using

```bash
gst-play-1.0 video.name
```

In this way the video playing will exploits GPU and will not impact on the CPU load a lot.  

### Reference

For more info you can check this page [Hardware_video_acceleration](https://wiki.archlinux.org/index.php/Hardware_video_acceleration). 
