FROM jenkins/jenkins:windowsservercore-2019
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
COPY jcasc/plugins.txt C:/ProgramData/jenkins/plugins.txt
RUN powershell.exe C:/ProgramData/jenkins/jenkins-plugin-cli.ps1 -f C:/ProgramData/jenkins/plugins.txt
