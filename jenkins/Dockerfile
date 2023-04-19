FROM jenkins/jenkins:2.361.3-jdk11
USER root
RUN apt-get update
RUN apt-get install -y python3 python3-pip
COPY --chown=jenkins:jenkins plugins.txt /usr/share/jenkins/ref/plugins.txt
USER jenkins
RUN jenkins-plugin-cli  --plugins -f /usr/share/jenkins/ref/plugins.txt
