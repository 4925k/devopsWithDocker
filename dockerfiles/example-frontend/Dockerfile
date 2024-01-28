FROM node:16-alpine3.18 as build

WORKDIR /app

COPY . ./app

RUN npm install && \
    npm run build
    
    
# smaller file
FROM node:alpine  
    
WORKDIR /app

COPY --from=build /usr/src/app/build /app/build

RUN npm install -g serve && \
    adduser -D fe-user

USER fe-user

EXPOSE 5001

CMD ["serve", "-s", "-l", "5001", "build"]

