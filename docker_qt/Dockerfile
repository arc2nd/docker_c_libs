FROM ubuntu:18.04

RUN apt-get update 
#RUN apt-get -y install unzip wget libfontconfig1 build-essential mesa-common-dev libglu1-mesa-dev

#ENV QT_VERSION_A=5.9
#ENV QT_VERSION_B=5.9.4
#ENV QT_VERSION_SCRIPT=594
#RUN wget https://download.qt.io/archive/qt/${QT_VERSION_A}/${QT_VERSION_B}/qt-opensource-linux-x64-${QT_VERSION_B}.run
#RUN chmod +x qt-opensource-linux-x64-${QT_VERSION_B}.run 
#COPY qt-noninteractive.qs /qt-noninteractive.qs
#RUN ./qt-opensource-linux-x64-${QT_VERSION_B}.run --script 


# basic essentials
RUN apt-get -y install qt5-default libxcb-xinerama0-dev build-essential perl python git
# libxcb
RUN apt-get -y install '^libxcb.*-dev' libx11-xcb-dev libglu1-mesa-dev libxrender-dev libxi-dev
# Qt WebKit
RUN apt-get -y install flex bison gperf libicu-dev libxslt-dev ruby
# Qt Multimedia
# RUN apt-get -y install libasound2-dev libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev
# RUN apt-get -y install libasound2-dev libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev

COPY qt-noninteractive.qs /qt-noninteractive.qs
#RUN ./qt-opensource-linux-x64-${QT_VERSION_B}.run --script 
