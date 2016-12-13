FROM jenkinsci/jnlp-slave
MAINTAINER Naveen <naveensrinivasan@yahoo.com>

USER root
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -
RUN apt-get install -y nodejs
RUN npm install -g gulp

ENV CLOUDSDK_CORE_DISABLE_PROMPTS 1
ENV PATH /opt/google-cloud-sdk/bin:$PATH


RUN curl https://sdk.cloud.google.com | bash && mv google-cloud-sdk /opt \
    && gcloud components install kubectl

RUN wget -O /usr/bin/docker --no-check-certificate https://get.docker.com/builds/Linux/x86_64/docker-1.10.3 \
&& chmod a+x /usr/bin/docker

RUN curl -fsSL  http://storage.googleapis.com/kubernetes-helm/helm-v2.0.2-linux-amd64.tar.gz -o helm.tar.gz && tar -C /usr/local/ -xzf helm.tar.gz
RUN apt-get install curl

WORKDIR /usr/local
COPY ./sonar sonar
ENV PATH /usr/local/sonar/bin:$PATH
RUN apt-get install zip unzip -y
