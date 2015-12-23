FROM centos:centos7
MAINTAINER krisbuytaert  "kris@inuits.eu"


RUN yum -y update
RUN yum -y install openssh-server which

RUN yum install -y passwd

RUN echo d0cker | passwd --stdin root

RUN chkconfig sshd on

RUN yum install -y epel-release ruby-devel gcc rsync postgresql-devel rpm-build make
RUN gem install fpm


# RUN sed -i -e '/pam_loginuid\.so/ d' /etc/pam.d/sshd

EXPOSE 22
CMD /sbin/init
