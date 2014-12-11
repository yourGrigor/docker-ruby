FROM phusion/baseimage:0.9.15

RUN apt-get update

ENV RUBY_VERSION 2.1.2

RUN apt-get install -y wget curl \
    build-essential git git-core \
    zlib1g-dev libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev

RUN apt-get update

RUN cd /tmp &&\
  wget -O ruby-install-0.4.3.tar.gz https://github.com/postmodern/ruby-install/archive/v0.4.3.tar.gz &&\
  tar -xzvf ruby-install-0.4.3.tar.gz &&\
  cd ruby-install-0.4.3/ &&\
  make install

RUN ruby-install ruby $RUBY_VERSION

ENV PATH /opt/rubies/ruby-2.1.2/bin:$PATH

RUN echo "gem: --no-document" > ~/.gemrc

RUN gem install bundler
