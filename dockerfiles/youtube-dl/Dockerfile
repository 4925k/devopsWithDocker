
# specify image version for stability
FROM ubuntu:20.04

# set workdir
WORKDIR /mydir

# install curl and python3
RUN apt update
RUN apt install -y python3 
RUN apt install -y curl

# install youtube downloader
RUN curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp
RUN chmod a+rx /usr/local/bin/yt-dlp 

# mention the whole path to be safe
ENTRYPOINT ["/usr/local/bin/yt-dlp"]

