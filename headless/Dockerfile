FROM debian:sid AS builder

RUN  apt-get update \
     && apt-get install -y wget unzip \
     && rm -rf /var/lib/apt/lists/* \
     && wget https://downloads.tuxfamily.org/godotengine/3.2.2/Godot_v3.2.2-stable_linux_headless.64.zip \
     && unzip Godot_v3.2.2-stable_linux_headless.64.zip \
     && rm Godot_v3.2.2-stable_linux_headless.64.zip \
     && mv Godot_v3.2.2-stable_linux_headless.64 godot

FROM debian:sid-slim

COPY --from=builder /godot .
