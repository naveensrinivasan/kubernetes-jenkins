FROM jenkinsci/jnlp-slave
MAINTAINER Naveen <naveensrinivasan@yahoo.com>

ENV CLOUDSDK_CORE_DISABLE_PROMPTS 1
ENV PATH /opt/google-cloud-sdk/bin:$PATH

USER root

RUN curl https://sdk.cloud.google.com | bash && mv google-cloud-sdk /opt
RUN gcloud components install kubectl

RUN wget -O /usr/bin/docker --no-check-certificate https://get.docker.com/builds/Linux/x86_64/docker-1.10.3
RUN chmod a+x /usr/bin/docker

RUN curl -fsSL http://storage.googleapis.com/kubernetes-helm/helm-v2.0.0-alpha.5-linux-amd64.tar.gz -o helm.tar.gz && tar -C /usr/local/ -xzf helm.tar.gz 

WORKDIR /usr/local
RUN wget http://repo1.maven.org/maven2/org/codehaus/sonar/runner/sonar-runner-dist/2.4/sonar-runner-dist-2.4.zip && \
    unzip sonar-runner-dist-2.4.zip && \
    rm sonar-runner-dist-2.4.zip
ENV PATH /usr/local/sonar-runner-2.4/bin:$PATH
