FROM centos:7
LABEL author=ipple1986 email=ipple1986@gmail.com site=https://zhaozhiwen.net.cn

RUN yum install -y httpd php git wget && \
yum clean all && mkdir -p /home/git/repositories/ && cd /home/git/repositories/ && git init demo --bare && \
# ADD gitlist-0.5.0.tar.gz /opt
 cd /opt/ && wget -c https://s3.amazonaws.com/gitlist/gitlist-0.5.0.tar.gz && tar -xvf gitlist-0.5.0.tar.gz  && \
 cp -r /opt/gitlist/. /var/www/html && rm -rf /opt/gitlist*   && cd /var/www/html \
 && mkdir -p cache && chmod 777 cache && cp config.ini-example config.ini

COPY .htaccess /var/www/html/
COPY config.ini /var/www/html/
COPY httpd.conf /etc/httpd/conf/
COPY start.sh /etc/
RUN chmod u+x /etc/start.sh

EXPOSE 80 443
ENTRYPOINT ["/bin/bash","/etc/start.sh"]


