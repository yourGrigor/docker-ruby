FROM phusion/baseimage:0.9.15

ENV HOME /root

CMD ["/sbin/my_init"]

RUN apt-get update

RUN apt-get install -y wget curl \
    build-essential git git-core \
    zlib1g-dev libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev

RUN apt-get update

RUN cd /tmp &&\
  wget -O ruby-install-0.4.3.tar.gz https://github.com/postmodern/ruby-install/archive/v0.4.3.tar.gz &&\
  tar -xzvf ruby-install-0.4.3.tar.gz &&\
  cd ruby-install-0.4.3/ &&\
  make install

RUN ruby-install ruby 2.1.3

ENV PATH /opt/rubies/ruby-2.1.3/bin:$PATH

RUN echo "gem: --no-document" > ~/.gemrc

RUN gem install bundler

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
