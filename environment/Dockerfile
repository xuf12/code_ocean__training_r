# hash:sha256:210966264f158ab8e27f664ee9496d88d2d4bd582376e6def003632eee7beb0f
FROM localhost:5000/codeocean/r-base:4.0.0-ubuntu18.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends software-properties-common \
    && apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys \
        0xAD2323F17326AE31401037733E05EBFF05441C52 \
    && add-apt-repository -y 'deb http://deb.codeocean.com/rstudio-server-bionic/ ubuntu main' \
    && apt-get purge -y --autoremove software-properties-common \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
        pandoc=1.19.2.4~dfsg-1build4 \
        rstudio-server=1.2.5033 \
    && rm -rf /var/lib/apt/lists/*
