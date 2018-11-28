# Ubuntu Server Setup

Documentation explains you how to setup a Ubuntu server step by step with Apache, php, mysql etc.

## Installin process

### Pre-Requisites

    $ sudo apt-get update 
    
    $ sudo apt-get upgrade
    
### Check php version if available

    $ php -v

    $ sudo apt cache search php
    
### Add php repository and update packages

    $ sudo apt-add-repository ppa:ondrej/php

    $ sudo apt-get update
    
### Install php and esential packages
    
    $ sudo apt-get install apache2 libapache2-mod-php7.2 php7.2 php7.2-xml php7.2-gd php7.2-opcache php7.2-cli php7.2-fpm php7.2-mbstring php7.2-mysql php7.1-mcrypt php7.2-curl php7.2-xmlrpc php7.2-soap php7.2-zip

### Install mysql and securing it

    $ sudo apt-get install mysql-server
    
    $ mysql_secure_installation
    
### Install Git and more essential packages

    $ sudo apt-get install git curl wget zip unzip
    
### Install composer

    $ curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
    
    
### Update php.ini for secuirity reasons

    memory_limit = 256M
    upload_max_filesize = 64M
    cgi.fix_pathinfo=0
    
## Configure Apache2

### Create new configuratuin file

    $ sudo nano /etc/apache2/sites-available/laravel.conf
    
### Update configuratuon file (laravel.conf)

    <VirtualHost *:80>   
        ServerAdmin admin@example.com
        ServerName example.com
        ServerAlias www.example.com
        DocumentRoot /var/www/example.com/public_html
    
        <Directory /var/www/example.com/public_html>
            Options +FollowSymlinks
            AllowOverride All
            Require all granted
        </Directory>
    
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>

To edit configuration file

    $ vim /path/to/file
    
### Enable The laravel.conf And Rewrite Module
    
    $ sudo a2dissite 000-default.conf
    
    $ sudo a2ensite laravel.conf
    
    $ sudo a2enmod rewrite
    
### Restart Apache
    
    $ sudo systemctl restart apache2.service
    
To enable or disable modules

    $ sudo a2enmod example_mod // enable
    $ sudo a2dismod example_mod // disable
    
## Create directory for a project

### Set permissions

    $ sudo chmod -R 755 /path/to/project/directory
    


    


    
    
    
    
    
    
    
    
    
    
    
    
    
    
    