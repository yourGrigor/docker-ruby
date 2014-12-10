FROM phusion/baseimage:0.9.9

RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys D39DC0E3

RUN \curl -sSL https://get.rvm.io | bash -s stable --ruby

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
