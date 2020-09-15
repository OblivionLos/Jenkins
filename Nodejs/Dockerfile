FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    npm \
    net-tools \
    git \
    wget

RUN apt-get update

RUN npm install -g serve

RUN git clone https://github.com/americans007/react-app

WORKDIR react-app

RUN npm install

RUN npm run build

ENTRYPOINT ["serve", "-s", "build", "-l", "3456"]
