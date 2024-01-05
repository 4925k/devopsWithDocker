# use alpine image
FROM alpine:3.19

# set work directory, all commands will be exectued from here
WORKDIR /usr/src/app

# copy script
COPY hello.sh .

# give execution permission to hello.sh
RUN chmod +x hello.sh

# execute commands with RUN 
RUN touch test_file.txt

# when docker starts, run the following command
CMD ./hello.sh