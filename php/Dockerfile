FROM centos:7
LABEL author=ipple1986 email=ipple1986@gmail.com site=https://zhaozhiwen.net.cn

RUN yum install -y httpd  php php-mysql php-gd php-imap php-ldap php-odbc php-pear php-xml php-xmlrpc && \
yum clean all && echo "demo html" > /var/www/html/index.html && rm -rf /etc/httpd/conf.d/welcome.conf
EXPOSE 80
ENTRYPOINT ["apachectl","-D","FOREGROUND"]


