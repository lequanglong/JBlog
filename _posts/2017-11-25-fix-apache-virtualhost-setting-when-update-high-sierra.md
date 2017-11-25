---
layout: post
title: "Note for upgrade Mac OS X from Sierra to High Sierra"
date: 2017-08-08
excerpt: "How to update config apache, php , virtual host when update to High Sierra"
tags: [Google Cloud Platform, GCP]
---

{% include toc.html %}

# 1. Fix Apache when update to High Sierra

## a) Fix httpd
Backup new configuration.

```{r, engine='bash', count_lines}
sudo cp /private/etc/apache2/httpd.conf /private/etc/apache2/httpd.conf.bak
```
Restore to previous configugration
```{r, engine='bash', count_lines}
sudo mv /private/etc/apache2/httpd.conf~previous /private/etc/apache2/httpd.conf
```
Config correct the module php you want to use.
I use php5.6.30.
Find the line : LoadModule php5_module libexec/apache2/libphp5.so
Update the line to your path:
My path : LoadModule php5_module  /usr/local/php5/libphp5.so
On top of file , add two lines

AddType x-httpd-php .php
AddHandler application/x-httpd-php .php .php5

## b) Fix VirtualHost

Backup new configuration.

```{r, engine='bash', count_lines}
sudo cp /private/etc/apache2/extra/httpd-vhosts.conf /private/etc/apache2/extra/httpd-vhosts.conf.bak
```
Restore to previous configugration
```{r, engine='bash', count_lines}
sudo mv /private/etc/apache2/extra/httpd-vhosts.conf~previous /private/etc/apache2/extra/httpd-vhosts.conf
```
Verify your fixing by runing below command

httpd -S

Check your hosts file: sudo vi /etc/hosts

Restart apache : sudo apachectl restart.

That is all.



