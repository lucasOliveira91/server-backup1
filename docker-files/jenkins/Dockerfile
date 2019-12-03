from jenkins/jenkins:lts
USER root
RUN apt-get update
RUN apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg2 \
    software-properties-common -y
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
RUN apt-key fingerprint 0EBFCD88
RUN  add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"
RUN apt-get update
RUN apt-get install docker-ce docker-ce-cli containerd.io -y
RUN apt install maven -y
RUN touch /etc/apt/sources.list.d/java-13-debian.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys EA8CACC073C3DB2A
