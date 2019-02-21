FROM opensuse/leap

RUN zypper --non-interactive --no-gpg-checks ref; \
	zypper --non-interactive in --recommends apache2;\
	zypper --non-interactive in --recommends php7 php7-mysql apache2-mod_php7; \
	zypper clean; 

RUN a2enmod php7

VOLUME /srv/www/htdocs

EXPOSE 80 443

CMD /usr/sbin/apache2ctl -DFOREGROUND
