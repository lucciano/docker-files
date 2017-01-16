FROM debian:8.0

RUN apt-get update -yq && apt-get install wget php5-cli php5-intl -yq

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php -r "if (hash_file('SHA384', 'composer-setup.php') === '55d6ead61b29c7bdee5cccfb50076874187bd9f21f65d8991d46ec5cc90518f447387fb9f76ebae1fbbacf329e583e30') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
RUN php composer-setup.php --filename=composer --install-dir=/usr/local/bin
RUN php -r "unlink('composer-setup.php');"

RUN apt-get update -yq && apt-get install -yq git

RUN composer create-project -s dev jmather/symfony-sonata-distribution /opt/sonata-distribution
