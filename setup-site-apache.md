# How to setup a site on Apache 2

## References

* [http://httpd.apache.org/docs/current/]()
* [http/2](http://httpd.apache.org/docs/2.4/howto/http2.html)

## Locations

### Website sourcefiles
The source files for the website are located in **/var/www/** e.g. */var/www/example.com/public_html*

### Apache2

Apache dir: **/etc/apache2/**

1. Create a new virtual host configuratie in etc/apache2/sites-available, e.g. *001-icws.nl.conf* with the cp command.
2. Enable the site `$sudo a2ensite icws.nl`
3. Restart apache `service apache2 reload` OR `$sudo systemctl restart apache2.service`

To disable a site run `$sudo a2dissite [site-file]` 

### Mongo DB

See also the [mongodb.md](./mongodb.md) file 





More info:

[https://docs.mongodb.com/master/tutorial/install-mongodb-on-ubuntu/]()

[https://www.digitalocean.com/community/tutorials/how-to-configure-the-apache-web-server-on-an-ubuntu-or-debian-vps]()
