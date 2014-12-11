FROM phusion/baseimage:0.9.15
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

RUN apt-get update

RUN apt-get install curl -y

RUN \curl -L https://get.rvm.io | bash -s stable

RUN /bin/bash -c "source /usr/local/rvm/scripts/rvm
                  && rvm requirements"
