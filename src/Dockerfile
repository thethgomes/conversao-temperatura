FROM ubuntu 
ARG NODE_MAJOR=20
RUN apt-get update && \
    apt-get install -y curl && \
    curl -fsSL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh && \
    bash nodesource_setup.sh && \
    apt-get install nodejs -y 
WORKDIR /app
COPY . .
RUN npm install
ENTRYPOINT [ "node",  "server.js" ]


