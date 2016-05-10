FROM dashing/centos7
MAINTAINER krisbuytaert  "kris@inuits.eu"



RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
RUN curl -sSL https://get.rvm.io | bash -s stable --autolibs=enabled
RUN which fpm
RUN /usr/local/bin/fpm -s dir -t rpm -n rvm -v 1.26.11  /usr/local/rvm

