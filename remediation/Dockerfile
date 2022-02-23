FROM quay.io/rdacosta/broken_httpd:latest

EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"

RUN sed -i -e 's/Listen 80/Listen 8080/g' /etc/httpd/conf/httpd.conf && \
    sed -i -e 's/#ServerName www.example.com:80/ServerName 0.0.0.0:8080/g' /etc/httpd/conf/httpd.conf && \
    chgrp -R 0 /var/log/httpd/ /var/run/httpd/ && \
    chmod -R g=u /var/log/httpd/ /var/run/httpd/



