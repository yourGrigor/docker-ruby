FROM phusion/baseimage:0.9.15

ENV HOME /root

CMD ["/sbin/my_init"]

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

ENV PATH /opt/rubies/ruby-2.1.2/bin:$PATH

RUN echo "gem: --no-document" > ~/.gemrc && gem install bundler
