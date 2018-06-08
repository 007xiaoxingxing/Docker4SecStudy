#base image

FROM centos:latest

# MAINTAINER
MAINTAINER chanxing9@gmail.com

RUN yum -y install epel-release && yum update && yum -y install httpd && yum -y \
    install mariadb-server mariadb-client && yum -y install git\
    yum -y install vim && yum -y install curl && yum -y install php\
    yum -y install php-mysql && yum install supervisor -y
RUN rm -rf /var/www/html/*

RUN git clone https://github.com/Audi-1/sqli-labs.git "/var/www/html/"

ADD ./mysql.ini /etc/supervisord.d/mysql.ini
ADD ./httpd.ini /etc/supervisord.d/httpd.ini
CMD ["/usr/bin/supervisord", "-n"]
