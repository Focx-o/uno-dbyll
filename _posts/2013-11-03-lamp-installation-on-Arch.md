---
layout: post
title: Lamp Installation on Arch 
description: Linux, Apache, MySQL/MariaDB, PHP. In short LAMP, a complete Open Source solution for web-developer.
image: /assets/media/Lamp.jpg
categories: [linux]
tags: [Arch, lamp, setup, php, mariadb, appache, mysql ]

---
<img src="{{page.image}}" width="85%"/>
<br/>
<br/>
Linux, <a href="http://httpd.apache.org/">Apache</a>, MySQL/MariaDB, PHP: In short LAMP, a complete Open Source solution for web-developer. Apache Web Server,Often referred to as simply <a href="http://httpd.apache.org/">Apache</a>, a public-domain open source Web server developed by a loosely-knit group of programmers which runs roughly 50% of the servers in the world.
Here i show you the simple steps to install LAMP on your Arch System:

Install php,php-apache,apache and mariadb:
(note: use your favorite text editor, am using "gedit")

{% highlight ruby %}

$ sudo Pacman -S php-apache apache mariadb

{% endhighlight %}

Now configure apache:

{% highlight ruby %}

$ sudo gedit /etc/httpd/conf/httpd.conf 

#> comment the line .i.e. put a # before it.

LoadModule unique_id_module modules/mod_unique_id.so

#> restart apache

$ sudo systemctl restart httpd

{% endhighlight %}

then configure mariadb:

{% highlight ruby %}

$ sudo systemctl start mysqld
$ sudo mysql_secure_installation

#> press enter and then "yes" to all.

{% endhighlight %}

Lastly configure php and php-apache:

{% highlight ruby %}

$ sudo gedit /etc/httpd/conf/httpd.conf

#> add the following lines at the end of the files

LoadModule php5_module modules/libphp5.so 
AddHandler php5-script php 
Include conf/extra/php5_module.conf

#> save and exit .

$ sudo gedit /srv/http/info.php

#> add this in your php file:

<?php phpinfo(); ?>


{% endhighlight %}


finally, restart apache and all is done.enjoy!
