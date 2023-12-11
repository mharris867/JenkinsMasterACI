FROM jenkins/jenkins:latest
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
ENV CASC_JENKINS_CONFIG /var/jenkins_home/casc.yaml
ENV GitVersion_EscapedBranchName ${GitVersion_EscapedBranchName}
ENV RUNNER_OS_TOLOWER ${RUNNER_OS_TOLOWER}
COPY --chown=jenkins:jenkins jcasc/plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt
COPY --chown=jenkins:jenkins jcasc/casc.yaml /usr/share/jenkins/ref/casc.yaml
