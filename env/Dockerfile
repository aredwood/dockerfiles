# this is a test file I use across projects.
# i do not recommend using it if you're not me.
FROM debian:stretch-20200422

WORKDIR /tmp

RUN apt-get update

RUN apt-get install curl unzip -y

# Install Packer 1.5.6
RUN curl https://releases.hashicorp.com/packer/1.5.6/packer_1.5.6_linux_amd64.zip -o /tmp/packer.zip

RUN unzip /tmp/packer.zip

RUN mv /tmp/packer /usr/local/bin


