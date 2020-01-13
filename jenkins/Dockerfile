
FROM jenkins/jenkins:2.176.1

RUN mkdir $JENKINS_HOME/casc_configs
COPY ../casc_configs/jenkins.yaml $JENKINS_HOME/casc_configs/jenkins.yaml
ENV CASC_JENKINS_CONFIG=$JENKINS_HOME/casc_configs

ENV JAVA_OPTS=-Djenkins.install.runSetupWizard=false

# Install plugins
RUN /usr/local/bin/install-plugins.sh \
  blueocean \
  cloudbees-folder \
  configuration-as-code \
  configuration-as-code-support \
  generic-webhook-trigger \
  git \
  git-changelog \
  greenballs \
  job-dsl \
  kubernetes \
  pipeline-utility-steps \
  simple-theme-plugin \
  ssh-slaves \
  violation-comments-to-gitlab \
  workflow-aggregator

VOLUME /var/jenkins_home

USER jenkins
