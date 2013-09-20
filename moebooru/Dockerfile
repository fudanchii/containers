FROM base
MAINTAINER Nurahmadie <nurahmadie@gmail.com>

RUN apt-get install -y software-properties-common

RUN apt-add-repository ppa:brightbox/ruby-ng-experimental
RUN add-apt-repository ppa:chris-lea/node.js

RUN apt-get update
RUN apt-get upgrade

RUN apt-get install -y ruby2.0 ruby2.0-dev ruby-switch rubygems postgresql-contrib postgresql libpq-dev libxml2-dev libxslt-dev mercurial jhead build-essential libgd2-noxpm-dev imagemagick nodejs git-core && apt-get clean

RUN mkdir -p /srv && cd /srv && git clone https://github.com/moebooru/moebooru

RUN ruby-switch --set ruby2.0

RUN gem install bundler

RUN cd /srv/moebooru && bundle install

