FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
    curl\
    sudo\
    wget

RUN curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

RUN apt install -y git

RUN apt-get update && apt-get install -y \
    nodejs

RUN npm install -g serve

RUN git clone https://github.com/americans007/react-app

WORKDIR react-app

RUN npm install

RUN npm run build

EXPOSE 3456

ENTRYPOINT ["serve", "-s", "build", "-l", "3456", "&"]
