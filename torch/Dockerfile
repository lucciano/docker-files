FROM ubuntu:16.10

RUN apt-get update && apt-get install git sudo build-essential cmake -yq

RUN git clone https://github.com/torch/distro.git /opt/torch --recursive
RUN cd /opt/torch; bash install-deps; ./install.sh
