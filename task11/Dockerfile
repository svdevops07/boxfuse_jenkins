FROM openjdk:8u151-stretch

# Install pacakges
RUN apt-get update

# Install ssh
RUN apt-get -y install openssh-client maven git

# Confugure ssh client
COPY id_rsa /root/.ssh/id_rsa
RUN chmod 600 /root/.ssh/id_rsa

# Install docker
RUN apt-get update
RUN apt-get install -y ca-certificates curl gnupg lsb-release
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
RUN apt-get update
RUN apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin


# Install docker 18.03
#RUN apt-get -y install apt-transport-https ca-certificates curl gnupg2 software-properties-common
#RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
#RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
#RUN apt-get update
#RUN apt-get -y install docker-ce=18.03.1~ce-0~debian
#RUN apt-get clean