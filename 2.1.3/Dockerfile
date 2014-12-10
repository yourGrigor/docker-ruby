FROM yourgrigor/ruby:rvm

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh

CMD ["/sbin/my_init"]

RUN rvm 2.1.3

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
