
FROM ubuntu:20.04

# latest, v9.0.0, etc.
ARG FIREBASE_VERSION="latest"

RUN apt-get update && apt-get install curl -y

RUN curl -Lo /usr/local/firebase https://firebase.tools/bin/linux/${FIREBASE_VERSION}

