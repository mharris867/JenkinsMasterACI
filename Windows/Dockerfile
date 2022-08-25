FROM jenkins/jenkins:windowsservercore-2019
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
COPY jcasc/plugins.txt C:/ProgramData/jenkins/plugins.txt
RUN jenkins-plugin-cli -f C:/ProgramData/jenkins/plugins.txt
