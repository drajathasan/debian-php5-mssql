FROM debian:latest
MAINTAINER DrajatHasan
RUN apt-get update && apt-get install -y ca-certificates apt-transport-https wget gnupg2
RUN wget -q https://packages.sury.org/php/apt.gpg -O- | apt-key add -
RUN echo "deb https://packages.sury.org/php/ buster main" | tee /etc/apt/sources.list.d/php.list
RUN apt-get update && apt-get install -y apache2 php5.6 php5.6-sybase freetds-common libsybdb5
EXPOSE 80
CMD ["/usr/sbin/apache2ctl", "-DFOREGROUND"]
