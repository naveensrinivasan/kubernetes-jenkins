FROM  openjdk:8
MAINTAINER Naveen <naveensrinivasan@yahoo.com>
USER root
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -
RUN apt-get install -y nodejs zip git
RUN npm install -g gulp
WORKDIR /usr/local
COPY ./github-release .
COPY ./sonar sonar
ENV PATH /usr/local/sonar/bin:$PATH
