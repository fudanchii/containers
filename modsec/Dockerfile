FROM base
MAINTAINER Nurahmadie <nurahmadie@gmail.com>

RUN apt-get install -y software-properties-common


RUN apt-get update
RUN apt-get upgrade

RUN apt-get install -y apache2-threaded-dev git-core build-essential libpcre3-dev libxml2-dev libxslt-dev wget autotools-dev && apt-get clean

RUN apt-get install -y libtool automake autoconf m4 && apt-get clean

RUN apt-get install -y libcurl4-openssl-dev lua5.2 liblua5.2-dev openssh-server

RUN cd /root; wget http://nginx.org/download/nginx-1.5.5.tar.gz; wget http://www.openssl.org/source/openssl-1.0.1e.tar.gz

RUN cd /root; mkdir -p stubs; cd stubs; git clone https://github.com/SpiderLabs/ModSecurity

