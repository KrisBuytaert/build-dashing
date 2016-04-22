FROM dashing/ruby21 

MAINTAINER krisbuytaert  "kris@inuits.eu"


RUN yum -y install nodejs
RUN /bin/bash -l -c "mkdir -p /opt/dashing/"
RUN /bin/bash -l -c "rvm use 2.1.8 && gem install bundle && gem install dashing && cd /opt/dashing/ && /usr/local/rvm/gems/ruby-2.1.8/bin/dashing new dashboard && cd /opt/dashing/dashboard &&  /usr/local/rvm/gems/ruby-2.1.8/bin/bundle install"

EXPOSE 3030


WORKDIR  /opt/dashing/dashboard

CMD /bin/bash -l -c "rvm use 2.1.8 && dashing start"
