FROM httpd:2.4

ARG DOCUMENTROOT="/usr/local/apache2/htdocs"

RUN rm -f ${DOCUMENTROOT}/index.html

RUN echo 'LoadModule proxy_module modules/mod_proxy.so' >> /usr/local/apache2/conf/httpd.conf
RUN echo 'LoadModule proxy_fcgi_module modules/mod_proxy_fcgi.so' >> /usr/local/apache2/conf/httpd.conf
RUN echo 'Include conf/extra/httpd-vhosts.conf' >> /usr/local/apache2/conf/httpd.conf

COPY conf /usr/local/apache2/conf/extra

EXPOSE 80