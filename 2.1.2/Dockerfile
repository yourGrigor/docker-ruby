FROM phusion/baseimage:0.9.15

ENV HOME /root

CMD ["/sbin/my_init"]

RUN apt-get update

RUN apt-get install ruby2.1.2

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
