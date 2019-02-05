# PHP Downgrade to version 7.0 

    $ sudo add-apt-repository ppa:ondrej/php

    $ sudo apt-get update && apt-get upgrade

    $ sudo apt-get -y install php7.0 libapache2-mod-php7.0

    $ sudo service apache2 restart

    $ sudo apt-get -y install php7.0-mysql php7.0-curl php7.0-gd php7.0-intl php-pear php-imagick php7.0-imap php7.0-mcrypt php-memcache php7.0-pspell php7.0-recode php7.0-sqlite3 php7.0-tidy php7.0-xmlrpc php7.0-xsl php7.0-mbstring php-gettext php7.0-cli php7.0-common php7.0-fpm php7.0-cgi php7.0-dev

    $ sudo service apache2 restart

# Remove phpmyadmin warnings

    $ sudo apt-get dist-upgrade