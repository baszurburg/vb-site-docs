# NginX

## Install

`sudo apt-get install nginx`

## Locations

NginX dir: **/etc/nginx/**

## Configuration


### Enable/disable a site

To list all available virtualhosts, you can run the following command:

`ls /etc/nginx/sites-available`	

To enable a site, run the following command:

`ln -s /etc/nginx/sites-available/www.example.org.conf /etc/nginx/sites-enabled/`

## Useful commands

* start: `sudo service nginx start`
* stop: `sudo /etc/init.d/nginx stop`
* restart: `sudo service nginx restart`

## More resources

[https://www.rosehosting.com/blog/install-keystonejs-on-an-ubuntu-14-04/](https://www.rosehosting.com/blog/install-keystonejs-on-an-ubuntu-14-04/)

[How To Set Up a Node.js Application for Production on Ubuntu 16.04 with NginX and SSL](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-node-js-application-for-production-on-ubuntu-16-04)

[NGINX wiki](https://www.nginx.com/resources/wiki/)

[How To Set Up Nginx with HTTP/2 Support on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-with-http-2-support-on-ubuntu-16-04)

[Nginx Cheat Sheet](https://gist.github.com/carlessanagustin/9509d0d31414804da03b)

# http://wiki.nginx.org/Pitfalls
# http://wiki.nginx.org/QuickStart
# http://wiki.nginx.org/Configuration
