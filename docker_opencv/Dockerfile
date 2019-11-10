# FROM ubuntu:18.04
FROM library_qt
MAINTAINER James Parks

RUN apt-get update
# RUN apt-get -y upgrade

RUN apt-get -y install build-essential cmake git pkg-config libgtk-3-dev
RUN apt-get -y install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libxvidcore-dev libx264-dev
RUN apt-get -y install libjpeg-dev libpng-dev libtiff-dev gfortran openexr libatlas-base-dev
RUN apt-get -y install python3-pip python3-dev python3-numpy libtbb2 libtbb-dev libdc1394-22-dev

# RUN mkdir ~/opencv_build && cd ~/opencv_build
# RUN git clone https://github.com/opencv/opencv.git
# RUN git clone https://github.com/opencv/opencv_contrib.git

RUN pip3 install numpy

RUN apt-get install -y python-pip
RUN pip install --upgrade pip 


RUN cd ~/ &&\ 
    git clone https://github.com/opencv/opencv.git &&\ 
    git clone https://github.com/opencv/opencv_contrib.git &&\ 
    cd opencv && mkdir build && cd build && cmake  -DWITH_QT=ON -DWITH_OPENGL=ON -DFORCE_VTK=ON -DWITH_TBB=ON -DWITH_GDAL=ON -DWITH_XINE=ON -DBUILD_EXAMPLES=ON .. && \
    make -j4 && make install && ldconfig

# Set the appropriate link
RUN ln /dev/null /dev/raw1394

RUN cd ~/opencv

