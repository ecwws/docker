FROM ubuntu:14.04
MAINTAINER Richard Li <richard+docker@wisewolfsolutions.com>

RUN apt-get -qq update
RUN apt-get -qqy install build-essential zlib1g-dev libssl-dev libreadline6-dev libyaml-dev curl
RUN apt-get -qqy install gcc-4.6

RUN locale-gen en_US.UTF-8
RUN update-locale LANG=en_US.UTF-8

RUN curl -L ftp://ftp.ruby-lang.org/pub/ruby/2.1/ruby-2.1.2.tar.bz2 | tar -xj -C /tmp
RUN cd /tmp/ruby-2.1.2 && CC=gcc-4.6 ./configure --disable-install-doc && make install clean

ENV LC_ALL en_US.UTF-8

RUN gem update --system
RUN rm -rf /tmp/ruby-2.1.1
