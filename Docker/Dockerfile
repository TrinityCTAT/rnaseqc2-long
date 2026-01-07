# Dockerfile for RNASeQC2-long
FROM ubuntu:20.04
MAINTAINER bhaas

RUN apt-get update && apt-get install -y software-properties-common && \
    apt-get update && apt-get install -y \
        build-essential \
        cmake \
        git \
        python3 \
        python3-pip \
        libboost-filesystem-dev \
        libboost-regex-dev \
        libboost-system-dev \
        libbz2-dev \
        libcurl3-dev \
        liblzma-dev \
        libpthread-stubs0-dev \
        wget \
        zlib1g-dev \
    && rm -rf /var/lib/apt/lists/*




WORKDIR /usr/local/src
RUN git clone https://github.com/TrinityCTAT/rnaseqc2-long.git && \
      cd rnaseqc2-long && \
      make && \
      ln -sf /usr/local/src/rnaseqc2-long/rnaseqc2-long /usr/local/bin/rnaseqc2-long

