FROM ubuntu:latest
LABEL name="Marco Liao"
LABEL email="marco.w.liew@gmail.com"
ENV UBUNTU_HOME=/var/www/html/
RUN rm /bin/sh && ln -s /bin/bash /bin/sh
RUN apt-get update -y
ENV DEBIAN_FRONTEND noninteractive	
RUN apt-get -y install tzdata
RUN apt-get install apache2 -y
RUN chmod a+x /etc/apache2/apache2.conf
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf
WORKDIR UBUNTU_HOME
#COPY docker/source/index.html ${UBUNTU_HOME}
COPY source/index.html ${UBUNTU_HOME}
EXPOSE 80
CMD ["apachectl" , "-D","FOREGROUND"]
