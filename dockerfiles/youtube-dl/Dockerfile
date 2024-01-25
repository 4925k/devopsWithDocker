
# specify image version for stability
FROM ubuntu:20.04

# set workdir
WORKDIR /usr/videos

# install curl and python3
RUN apt update && \
    apt install -y python3 && \
    apt install -y curl && \
    curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp && \
    chmod a+rx /usr/local/bin/yt-dlp && \
    useradd -m appuser && \
    chown appuser . && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* 

USER appuser

# mention the whole path to be safe
ENTRYPOINT ["/usr/local/bin/yt-dlp"]

