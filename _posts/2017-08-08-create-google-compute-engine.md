---
layout: post
title: "Create project on Google Compute Engine"
date: 2017-08-08
excerpt: "Create project on Google Compute Engine"
tags: [Google Cloud Platform, GCP]
---

{% include toc.html %}

# Create project on Google Cloud Platform (GCP)

If you don't have a Google Accout or your Google Account can not use Google Cloud Platform (GCP), please read [this guide](https://lequanglong.github.io/create-google-cloud-platform/).
<br>
If you already have had an account, you access to [this link](http://console.cloud.google.com), login with your account.

On the top-left, there is a down-arrow , click on that as below image : <br>
![alt text](https://farm5.staticflickr.com/4396/36343675972_aaf6f8a108_o.png "create new project on Google Console")

An popup will display, show all projects on your account in the list.<br>
![alt text](https://farm5.staticflickr.com/4338/36511823365_80e368a999_o.png "List projects on Google Cloud Platform")

Click on + button to begin to create new project.
<br>
![alt text](https://farm5.staticflickr.com/4352/36511822965_b992ea7003_o.png "Fill name of project on GCP")

Fill the naem of your project you want, then click on Create button.
You have to wait for awhile to Google create the project.

When the Google have finished, You will be redirect to other page. 
At this page, you will see all information about the project that you created.
<br>
![alt text](https://farm5.staticflickr.com/4430/35677087114_34c75a22a1_o.png "Information about the project on GCP")

# Create Google Compute Engine (GCE) instance runs Centos 7

Now, I will create a GCE instance. It has requirements as below:

+ It runs Centos 7
+ It has 3.75GB in memory.
+ It has 10GB HDD.
+ It allows http,https access.
+ ...
<br>
![alt text](https://farm5.staticflickr.com/4432/35677087394_37c76ea01d_o.png "Menu has Compute Engine")

Let's see on the top-left, click on the menu icon, then scroll down you will see a label has name is Compute Engine.
Click on it and begin to create new GCE instance. <br>
![alt text](https://farm5.staticflickr.com/4426/36343676242_914fede29e_o.png "Menu has Compute Engine")
<br>
![alt text](https://farm5.staticflickr.com/4376/35677444474_2a963a9655_o.png "Create a Compute Engine instance")

At this step, you have to fill your instance name, choose zone for your GCE instance, select your boot image disk, config your size of disk.
These are my configuration for my GCE instance.
Name : cakephp-instance-gce
Zone: Because my application serves in Tokyo, Japan. I choose asia-notheast1-a. (You can choose other zone based on your system)
Machine type : 1vCPU, 3.65 GB in memory.
Boot disk : I choose Centos 7
<br>
![alt text](https://farm5.staticflickr.com/4381/36115661130_ae58bd11b9_o.png "Choose the Boot disk for GCE instance")

You have to wait for awhile to Google create the instance, when it is done. 
You will see a screen like this : <br>
![alt text](https://farm5.staticflickr.com/4436/36465884756_779d15877b_o.png "Success to create GCE instance")

Congrats!

Now, you have a GCE instance. You can use it in to your application.
Next time, I will try to use it to install LAMP to run Cakephp application.

You can see all the above steps in the video as below : <br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/UvQ86wl-PtM" frameborder="0" allowfullscreen></iframe>


If you like my post, please leave with a comment:).
