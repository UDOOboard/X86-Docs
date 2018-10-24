The Graphic controller of the **UDOO X86** is the integrated **Intel&reg; HD Graphics**.  
Depending of the UDOO X86 version this are the specification:

* Intel&reg; HD Graphics 405 Up to 700 MHz 16 execution units (**ULTRA** version)
* Intel&reg; HD Graphics 400 Up to 640 MHz 12 execution units (**ADVANCED PLUS**)


### Decoding/Encoding specification

|             | formats                                                     |
|-------------|-------------------------------------------------------------|
| HW decoding | HEVC(H.265), H.264, MPEG2, MVC, VC-1, VP8, WMV9, JPEG/MJPEG |
| HW encoding | H.264, MVC, JPEG/MPEG                                       |


### Video Output Connectors

The Intel® Braswell family of SoCs offer three Digital Display Interfaces, configurable to work in HDMI/DVI/DP++ modes.  

#### HDMI Connector

On the UDOO x86 board, the Digital Display Interface #0 is used to implement a HDMI interface.

HDMI featured by the Intel&reg; Braswell processor is the version v1.4b.  

Maximum resolution:
* 3840x2160 @ 30Hz
* 2560x1600 @ 60Hz
* 24bpp

<span class="label label-warning">Heads up!</span>  Always use HDMI-certified cables for the connection between the board and the HDMI display; a category 2 (High-Speed) cable is recommended for higher resolutions, category 1 cables can be used for 720p resolution.

You can use this [HDMI to HDMI](http://shop.udoo.org/cable-hdmi-to-hdmi.html) cable to connect to a HDMI display in 4k resolution.

#### MiniDisplay Port ++ Connectors

On the UDOO x86 board, the Digital Display Interfaces #1 and #2 are used to implement a multimode Display Port (DP++) interface, i.e. it can be used to support DP displays directly and, through an external adapter, also HDMI or DVI displays.

The configuration of this interface in DP or HDMI/DVI mode is automatic.

DP++ featured by the Intel&reg; Braswell processor is the version v1.1a.  

Maximum resolution:
* 3840x2160 @ 30Hz
* 2560x1600 @ 60Hz
* 24bpp


You can use this [MiniDP++ to DP](http://shop.udoo.org/cable-minidp-to-dp.html) cable to connect to a DisplayPort display in 4k resolution.  
You can use this [MiniDP++ to HDMI](http://shop.udoo.org/cable-minidp-to-hdmi.html) cable to connect to an HDMI display in FullHD resolution. To have 4k resolution from mDP to HDMI you need an active adapter.



### UDOO X86 Hardware and UEFI BIOS User Manual

For a complete explanation of the UDOO X86 hardware you can download the [UDOO X86 Hardware and UEFI User Manual](http://download.udoo.org/files/UDOO_X86/Doc/UDOO_X86_MANUAL.pdf)
