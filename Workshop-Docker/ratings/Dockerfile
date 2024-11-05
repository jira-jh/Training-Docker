FROM node:21.6-slim

#hadolint ignore=DL3008
RUN apt-get update \
    && apt-get install curl --no-install-recommends -y \
    && rm -rf /var/lib/apt/lists/*

ARG service_version
ENV SERVICE_VERSION=${service_version:-v1}

COPY src/package.json /opt/microservices/
COPY src/ratings.js /opt/microservices/
WORKDIR /opt/microservices
RUN npm install
RUN npm install node
CMD ["npm","start"]

USER 1000
