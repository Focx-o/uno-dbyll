---
layout: post
title: Easiest Way To Install Lamp On Ubuntu
description: original post at WOWMORON
tagline: original post at wowmoron.wordpress.com
image: /assets/media/lamp.jpg
categories: [linux]
tags: [ubuntu, lamp, setup, tasksel]
---
<img src="{{page.image}}" width="85%"/>
<br/>
<br/>
LAMP(Linux, Apache, MySQL, PHP or Perl) is one of the most essential servers needed by the web developers or web entrepreneurs around the globe. This tutorial explains one of the easiest ways to install LAMP on Ubuntu. Because Ubuntu uses Linux as it’s kernel we are done with the Linux part ;) .


Install tasksel on your system:

{% highlight ruby %}

$ sudo apt-get update && sudo apt-get install tasksel

{% endhighlight %}

Tasksel is a Debian/Ubuntu tool that installs multiple related packages as a co-ordinated “task” onto your system.
Start tasksel:

{% highlight ruby %}

$ sudo tasksel

{% endhighlight %}

select the lamp-server and press 'Ok'. Follow the steps as directed and create your Mysql password.</br>
Lastly,start apache2 server:

{% highlight ruby %}

$ sudo service apache2 restart

{% endhighlight %}

Congratulations you have successfully installed LAMP server on your system. To test just visit your web browser and type in the following url:


<a href="http://localhost/">http://localhost/</a>


To test the php installation:
{% highlight ruby %}

$ sudo nano /var/www/phptest.php

{% endhighlight %}

type in and save:

{% highlight ruby %}

<?php phpinfo(); ?>

{% endhighlight %}

and open the following url in your browser:


<a href="http://localhost/phptest.php">http://localhost/phptest.php</a>