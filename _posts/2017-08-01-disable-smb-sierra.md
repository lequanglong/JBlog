---
layout: post
title: "Disable SMB Signing on macOS Sierra"
date: 2017-08-01
excerpt: "Disable SMB Signing on macOS Sierra"
tags: [MAC OS X, MAC OS Sierra, Sierra]
---

{% include toc.html %}

# Disable SMB Signing on MAC OS Sierra

 ``` bash
 sudo -s
 echo "[default]" > /etc/nsmb.conf
 echo signing_required=no >> /etc/nsmb.conf
 exit
 ```
 To check that it properly wrote the nsmb.conf file:
 ``` bash
 cat /etc/nsmb.conf
```
 result:
  ``` bash
 [default]
signing_required=no
 ```
Check if SMB signing is disabled on your share after you remount the SMB volume
smbutil statshares -a
<p>
================================================================================================== <br>
SHARE                         ATTRIBUTE TYPE                VALUE<br>
==================================================================================================<br>
</p>
If you see the the SIGNING_ON = TRUE Variable, that means its still on and you did not execute the instructions properly.

This variable should not show up after you have disabled SMB signing on the OS X 10.11.5 client. This is also applicable for OS X 10.11.6>10.12 (Mac OS Sierra)
