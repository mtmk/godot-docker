FROM debian:buster AS builder

RUN  apt-get update \
     && apt-get install -y wget unzip \
     && rm -rf /var/lib/apt/lists/* \
     && wget https://downloads.tuxfamily.org/godotengine/3.2.3/Godot_v3.2.3-stable_linux_headless.64.zip \
     && unzip Godot_v3.2.3-stable_linux_headless.64.zip \
     && rm Godot_v3.2.3-stable_linux_headless.64.zip \
     && mv Godot_v3.2.3-stable_linux_headless.64 godot

FROM debian:buster-slim

COPY --from=builder /godot .
