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

# Install Python 3 & 2
RUN apt-get install python python3 -y

# Install Pip
RUN curl https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py
RUN python3 /tmp/get-pip.py

# Install yq
RUN pip install yq


# Set the workdir to /workspaces, compliant with GCP
# https://cloud.google.com/cloud-build/docs/create-custom-build-steps
RUN mkdir /workspace
WORKDIR /workspace