
FROM jenkins/jenkins:2.176.1

# Distributed Builds plugins
RUN /usr/local/bin/install-plugins.sh ssh-slaves

#Install GIT
RUN /usr/local/bin/install-plugins.sh git

# UI
RUN /usr/local/bin/install-plugins.sh greenballs

RUN /usr/local/bin/install-plugins.sh simple-theme-plugin
# Scaling
RUN /usr/local/bin/install-plugins.sh \
  kubernetes \
  configuration-as-code \
  configuration-as-code-support \
  blueocean \
  job-dsl \
  cloudbees-folder \
  workflow-aggregator \
  pipeline-utility-steps \
  generic-webhook-trigger \
  git-changelog \
  violation-comments-to-gitlab

VOLUME /var/jenkins_home

USER jenkins
