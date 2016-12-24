# Keystone

This document refers to the vb-site-cms implementation.

## Documentation

[Keystone documentation](http://keystonejs.com/docs/)

## Prerequisites

* nodejs + npm
* mongodb
* yo

## optional requirements

* [PM2](http://pm2.keymetrics.io/)
* [Apache](https://httpd.apache.org/) or [Nginx](https://www.nginx.com/)

## Install & setup

### Keystone configuration

### NginX configuration

```
server {
    server_name myKeystoneApp.com;
    listen 80;

    access_log /var/log/nginx/myKeystoneApp-access.log;
    error_log /var/log/nginx/myKeystoneApp-error.log;

    location / {
        proxy_set_header   X-Real-IP $remote_addr;
        proxy_set_header   Host      $http_host;
        proxy_pass         http://127.0.0.1:3000;
    }
}
```
* To enable a site, run the following command:
`ln -s /etc/nginx/sites-available/www.example.org.conf /etc/nginx/sites-enabled/`
* restart: `sudo service nginx restart`

## Run

1. start mongodb: `sudo service mongod start`
1. start keystone: `pm2 start keystone.js`




More documentation: 

* [Keystone documentation](http://keystonejs.com/docs/)
* [Keystone wiki](https://github.com/keystonejs/keystone/wiki)
* [Practical Keystone.js](https://leanpub.com/keystonejs/read). It contains an interesting paragraph about debugging in visual code.

