FROM ubuntu:20.04 AS builder

# latest, v9.0.0, etc.
ARG FIREBASE_VERSION="latest"

RUN apt-get update && apt-get install curl -y

RUN curl -Lo /usr/local/bin/firebase https://firebase.tools/bin/linux/${FIREBASE_VERSION} \
    && chmod +rx /usr/local/bin/firebase


FROM ubuntu:20.04 AS runner

COPY --from=builder /usr/local/bin/firebase /usr/local/bin/firebase

