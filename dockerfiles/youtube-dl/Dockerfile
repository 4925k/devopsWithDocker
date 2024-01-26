
# specify image version for stability
FROM alpine:latest

# set workdir
WORKDIR /usr/videos

# install curl and python3
RUN apk add --no-cache curl python3 ca-certificates && \
    curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp && \
    chmod a+rx /usr/local/bin/yt-dlp && \
    apk del curl && \
    adduser -D appuser 

USER appuser

# mention the whole path to be safe
ENTRYPOINT ["/usr/local/bin/yt-dlp"]

