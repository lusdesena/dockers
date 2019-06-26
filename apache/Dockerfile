FROM library/debian:stretch-slim
LABEL maintainer="alucena5@xtec.cat"

RUN apt-get -y update&& \
	apt-get -y install apache2 && \
	ln -sf /dev/stdout /var/log/apache2/access.log && \
	ln -sf /dev/stderr /var/log/apache2/error.log && \
	echo "ServerName Happy_Apache" > /etc/apache2/conf-enabled/serverName.conf  

COPY index.html /var/www/html/index.html
EXPOSE 80
CMD apachectl -D FOREGROUND

