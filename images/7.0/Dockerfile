FROM php:7.0.22
MAINTAINER Luis Mayta <@slovacus>

ENV BUILD_DEPS default-libmysqlclient-dev \
  libbz2-dev \
  libmemcached-dev \
  libsasl2-dev

ENV RUNTIME_DEPS curl \
  git-core \
  g++ \
  software-properties-common \
  libfreetype6-dev \
  libicu-dev \
  libjpeg-dev \
  libldap2-dev \
  libmcrypt-dev \
  libmemcachedutil2 \
  libpng-dev \
  libpq-dev \
  libzip-dev \
  libjpeg62-turbo-dev \
  libpng12-dev \
  zlib1g-dev

RUN echo \
  'deb ftp://ftp.us.debian.org/debian/ jessie main\n \
  deb ftp://ftp.us.debian.org/debian/ jessie-updates main\n \
  deb http://security.debian.org jessie/updates main\n' \
  > /etc/apt/sources.list \
  && apt update -y --fix-missing \
  && apt install -y $BUILD_DEPS $RUNTIME_DEPS \
# install php dependencies
  && docker-php-ext-install bcmath bz2 calendar iconv intl mbstring mcrypt mysqli opcache pdo_mysql pdo_pgsql pgsql soap zip \
  && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
  && docker-php-ext-install gd \
  && docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu/ \
  && docker-php-ext-configure intl \
  && docker-php-ext-install ldap \
  && docker-php-ext-install intl\
  && docker-php-ext-install exif \
  && pecl install memcached redis \
  && docker-php-ext-enable memcached.so redis.so \

  && pecl install xdebug \
  && docker-php-ext-enable xdebug \

  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
  && apt-get purge -y --auto-remove $BUILD_DEPS \
  && rm -r /var/lib/apt/lists/* \
  && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
  && ln -s $(composer config --global home) /root/composer
