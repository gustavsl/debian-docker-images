ARG IMAGE_ARCH=arm32v7
ARG BASE_NAME=debian-wayland-base
FROM gustavsl/$BASE_NAME:bullseye

RUN apt-get -y update && apt-get install -y --no-install-recommends \
    apt-utils \
    && apt-mark hold dash && apt-get -y upgrade && apt-mark unhold dash \
    && apt-get clean && apt-get autoremove && rm -rf /var/lib/apt/lists/*

RUN apt-get -y update && apt-get install -y --no-install-recommends \
    qtwayland5 \
    qml-module-qtquick-controls2 \
    qml-module-qtquick-layouts \
    qml-module-qtquick2 \
    qtbase5-examples \
    && apt-get clean && apt-get autoremove && rm -rf /var/lib/apt/lists/*


ENV QT_QPA_PLATFORM="wayland"
