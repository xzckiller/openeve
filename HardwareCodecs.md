## Encoder ##
  * libOmxVidEnc.so

## Decoders ##
  * libOmxH264Dec.so : H264, H263
  * libOmxMpeg4Dec.so
  * libOmxWmvDec.so


## Software codecs ##
libstagefright support the following encoding/decoding codecs
  * AVC Codec (H264/H263)
  * MPEG4 Codec
  * MP3 Codec

## Packet Video OpenCore ##
the old opencore software codecs used by Froyo is no longer supported by Gingerbread. it is not used by gingerbread anymore.

but it is turned out that it have been imported into the libstagefright and now become a built-in feature of the GingerBread.

http://android.git.kernel.org/?p=platform/external/opencore.git;a=tree;f=codecs_v2/omx

https://www.codeaurora.org/gitweb/quic/la/?p=platform/frameworks/base.git;a=tree;f=media/libstagefright/codecs;hb=gingerbread