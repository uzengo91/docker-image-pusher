FROM eclipse-temurin:8u432-b06-jdk-focal
MAINTAINER luhao
LABEL description="AITelevision"

ENV ffmpeg_version_file=ffmpeg-n5.1-latest-linux64-lgpl-5.1.tar.xz
ENV ffmpeg_version=ffmpeg-n5.1-latest-linux64-lgpl-5.1
RUN apt update && apt install -y xz-utils libgdiplus curl tar && apt clean
RUN curl -O -L "https://github.com/BtbN/FFmpeg-Builds/releases/download/latest/${ffmpeg_version_file}" && tar -xvf ${ffmpeg_version_file} && cp ${ffmpeg_version}/bin/* /usr/local/bin/ && rm -rf ${ffmpeg_version_file} ${ffmpeg_version}
RUN ffmpeg -version
