FROM yourgrigor/ruby:rvm

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh

RUN apt-get -y update
RUN apt-get -y install build-essential zlib1g-dev libssl-dev libreadline6-dev libyaml-dev
RUN cd /tmp
RUN wget http://ftp.ruby-lang.org/pub/ruby/2.1/ruby-2.1.5.tar.gz
RUN tar -xvzf ruby-2.1.5.tar.gz
RUN cd ruby-2.1.5/
RUN ./configure --prefix=/usr/local
RUN make
RUN make install

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
