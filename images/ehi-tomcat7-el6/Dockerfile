FROM registry.access.redhat.com/rhel6:latest

# This image provides an EHI Tomcat image

EXPOSE 8080 8443

COPY base.repo /etc/yum.repos.d/base.repo
COPY lxeng6.repo /etc/yum.repos.d/lxeng6.repo
COPY rpm-app.repo /etc/yum.repos.d/rpm-app.repo

#preprod-epel-6-x86_64
#preprod-rhel-x86_64-server-6
#preprod-rhel-x86_64-server-6-rhscl-1
#preprod-rhel-x86_64-server-6-thirdparty-oracle-java
#preprod-rhel-x86_64-server-optional-6
#preprod-rhel-x86_64-server-rh-common-6
#preprod-rhel6-lxeng
#preprod-rhel6-vmware-x86_64
#preprod-rhn-tools-rhel-x86_64-server-6

RUN yum install -y wget ehi-linux-engineering
RUN yum install -y ehi-tomcat7 ehi-tomcat7-ROOT && \
    yum clean all -y

USER tomcat

CMD sudo service tomcat start

