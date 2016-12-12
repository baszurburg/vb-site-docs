# Apache configuration and commands

## enable a site

> enable site
> 
> `$sudo a2ensite [site-file]`
>  
> disable site
> 
> `$sudo a2dissite [site-file]`
>  
> enable an apache2 module
> 
> `$sudo a2enmod [module]`
>  
> e.g. a2enmod php4 will create the correct symlinks in mods-enabled to allow the module to be used. In this example it will link both php4.conf and php4.load for the user
>  
> disable an apache2 module
> 
> `$sudo a2dismod [module]`
>  
> force reload the server:
> `$sudo  /etc/init.d/apache2 force-reload`
> OR
> `$sudo service apache2 reload`