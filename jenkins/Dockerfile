FROM jenkins/jenkins
USER root
RUN apt-get update && apt-get install wget
RUN wget --no-verbose -O /tmp/apache-maven-3.9.6-bin.tar.gz https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz
RUN tar xzf /tmp/apache-maven-3.9.6-bin.tar.gz -C /opt/ 
RUN ln -s  /opt/apache-maven-3.9.6 /opt/maven 
RUN ln -s /opt/maven/bin/mvn /usr/local/bin 
RUN rm /tmp/apache-maven-3.9.6-bin.tar.gz 
RUN chown jenkins:jenkins /opt/maven;

ENV MAVEN_HOME=/opt/mvn

USER jenkins