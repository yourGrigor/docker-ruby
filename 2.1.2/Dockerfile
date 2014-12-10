FROM yourgrigor/ruby:rvm

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh

ENV RUBY_MAJOR 2.1
ENV RUBY_VERSION 2.1.2

RUN apt-get -y update
  && apt-get -y install build-essential zlib1g-dev libssl-dev libreadline6-dev libyaml-dev
  && cd /tmp
  && wget http://ftp.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz
  && tar -xvzf ruby-$RUBY_VERSION.tar.gz
  && cd ruby-$RUBY_VERSION/
  && ./configure --prefix=/usr/local
  && make
  && make install

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
