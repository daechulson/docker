FROM ubuntu:latest
LABEL maintainer="sdc8111@gmail.com"
# Install PHP, and supplimentary programs. openssh-server, curl, and lynx-cur are for debugging the container.
# RUN apt-get update && apt-get -y upgrade && DEBIAN_FRONTEND=noninteractive apt-get -y install \
# RUN apt-get update && apt-get install -y --no-install-recommends apt-utils
ARG DEBIAN_FRONTEND=noninteractive

# 레파지토리 추가
RUN apt-get -y install software-properties-common
RUN add-apt-repository ppa:ondrej/php

# 기본패키지 추가
RUN apt-get update && apt-get install -y --no-install-recommends apt-utils
RUN apt-get -y upgrade && apt-get -y install \
    php7.0 \
    php7.0-mysql \
    curl \
    php7.0-gd \
    php7.0-curl \
    php7.0-mbstring \
    php7.0-xml \
    php-zip \
    unzip \
    git \
    vim \
	&& rm -rf /var/lib/apt/lists/*
