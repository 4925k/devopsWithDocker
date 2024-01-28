# image with java 8 installed
FROM amazoncorretto:8

# set work dir
WORKDIR /usr/src/app

# copy source code
COPY . .

# add executable permission
RUN chmod +x mvnw

# build the project
RUN ./mvnw package

# expose port 8080
EXPOSE 8080

# run the app
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]