FROM jenkins/jenkins:windowsservercore-2019
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
ENV CASC_JENKINS_CONFIG C:/ProgramData/jenkins/jenkinshome/casc.yaml
ENV GitVersion_EscapedBranchName ${GitVersion_EscapedBranchName}
ENV RUNNER_OS_TOLOWER ${RUNNER_OS_TOLOWER}
COPY jcasc/plugins.txt C:/ProgramData/jenkins/plugins.txt
RUN powershell.exe C:/ProgramData/jenkins/jenkins-plugin-cli.ps1 -f C:/ProgramData/jenkins/plugins.txt
COPY jcasc/casc.yaml C:/ProgramData/jenkins/jenkinshome/casc.yaml
