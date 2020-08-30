FROM centos
RUN yum install httpd -y
RUN yum install php -y
RUN yum install java -y
RUN yum install openssh-server -y
RUN /usr/sbin/sshd -D &
RUN ssh-keygen -A
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN mkdir /root/.kube /root/jenkins
RUN mv ./kubectl /usr/local/bin/kubectl
COPY * /root/
RUN mv /root/info.yml /root/.kube/config
COPY index.html /var/www/html/
EXPOSE 80
CMD /usr/sbin/httpd -DFOREGROUND
