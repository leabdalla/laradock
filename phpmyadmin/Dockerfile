FROM phpmyadmin/phpmyadmin

LABEL maintainer="Bo-Yi Wu <appleboy.tw@gmail.com>"

# Add volume for sessions to allow session persistence
VOLUME /sessions

RUN echo '' >> /usr/local/etc/php/conf.d/phpmyadmin-misc.ini \
 && echo 'memory_limit = 6G' >> /usr/local/etc/php/conf.d/phpmyadmin-misc.ini \
 && echo 'post_max_size = 6G' >> /usr/local/etc/php/conf.d/phpmyadmin-misc.ini \
 && echo 'upload_max_filesize = 6G' >> /usr/local/etc/php/conf.d/phpmyadmin-misc.ini \
 && echo 'max_execution_time = 6000' >> /usr/local/etc/php/conf.d/phpmyadmin-misc.ini

# We expose phpMyAdmin on port 80
EXPOSE 80
