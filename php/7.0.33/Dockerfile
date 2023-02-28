# 从官方基础版本构建
FROM zengweiliang/php7.0.33-fpm

RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak \
    && echo 'deb http://mirrors.163.com/debian/ stretch main non-free contrib' > /etc/apt/sources.list \
    && echo 'deb http://mirrors.163.com/debian-security stretch/updates main' >> /etc/apt/sources.list \
    && echo 'deb http://mirrors.163.com/debian/ stretch-updates main non-free contrib' >> /etc/apt/sources.list \
    && echo 'deb http://mirrors.163.com/debian/ stretch-backports main non-free contrib' >> /etc/apt/sources.list \
    && apt-get update \
    && pecl channel-update pecl.php.net \
	&& pecl install xdebug-2.7.2 \
    && docker-php-ext-enable xdebug \