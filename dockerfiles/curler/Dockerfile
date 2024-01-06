# use a ubuntu 20:04 as base image
FROM ubuntu:20.04

# update dependencies and install curl
RUN apt -y update
RUN apt install -y curl

# set work dir
WORKDIR /usr/app/src

# copy curl script to container
COPY ./curler.sh .

# add executable permisson
RUN chmod +x curler.sh

# run the script when container starts
ENTRYPOINT [ "./curler.sh" ]