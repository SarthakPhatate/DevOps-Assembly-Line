From centos:7

RUN yum install wget -y

RUN yum install net-tools -y

RUN wget -0 /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo

RUN rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key

RUN yum install jenkins java -y

RUN yum install git -y

RUN echo "jenkins ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

RUN yum install python3 -y

COPY mail.py ws/

EXPOSE 8080

CMD java -jar /usr/lib/jenkins/jenkins.war
