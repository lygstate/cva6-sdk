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
            file \
            flex \
            gawk \
            git \
            gperf \
            libelf-dev \
            libexpat-dev \
            libgmp-dev \
            libgnutls28-dev \
            libmpc-dev \
            libmpfr-dev \
            libncurses5-dev \
            libssl-dev \
            libtool \
            libusb-1.0-0-dev \
            locales \
            patchutils \
            pkg-config \
            python3 \
            rsync \
            texinfo \
            universal-ctags \
            unzip \
            wget \
            xz-utils \
            zlib1g-dev \
            && \
    apt-get clean ; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN groupadd --gid 1000 lygstate && useradd -u 1000 -g 1000 lygstate
RUN mkdir -p /home/lygstate && chown -R lygstate:lygstate /home/lygstate
RUN echo "LC_ALL=en_US.UTF-8" >> /etc/environment && \
    echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen && \
    echo "LANG=en_US.UTF-8" > /etc/locale.conf && \
    locale-gen en_US.UTF-8
USER lygstate
ENV LC_ALL="en_US.UTF-8"
ENV LANG="en_US.UTF-8"
