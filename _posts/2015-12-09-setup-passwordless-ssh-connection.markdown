---
layout: post
title:  "Setup Passwordless SSH Connection"
date:   2015-12-09 10:51:25
categories: 
---
#Public Key and Private Key

Public Key --> encrypt

Private Key --> decrypt

#Generate Key Pair

{% highlight bash %}
$ ssh-keygen -t rsa -b 4096
{% endhighlight %}

This will generate two files id_rsa and id_rsa.pub.

id_rsa.pub is the public key, while id_rsa is the private key.

#Add Public Key to Server

{% highlight bash %}
$ ssh-copy-id user@server
{% endhighlight %}

This will add the default identified public key to the server which is store in `~/.ssh/id_rsa.pub`

It will promote you to enter the password btw.

**Enable Password Login**

In `/etc/ssh/ssh_config`, uncomment or add following to enable ssh login with password

{% highlight bash %}
PasswordAuthentication yes
{% endhighlight %}

And then restart SSH service with

{% highlight bash %}
$ sudo service ssh restart
{% endhighlight %}

*Vagrant default password is vagrant, the same as default username*


