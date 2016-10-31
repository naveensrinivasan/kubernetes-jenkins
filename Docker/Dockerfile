FROM jenkins:2.19.1
RUN /usr/local/bin/install-plugins.sh kubernetes:0.8 workflow-aggregator:2.4 credentials-binding:1.9 git:3.0.0 slack:2.0.1 slack-uploader:1.7 build-timeout:1.17.1 \
    && mkdir -p /usr/share/jenkins/ref/secrets/ \
    && echo "false" > /usr/share/jenkins/ref/secrets/slave-to-master-security-kill-switch
