Docker ffmpeg
=============

This repository contains dockerfile for compiling needed version of ```ffmpeg```. Base image is *Centos 7*

Also includes pre-installed Java 8

Before compilation it installes all reaquired build tooles like *make*, *g++* and then removes it after compilation.

To adjust versions of the software to be installed just edit environment variables:

```
FFMPEG_VERSION  2.6.3
YASM_VERSION    1.3.0
OGG_VERSION     1.3.2
VORBIS_VERSION  1.3.4
LAME_VERSION    3.99.5
FAAC_VERSION    1.28
XVID_VERSION    1.3.3
FDKAAC_VERSION  0.1.3
```

Also refer to the documentation for [Logicify/centos7](https://github.com/Logicify/docker-centos7) image for more environment specific details.

To check which version of ffmpeg and related libraries is installed you may use: 
```
docker run --rm -it "logicify/ffmpeg" ffmpeg -buildconf
```
