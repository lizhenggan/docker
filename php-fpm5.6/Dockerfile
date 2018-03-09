FROM php:5.6-fpm
RUN apt-get update && apt-get install -y libpng-dev vim supervisor

RUN	docker-php-ext-install mysqli mysql pdo_mysql gd pcntl \

	&& pecl install redis \
    && docker-php-ext-enable redis \

	# 用完包管理器后安排打扫卫生可以显著的减少镜像大小
    && apt-get clean \
    && apt-get autoclean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* 



