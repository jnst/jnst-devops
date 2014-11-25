FROM centos:centos7

# Change timezone
RUN ln -sf /usr/share/zoneinfo/Japan /etc/localtime

# Install requirement
RUN yum update -y && yum install -y \
  java-1.7.0-openjdk.x86_64 \
  wget

# Install jenkins
RUN wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
RUN rpm --import http://pkg.jenkins-ci.org/redhat/jenkins-ci.org.key
RUN yum install -y jenkins

EXPOSE 8080

ENTRYPOINT ["java", "-Djava.awt.headless=true", "-DJENKINS_HOME=/var/lib/jenkins",  "-jar", "/usr/lib/jenkins/jenkins.war", "--logfile=/var/log/jenkins/jenkins.log", "--webroot=/var/cache/jenkins/war"]
