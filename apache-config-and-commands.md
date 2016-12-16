# Apache configuration and commands

## Setup a site

Apache dir: **/etc/apache2/**

1. Create a new virtual host configuratie in etc/apache2/sites-available, e.g. *001-icws.nl.conf* with the cp command.
2. Enable the site `$sudo a2ensite icws.nl`
3. Restart apache `service apache2 reload` OR `$sudo systemctl restart apache2.service`

To disable a site run `$sudo a2dissite [site-file]` 

## enable a site

* enable a site: `$sudo a2ensite [site-file]`
* disable a site: `$sudo a2dissite [site-file]`
* enable an apache2 module: `$sudo a2enmod [module]`
* disable an apache2 module: `$sudo a2dismod [module]`

## start/stop server

* Reload the server:`$sudo  /etc/init.d/apache2 force-reload`
OR `$sudo service apache2 reload`