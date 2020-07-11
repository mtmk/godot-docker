FROM debian

RUN  apt-get update && apt-get install -y wget unzip && rm -rf /var/lib/apt/lists/*

RUN wget https://downloads.tuxfamily.org/godotengine/3.2.2/Godot_v3.2.2-stable_linux_headless.64.zip

RUN unzip Godot_v3.2.2-stable_linux_headless.64.zip
RUN rm Godot_v3.2.2-stable_linux_headless.64.zip

RUN mv Godot_v3.2.2-stable_linux_headless.64 godot
