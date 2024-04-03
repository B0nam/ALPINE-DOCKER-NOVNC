FROM alpine:edge

# INSTALL DEPENDENCIES
RUN apk add \
    bash \
    fluxbox \
    git \
    net-tools \
    novnc \
    supervisor \
    x11vnc \
    xterm \
    xvfb \
    xorg-server

# ENVIROMENT TABLES
ENV \
    HOME=/root \
    LANG=pt_BR.UTF-8 \
    LANGUAGE=pt_BR.UTF-8 \
    LC_ALL=C.UTF-8 \
    DISPLAY=:0.0 \
    DISPLAY_WIDTH=1024 \
    DISPLAY_HEIGHT=768 \
    X11_PASSWORD=Abacate123@ \
    RUN_XTERM=yes \
    RUN_FLUXBOX=yes

COPY . /app

CMD ["/usr/bin/supervisord", "-c", "/app/supervisord.conf"]
EXPOSE 6080