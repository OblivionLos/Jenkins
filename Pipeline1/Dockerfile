FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    openjdk-8-jdk \
    nginx \
    net-tools
 
COPY default.conf /etc/nginx/conf.d/default.conf

RUN adduser wideuser && usermod -aG sudo wideuser \
    adduser pepega && \
    echo "pepega ALL=(ALL) \
    NOPASSWD:/usr/sbin/service nginx start, \
    /usr/sbin/service nginx stop, \
    /usr/sbin/service nginx restart " \
    > /etc/sudoers.d/pepega
