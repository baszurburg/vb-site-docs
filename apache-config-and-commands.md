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

* Start: ``

* Stop: 

* Reload the server:`$sudo  /etc/init.d/apache2 force-reload`
OR `$sudo service apache2 reload`

+----------------------------------------+----------------------------------------+
| Apache2 Service Commands               | Apache2 Important Files                |
+----------------------------------------+----------------------------------------+
| Starting Apache2                       | Apach2 Syntax check                    |
| $ sudo /etc/init.d/apache2 start       | $ apachectl configtest                 |
| $ sudo service apache2 start           | $ apachectl -t                         |
| $ sudo apachectl -k start              |                                        |
+----------------------------------------+----------------------------------------+
| Restarting Apache2                     | Apache2 Web root                       |
| $ sudo /etc/init.d/apache2 restart     | $ /var/www/html - default              |
| $ sudo service apache2 restart         | $ /var/www/ - New domain location      |
| $ sudo apachectl -k restart            |                                        |
+----------------------------------------+----------------------------------------+
| Stopping Apache2                       | Enable / Disable Virtual Hosts         |
| $ sudo /etc/init.d/apache2 stop        | $ sudo a2ensite xxxx.conf              |
| $ sudo service apache2 stop            | $ sudo a2dissite xxxx.conf             |
| $ sudo apachectl -k stop               |                                        |
+----------------------------------------+----------------------------------------+
| Status Apache2                         | Loaded apache2 Modules                 |
| $ sudo /etc/init.d/apache2 status      | $ apachectl -M                         |
| $ sudo service apache2 status          | $ apache2ctl -M                        |
+----------------------------------------+----------------------------------------+
| Reload Apache                          | Apache2 Config file's                  |
| $ sudo /etc/init.d/apache2 reload      | $ /etc/apache2/apache2.conf            |
| $ sudo service apache2 reload          | $ /etc/apache2/ports.conf              |
| $ sudo apachectl -k reload             | $ /etc/apache2/sites-available/xxx.conf|
+----------------------------------------+----------------------------------------+
| Apache2 Graceful                       | Available apache2 Modules              |
| $ sudo apachectl -k graceful           | $ /usr/lib/apache2/modules/            |
| $ sudo apachectl -k graceful-stop      |                                        |
|                                        +----------------------------------------+
|                                        | Apache2 log file's                     |
|                                        | $ /var/log/apache2/error.log           |
|                                        | $ /var/log/apache2/access.log          |
+----------------------------------------+----------------------------------------+
