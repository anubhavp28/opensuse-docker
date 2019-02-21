FROM opensuse/leap

RUN zypper --non-interactive refresh; \
    zypper --non-interactive in --recommends apache2; \
    zypper clean; 
    
ADD run-httpd.sh /run-httpd.sh
RUN chmod -v +x /run-httpd.sh

VOLUME /srv/www/htdocs

EXPOSE 80 443

CMD ["/run-httpd.sh"]
