---
layout: post
title: Shadow on Pop!_OS/Ubuntu 19.10
categories: Linux
mathjax: true
---

I recently moved to a [System76](https://system76.com) Darter Pro running [Pop!\_OS 19.10](https://system76.com/pop) as my primary laptop (review coming soon). As you might have guessed by the version number, Pop!\_OS is System76's fork of Ubuntu. With this move, I switched to [Shadow](https://shadow.tech) as my cloud gaming service, since they have a supported Linux client - no messing with Wine, dual boots, or VMs required! The Shadow Linux client is built to be compatible with 18.04+ but didn't work right away due to some [Video Acceleration](https://wiki.archlinux.org/index.php/Hardware_video_acceleration) issues. Below is a guide for getting Shadow running on 19.10 based on my experience troubleshooting.

<div style="content: ''; clear: both; display: flex;">
  <div style="float: left; width 40%; padding: 5px; flex: 40%">
    <img src="/images/blog/shadow_pop/pop.png">
  </div>
  <div style="float: right; width 60%; padding: 5px; flex:60%">
    <img src="/images/blog/shadow_pop/shadow_logo.jpeg">
  </div>
</div>

The [Shadow Linux client](https://nicolasguilloux.github.io/blade-shadow-beta/) is an easy to use AppImage file which looks to have been developed initially by the Shadow Linux community. Following the documentation for getting the VA-API to detect my onboard GPU, I ran into numerous issues with drivers. Despite my efforts, I could not get any results with the i965 driver, so I tried using the iHD driver suggested by a random StackExchange post. By switching drivers and passing a flag when launching Shadow, the client runs and streams without issues.

Here are the steps:

1 - Use `vainfo` to find your GPU. If you see `-1` returned anywhere (like below), then you likely have driver problems.

{% highlight Bash %}
> sudo apt-get install vainfo
> vainfo
libva info: VA-API version 1.5.0
libva info: va_getDriverName() returns 0
libva info: Trying to open /usr/lib/x86_64-linux-gnu/dri/i965_drv_video.so
libva info: Found init function __vaDriverInit_1_4
libva error: /usr/lib/x86_64-linux-gnu/dri/i965_drv_video.so init failed
libva info: va_openDriver() returns -1
vaInitialize failed with error code -1 (unknown libva error),exit
{% endhighlight %}

2 - Install the [drivers for the onboard GPU](https://github.com/intel/media-driver). Note that `intel-media-va-driver` doesn't seem to give you all that you need, so `intel-media-va-driver-non-free` may be necessary.

{% highlight Bash %}
>sudo apt-get install libva libmfx1 libmfx-tools intel-media-va-driver-non-free
{% endhighlight %}

3 - Check that the drivers are recognized. You should be seeing both `H264` and `HEVC` in the output.

{% highlight Bash %}
> export LIBVA_DRIVER_NAME=iHD
> vainfo
libva info: VA-API version 1.5.0
libva info: va_getDriverName() returns 0
libva info: User requested driver 'iHD'
libva info: Trying to open /usr/lib/x86_64-linux-gnu/dri/iHD_drv_video.so
libva info: Found init function __vaDriverInit_1_5
libva info: va_openDriver() returns 0
vainfo: VA-API version: 1.5 (libva 2.5.0)
vainfo: Driver version: Intel iHD driver - 1.0.0
vainfo: Supported profile and entrypoints
      VAProfileNone                   :	VAEntrypointVideoProc
      VAProfileNone                   :	VAEntrypointStats
      VAProfileMPEG2Simple            :	VAEntrypointVLD
      VAProfileMPEG2Simple            :	VAEntrypointEncSlice
      VAProfileMPEG2Main              :	VAEntrypointVLD
      VAProfileMPEG2Main              :	VAEntrypointEncSlice
      VAProfileH264Main               :	VAEntrypointVLD
      VAProfileH264Main               :	VAEntrypointEncSlice
      VAProfileH264Main               :	VAEntrypointFEI
      VAProfileH264Main               :	VAEntrypointEncSliceLP
      VAProfileH264High               :	VAEntrypointVLD
      VAProfileH264High               :	VAEntrypointEncSlice
      VAProfileH264High               :	VAEntrypointFEI
      VAProfileH264High               :	VAEntrypointEncSliceLP
      VAProfileVC1Simple              :	VAEntrypointVLD
      VAProfileVC1Main                :	VAEntrypointVLD
      VAProfileVC1Advanced            :	VAEntrypointVLD
      VAProfileJPEGBaseline           :	VAEntrypointVLD
      VAProfileJPEGBaseline           :	VAEntrypointEncPicture
      VAProfileH264ConstrainedBaseline:	VAEntrypointVLD
      VAProfileH264ConstrainedBaseline:	VAEntrypointEncSlice
      VAProfileH264ConstrainedBaseline:	VAEntrypointFEI
      VAProfileH264ConstrainedBaseline:	VAEntrypointEncSliceLP
      VAProfileVP8Version0_3          :	VAEntrypointVLD
      VAProfileVP8Version0_3          :	VAEntrypointEncSlice
      VAProfileHEVCMain               :	VAEntrypointVLD
      VAProfileHEVCMain               :	VAEntrypointEncSlice
      VAProfileHEVCMain               :	VAEntrypointFEI
      VAProfileHEVCMain10             :	VAEntrypointVLD
      VAProfileHEVCMain10             :	VAEntrypointEncSlice
      VAProfileVP9Profile0            :	VAEntrypointVLD
      VAProfileVP9Profile2            :	VAEntrypointVLD

{% endhighlight %}

4 - Test the video encoding. It's a strange video... but it's in the [Intel Media Kit documentation](https://github.com/Intel-Media-SDK/MediaSDK/wiki/Intel-media-stack-on-Ubuntu).

{% highlight Bash %}
>wget https://fate-suite.libav.org/h264-conformance/AUD_MW_E.264
>/usr/share/mfx/samples/sample_decode h264 -i AUD_MW_E.264 -r -f 30 -rgb4
{% endhighlight %}

5 - Run the Shadow AppImage with the _no sandbox_ option set.

{% highlight Bash %}
>cd path/to/AppImage/directory
>./Shadow.AppImage --no-sandbox
{% endhighlight %}

For the future, you may want to add the export statement from step three to your .bashrc file or create a shell script to that runs the export statement and the AppImage. Enjoy!

>Note: I'm still not 100% confident in the details of how this method works under the hood. If anyone wants to chat about it, feel free to email me at brettcmullins at gmail.com.
