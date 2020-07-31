FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    openjdk-8-jdk \
    nginx \
    net-tools
 
COPY default.conf /etc/nginx/conf.d/default.conf

ENTRYPOINT 

CMD passwd root
