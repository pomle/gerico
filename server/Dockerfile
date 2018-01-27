FROM debian:wheezy

RUN apt-get update
RUN apt-get install -y curl nano lighttpd php5-cgi php5-mysql imagemagick

COPY lighttpd /etc/lighttpd

RUN lighttpd-enable-mod fastcgi auth

RUN ln -s /etc/lighttpd/sites

EXPOSE 80

VOLUME /data/www

CMD ["lighttpd", "-f", "/etc/lighttpd/lighttpd.conf", "-D"]
