FROM jenkins/jenkins:lts
USER root
RUN apt-get update && apt-get install -y --no-install-recommends curl ca-certificates \
 && ARCH=$(uname -m) \
 && curl -fsSL https://download.docker.com/linux/static/stable/${ARCH}/docker-27.3.1.tgz | tar -xz -C /tmp \
 && mv /tmp/docker/docker /usr/local/bin/docker && rm -rf /tmp/docker /var/lib/apt/lists/*
USER jenkins
RUN jenkins-plugin-cli --plugins workflow-aggregator
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
