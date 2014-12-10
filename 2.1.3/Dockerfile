FROM phusion/baseimage:0.9.9

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh

CMD ["/sbin/my_init"]

ENV RUBY_VERSION 2.1.3

RUN apt-get update

RUN apt-get install python-software-properties
    && apt-add-repository ppa:brightbox/ruby-ng
    && apt-get update

RUN sudo apt-get install ruby rubygems ruby-switch

RUN ruby-switch --set ruby$RUBY_VERSION

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
