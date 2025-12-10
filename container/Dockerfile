FROM debian:trixie

RUN apt-get update && \
    apt-get install -y \
            autoconf \
            automake \
            autotools-dev \
            bc \
            bison \
            build-essential \
            cpio \
            curl \
            device-tree-compiler \
            flex \
            gawk \
            git \
            gperf \
            libexpat-dev \
            libgmp-dev \
            libmpc-dev \
            libmpfr-dev \
            libtool \
            libusb-1.0-0-dev \
            patchutils \
            pkg-config \
            python3 \
            rsync \
            texinfo \
            unzip \
            wget \
            zlib1g-dev \
            && \
    apt-get clean ; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

