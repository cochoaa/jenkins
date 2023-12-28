#FROM jenkins/jenkins:2.426.2-jdk17
FROM jenkins/jenkins:2.437-jdk17
USER root
RUN apt-get update
RUN apt-get install -y lsb-release
RUN apt-get install vim -y
RUN apt-get install python3 -y
RUN apt-get install python3-pip -y
RUN apt-get install python3.11-venv -y 
COPY --chown=jenkins:jenkins plugins.txt /usr/share/jenkins/ref/plugins.txt
COPY requirements.txt .
RUN echo "$(pwd)"
#RUN python3 -m venv venv
#RUN /bin/bash -c "source venv/bin/activate &&   pip  install -r requirements.txt"
RUN pip3  install --break-system-packages -r requirements.txt

#RUN jenkins-plugin-cli  --plugins -f /usr/share/jenkins/ref/plugins.txt
USER jenkins
