FROM ubuntu:18.10

COPY unpack_bam.pl /opt/

RUN mkdir -p /opt/common/CentOS_6-dev/picard/v2.13/

RUN apt-get update -y && apt-get install -y \
    libnss-sss \
    curl \
    less \
    vim  \
    wget \
    unzip \
    build-essential 

RUN apt-get update -y && apt-get install -y \
    bzip2 \
    libcurl4-openssl-dev \
    cpanminus \
    git

RUN apt-get update -y && apt-get install -y \
   && cd /tmp && wget https://github.com/broadinstitute/picard/releases/download/2.13/picard.jar \
   && mv /tmp/picard.jar /opt/common/CentOS_6-dev/picard/v2.13

RUN cpanm Pod::Usage && cpanm JSON::Parse
