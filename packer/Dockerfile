# Debian, with Packer 1.5.6
FROM debian:stretch-20200422

RUN apt-get update

RUN apt-get install curl unzip -y

RUN curl https://releases.hashicorp.com/packer/1.5.6/packer_1.5.6_linux_amd64.zip -o /tmp/packer.zip

RUN unzip /tmp/packer.zip

RUN mv /tmp/packer /usr/local/bin


