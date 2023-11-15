FROM php:8.2-fpm

RUN apt-get update

# This library required by xdiff extension.
WORKDIR /usr/src
COPY libs/libxdiff-0.23.tar.gz ./libxdiff-0.23.tar.gz
RUN tar -xzf libxdiff-0.23.tar.gz && cd libxdiff-0.23 && ./configure && make && make install
WORKDIR /

RUN echo "Installing PHP extensions...\n" \
    \
#    && docker-php-ext-install bcmath \
#    && docker-php-ext-install calendar \
#    && docker-php-ext-install dba \
#    && docker-php-ext-install exif \
#    && docker-php-ext-install pcntl \
#    && docker-php-ext-install sysvshm \
#    && docker-php-ext-install shmop \
#    && docker-php-ext-install sockets \
#    && docker-php-ext-install gettext \
#    && docker-php-ext-install mysqli \
    \
#    && apt-get install libffi-dev -y && docker-php-ext-install ffi \
#    && apt-get install libgd-dev -y && docker-php-ext-install gd \
#    && apt-get install libicu-dev -y && docker-php-ext-install intl \
#    && apt-get install libbz2-dev -y && docker-php-ext-install bz2 \
#    && apt-get install libenchant-2-dev -y && docker-php-ext-install enchant \
#    && apt-get install libgmp-dev -y && docker-php-ext-install gmp \
#    && apt-get install libc-client-dev libkrb5-dev -y && docker-php-ext-configure imap --with-kerberos --with-imap-ssl && docker-php-ext-install imap \
#    && apt-get install libldap2-dev -y && docker-php-ext-install ldap \
#    && apt-get install libpq-dev -y && docker-php-ext-install pgsql \
#    && apt-get install libpspell-dev -y && docker-php-ext-install pspell \
#    && apt-get install libsnmp-dev -y && docker-php-ext-install snmp \
#    && apt-get install libxml2-dev -y && docker-php-ext-install soap \
#    && apt-get install libtidy-dev -y && docker-php-ext-install tidy \
#    && apt-get install libxslt-dev -y && docker-php-ext-install xsl \
#    && apt-get install libzip-dev -y && docker-php-ext-install zip \
    \
#    && pecl install apcu-5.1.22 && docker-php-ext-enable apcu \
#    && apt-get install libcmark-dev -y && pecl install cmark-1.2.0 && docker-php-ext-enable cmark \
#    && pecl install dbase-7.1.1 && docker-php-ext-enable dbase \
#    && pecl install dio-0.2.1 && docker-php-ext-enable dio \
#    && pecl install ds-1.4.0 && docker-php-ext-enable ds \
#    && pecl install eio-3.0.0RC4 && docker-php-ext-enable eio \
#    && pecl install ev-1.1.5 && docker-php-ext-enable ev \
    # !Important! The "event" extension requires the "sockets" extension.
#    && apt-get install libevent-dev libssl-dev -y && pecl install event-3.0.8 && docker-php-ext-enable event \
#    && apt-get install libfann-dev -y && pecl install fann-1.2.0RC2 && docker-php-ext-enable fann \
#    && apt-get install libgearman-dev libevent-dev uuid -y && pecl install gearman-2.1.0 && docker-php-ext-enable gearman \
#    && apt-get install libgraphicsmagick1-dev -y && pecl install gmagick-2.0.6RC1 && docker-php-ext-enable gmagick \
#    && apt-get install libgpgme-dev -y && pecl install gnupg-1.5.1 && docker-php-ext-enable gnupg \
#    && apt-get install libyaml-dev -y && pecl install yaml-2.2.2 && docker-php-ext-enable yaml \
#    && apt-get install libcurl4-openssl-dev -y && pecl install yar-2.3.2 && docker-php-ext-enable yar \
#    && apt-get install libyaz-dev -y && pecl install yaz-1.2.4 && docker-php-ext-enable yaz \
#    && pecl install sync-1.1.2 && docker-php-ext-enable sync \
#    && pecl install swoole-4.8.12 && docker-php-ext-enable swoole \
#    && pecl install svm-0.2.3 && docker-php-ext-enable svm \
#    && apt-get install libssl-dev -y && pecl install stomp-2.0.3 && docker-php-ext-enable stomp \
#    && pecl install yac-2.3.1 && docker-php-ext-enable yac \
#    && pecl install yaconf-1.1.2 && docker-php-ext-enable yaconf \
#    && pecl install yaf-3.3.5 && docker-php-ext-enable yaf \
#    && apt-get install libxml2-dev -y && pecl install xmlrpc-1.0.0RC3 && docker-php-ext-enable xmlrpc \
#    && apt-get install libxml2-dev -y && pecl install xmldiff-1.1.3 && docker-php-ext-enable xmldiff \
#    && apt-get install zlib1g-dev -y && pecl install xlswriter-1.5.2 && docker-php-ext-enable xlswriter \
#    && pecl install inotify-3.0.0 && docker-php-ext-enable inotify \
#    && pecl install igbinary-3.2.7 && docker-php-ext-enable igbinary \
#    && pecl install parle-0.8.3 && docker-php-ext-enable parle \
#    && pecl install xhprof-2.3.7 && docker-php-ext-enable xhprof \
    # !Important! xdiff extension requires a libxdiff library.
