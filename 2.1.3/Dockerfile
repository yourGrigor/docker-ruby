FROM ubuntu:14.04

RUN apt-get -y update
    && apt-get -y install build-essential zlib1g-dev libssl-dev libreadline6-dev libyaml-dev
    && cd /tmp
    && wget http://ftp.ruby-lang.org/pub/ruby/2.1/ruby-2.1.3.tar.gz
    && tar -xvzf ruby-2.1.3.tar.gz
    && cd ruby-2.1.3/
    && ./configure --prefix=/usr/local
    && make
    && make install
