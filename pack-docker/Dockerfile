FROM debian:9-slim

RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/*
RUN wget -qO- https://github.com/buildpack/pack/releases/download/v0.1.0/pack-v0.1.0-linux.tgz | tar xvzf - -C /usr/local/bin && /usr/local/bin/pack set-default-builder cloudfoundry/cnb:cflinuxfs3

ENTRYPOINT ["/usr/local/bin/pack"]
