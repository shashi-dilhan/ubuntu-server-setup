# Add SSL Certificate

    $ sudo add-apt-repository ppa:certbot/certbot

    $ sudo apt-get update

    $ sudo apt-get install python-certbot-apache

### Add domain

    $ sudo certbot --apache -d yourdomain.com -d www.yourdomain.com

### Check SSL certificate

    https://www.ssllabs.com/ssltest/