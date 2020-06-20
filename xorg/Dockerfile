FROM ubuntu:focal

RUN ln -fs /usr/share/zoneinfo/Asia/Kolkata /etc/localtime

RUN	apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
	alsa-utils libgl1-mesa-dri libgl1-mesa-glx xdg-utils libxcursor1 libxinerama1 libxrandr2 \
	libxtst6 libxrender1 libxi6 libxt6 libxtst6 libfreetype6 libice6 libsm6 \
	libev4 libstartup-notification0 libxaw7 inotify-tools tzdata \
    rxvt-unicode x11-utils xfonts-base xfonts-encodings xfonts-utils \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/* && rm -rf /var/cache/apt/*

RUN dpkg-reconfigure --frontend noninteractive tzdata
