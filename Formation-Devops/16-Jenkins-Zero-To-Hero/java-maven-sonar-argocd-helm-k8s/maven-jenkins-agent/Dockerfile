# Base Maven + Java 17
FROM maven:3.9.6-eclipse-temurin-17

USER root

RUN apt-get update && \
    apt-get install -y curl git unzip && \
    curl -fsSL https://download.docker.com/linux/static/stable/x86_64/docker-29.0.3.tgz \
    | tar xz --strip-components=1 -C /usr/local/bin docker/docker

# Optionnel : inclure kubectl / helm plus tard
# RUN curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
# RUN chmod +x kubectl && mv kubectl /usr/local/bin/

WORKDIR /home/jenkins

# Garde le conteneur vivant
ENTRYPOINT ["tail", "-f", "/dev/null"]
