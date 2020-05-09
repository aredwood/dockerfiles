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

# Install gcloud SDK
# https://cloud.google.com/sdk/docs#deb
RUN echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
RUN apt-get install apt-transport-https ca-certificates gnupg -y
RUN curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -
RUN apt-get update 
RUN apt-get install google-cloud-sdk -y

# Install Node.Js
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
RUN source ~/.bashrc
RUN nvm install 12.16.3

# Install Powershell
RUN curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add -
RUN sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-debian-stretch-prod stretch main" > /etc/apt/sources.list.d/microsoft.list'
RUN apt-get update
RUN apt-get install powershell -y

# Set the workdir to /workspaces, compliant with GCP
# https://cloud.google.com/cloud-build/docs/create-custom-build-steps
RUN mkdir /workspace
WORKDIR /workspace