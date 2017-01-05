FROM sonarqube

MAINTAINER Izzet Mustafaiev "izzet@mustafaiev.com"


#Plugins


ENV JAVA_PLUGIN_VERSION 4.2
RUN curl -sLo $SONARQUBE_HOME/extensions/plugins/sonar-java-plugin-${JAVA_PLUGIN_VERSION}.jar \
	https://sonarsource.bintray.com/Distribution/sonar-java-plugin/sonar-java-plugin-${JAVA_PLUGIN_VERSION}.jar

ENV JS_PLUGIN_VERSION 2.15
RUN cd $SONARQUBE_HOME/extensions/plugins && \
	curl -sLo sonar-javascript-plugin-${JS_PLUGIN_VERSION}.jar \
    https://sonarsource.bintray.com/Distribution/sonar-javascript-plugin/sonar-javascript-plugin-${JS_PLUGIN_VERSION}.jar

ENV GENERIC_COVERAGE_PLUGIN_VERSION 1.1
RUN cd $SONARQUBE_HOME/extensions/plugins && \
	curl -sLo sonar-generic-coverage-plugin-${GENERIC_COVERAGE_PLUGIN_VERSION}.jar \
    http://downloads.sonarsource.com/plugins/org/codehaus/sonar-plugins/sonar-generic-coverage-plugin/${GENERIC_COVERAGE_PLUGIN_VERSION}/sonar-generic-coverage-plugin-${GENERIC_COVERAGE_PLUGIN_VERSION}.jar

ENV WEB_PLUGIN_VERSION 2.4
RUN cd $SONARQUBE_HOME/extensions/plugins && \
	curl -sLo sonar-web-plugin-${WEB_PLUGIN_VERSION}.jar \
    https://sonarsource.bintray.com/Distribution/sonar-web-plugin/sonar-web-plugin-${WEB_PLUGIN_VERSION}.jar

ENV XML_PLUGIN_VERSION 1.3
RUN cd $SONARQUBE_HOME/extensions/plugins && \
	curl -sLo sonar-xml-plugin-${XML_PLUGIN_VERSION}.jar \
    https://sonarsource.bintray.com/Distribution/sonar-xml-plugin/sonar-xml-plugin-${XML_PLUGIN_VERSION}.jar

ENV SONAR_GITHUB_PLUGIN 1.3
RUN cd $SONARQUBE_HOME/extensions/plugins && \
	curl -sLo sonar-github-plugin-${SONAR_GITHUB_PLUGIN}.jar \
    https://sonarsource.bintray.com/Distribution/sonar-github-plugin/sonar-github-plugin-${XML_PLUGIN_VERSION}.jar

ENV SONAR_GITHUB_AUTH_PLUGIN 1.3
RUN cd $SONARQUBE_HOME/extensions/plugins && \
	curl -sLo sonar-auth-github-plugin-${SONAR_GITHUB_AUTH_PLUGIN}.jar \
    https://sonarsource.bintray.com/Distribution/sonar-auth-github-plugin/sonar-auth-github-plugin-${XML_PLUGIN_VERSION}.jar
