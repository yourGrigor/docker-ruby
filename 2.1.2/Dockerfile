FROM yourgrigor/ruby:rvm

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh

RUN apt-get update

ENV RUBY_VERSION 2.1.2

RUN apt-get install ruby$RUBY_VERSION

ENV PATH /opt/rubies/ruby-$RUBY_VERSION/bin:$PATH

# Add options to gemrc
RUN echo "gem: --no-document" > ~/.gemrc

# Install bundler
RUN gem install bundler

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
