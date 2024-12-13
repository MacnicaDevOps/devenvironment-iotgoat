FROM ubuntu:20.04
RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

RUN apt-get update && apt-get install -y sudo
RUN apt-get install -y build-essential
RUN apt-get install -y  clang
RUN apt-get install -y  flex
RUN apt-get install -y  bison
RUN apt-get install -y  g++
RUN apt-get install -y  gawk 
RUN apt-get install -y gcc-multilib
RUN apt-get install -y  g++-multilib
RUN apt-get install -y  gettext
RUN apt-get install -y  git
RUN apt-get install -y  libncurses5-dev
RUN apt-get install -y  libssl-dev 
RUN apt-get install -y python3
RUN apt-get install -y  python3-setuptools
RUN apt-get install -y  rsync
RUN apt-get install -y  swig
RUN apt-get install -y  unzip
RUN apt-get install -y  zlib1g-dev
RUN apt-get install -y  file
RUN apt-get install -y  wget
ARG USERNAME=demo
ARG GROUPNAME=demo
ARG PASSWORD=Macnica123
ARG UID=1000
ARG GID=1000
RUN groupadd -g $GID $GROUPNAME && \
    useradd -m -s /bin/bash -u $UID -g $GID -G sudo $USERNAME && \
    echo $USERNAME:$PASSWORD | chpasswd && \
    echo "$USERNAME   ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER $USERNAME
WORKDIR /home/$USERNAME/
