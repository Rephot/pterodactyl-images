FROM        node:16-buster-slim

LABEL       author="Softwarenoob" maintainer="admin@softwarenoob.com"

RUN         apt update \
            && apt -y install ffmpeg iproute2 git sqlite3 python3 python tzdata ca-certificates dnsutils build-essential \
            && useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]
