FROM ubuntu:16.10
RUN apt-get update && apt-get install -yq build-essential
RUN apt-get update && apt-get install -yq cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
RUN apt-get update && apt-get install -yq python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

RUN git clone https://github.com/Itseez/opencv.git /opt/opencv
RUN git clone https://github.com/Itseez/opencv_contrib.git /opt/opencv_contrib