#    && pecl install xdiff-2.1.1 && docker-php-ext-enable xdiff \
#    && pecl install xattr-1.4.0 && docker-php-ext-enable xattr \
#    && apt-get install libvarnishapi-dev -y && pecl install varnish-1.2.6 && docker-php-ext-enable varnish \
#    && pecl install var_representation-0.1.2 && docker-php-ext-enable var_representation \
#    && pecl install uopz-7.1.1 && docker-php-ext-enable uopz \
#    && pecl install trader-0.5.1 && docker-php-ext-enable trader \
#    && apt-get install libssh2-1-dev -y && pecl install ssh2-1.4 && docker-php-ext-enable ssh2 \
#    && apt-get install libcurl4-openssl-dev -y && apt-get install libxml2-dev -y && pecl install solr-2.6.0 && docker-php-ext-enable solr \
#    && pecl install seaslog-2.2.0 && docker-php-ext-enable seaslog \
#    && pecl install scoutapm-1.9.1 && docker-php-ext-enable scoutapm \
#    && pecl install runkit7-4.0.0a6 && docker-php-ext-enable runkit7 \
#    && apt-get install librpm-dev -y && pecl install rpminfo-0.6.0 && docker-php-ext-enable rpminfo \
#    && apt-get install librrd-dev -y && pecl install rrd-2.0.3 && docker-php-ext-enable rrd \
#    && pecl install quickhash-1.1.1 && docker-php-ext-enable quickhash \
    # !Important! PS extension requires a GD extension.
#    && apt-get install pslib-dev -y && pecl install ps-1.4.4 && docker-php-ext-enable ps \
#    && apt-get install libpcre3-dev -y && pecl install oauth-2.0.7 && docker-php-ext-enable oauth \
#    && apt-get install libboost-dev protobuf-compiler -y && pecl install mysql_xdevapi-8.0.30 && docker-php-ext-enable mysql_xdevapi \
#    && apt-get install libmemcached-dev zlib1g-dev libssl-dev -y && pecl install memcached-3.2.0 && docker-php-ext-enable memcached \
#    && apt-get install zlib1g-dev -y && pecl install memcache-8.2 && docker-php-ext-enable memcache \
#    && apt-get install libmcrypt-dev -y && pecl install mcrypt-1.0.6 && docker-php-ext-enable mcrypt \
#    && pecl install mailparse-3.1.6 && docker-php-ext-enable mailparse \
#    && pecl install lzf-1.7.0 && docker-php-ext-enable lzf \
#    && apt-get install liblua5.1-0-dev -y && pecl install luasandbox-4.1.1 && docker-php-ext-enable luasandbox \
#    && pecl install redis-6.0.2 && docker-php-ext-enable redis \
#    && apt-get install unixodbc-dev -y && pecl install sqlsrv-5.11.1 && docker-php-ext-enable sqlsrv \
#    && apt-get install unixodbc-dev -y && pecl install pdo_sqlsrv-5.11.1 && docker-php-ext-enable pdo_sqlsrv \
#    && apt-get install libkrb5-dev -y && pecl install krb5-1.1.5 && docker-php-ext-enable krb5 \
#    && apt-get install libpam-dev -y && pecl install pam-2.2.5 && docker-php-ext-enable pam \
#    && pecl install timezonedb-2023.3 && docker-php-ext-enable timezonedb \
#    && pecl install openswoole-22.1.0 && docker-php-ext-enable openswoole \
#    && apt-get install librdkafka-dev -y && pecl install simple_kafka_client-0.1.4 && docker-php-ext-enable simple_kafka_client \
    \
    && echo "\nThe extensions are successfully installed."

# Set working directory
WORKDIR /var/www
