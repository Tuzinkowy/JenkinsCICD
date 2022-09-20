FROM jenkins/jenkins:latest-jdk17
USER root
RUN curl -fsSL https://get.docker.com | sh
RUN curl -fsSL https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
RUN chmod +x usr/local/bin/docker-compose
RUN usermod -aG docker jenkins
RUN groupmod -g 999 docker
USER jenkins