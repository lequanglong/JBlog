---
layout: post
title: "Working on GCP with gcloud command line"
date: 2017-08-08
excerpt: "Working on GCP with gcloud command line"
tags: [Google Cloud Platform, GCP, GCE, GAE, Google Compute Engine, Google App Engine, Google Cloud SQL, Google Cloud SDK,gcloud]
---
{% include toc.html %}

# Install Google Cloud SDK
You can refer [this link](https://cloud.google.com/sdk/docs/) to read full instruction.
I just note how to install Google Cloud SDK on MAC OS X.

+ Click to [download Google Cloud SDK](https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-166.0.0-darwin-x86_64.tar.gz).
+ Extract the package to any location you want.(I put it at : /Users/lequanglong/google-cloud-sdk)
+ Access to the extracted folder, open the Terminal application on MAC OS X , copy the commands as below, paste to the Terminal then press Enter key on your keyboard: <br>
<b>cd /Users/lequanglong/google-cloud-sdk</b><br>
<b> ./install.sh</b>

Or you can install Google Cloud SDK by copy the below command into Terminal: <br>
<b>curl https://dl.google.com/dl/cloudsdk/release/install_google_cloud_sdk.bash | bash</b><br>
After the the installation is finished, you can check the gcloud command is working or not by type : <br>
<b>gcloud -v</b>
I will return the version of Google Cloud SDK.
This is my result : 
<b>Google Cloud SDK 147.0.0</b>

If you can not run the gcloud on any location, please check the bash_profile at <br>
<b>sudo vi ~/.bash_profile</b><br> 
this is my bash_profile file:
<pre>
export PATH="/usr/local/mysql/bin:$PATH"
LUNCHY_DIR=$(dirname `gem which lunchy`)/../extras
   if [ -f $LUNCHY_DIR/lunchy-completion.bash ]; then
     . $LUNCHY_DIR/lunchy-completion.bash
   fi

# The next line updates PATH for the Google Cloud SDK.
if [ -f '/Users/lequanglong/google-cloud-sdk/path.bash.inc' ]; then source '/Users/lequanglong/google-cloud-sdk/path.bash.inc'; fi
export PATH=/Users/lequanglong/google-cloud-sdk/bin:$PATH
# The next line enables shell command completion for gcloud.
if [ -f '/Users/lequanglong/google-cloud-sdk/completion.bash.inc' ]; then source '/Users/lequanglong/google-cloud-sdk/completion.bash.inc'; fi
export PATH=/usr/local/mysql/bin:/Users/lequanglong/google-cloud-sdk/bin /usr/local/bin /usr/bin /bin /usr/sbin /sbin
</pre>
Let's play some commands with <b>gcloud</b> command.

+ Authentication with your account 
<b>gcloud auth login</b>

![alt text](https://farm5.staticflickr.com/4411/36344871062_486a2f4d73_o.png "gcloud auth login")
<br>
![alt text](https://farm5.staticflickr.com/4427/36116606800_b688890e20_o.png "authentication for gcloud")

<br>
![alt text](https://farm5.staticflickr.com/4344/36116606660_82099a2d31_o.png "authentication successfull")

+ Show projects list <br>
<b>gcloud projects list</b>
![alt text](https://farm5.staticflickr.com/4382/36116756600_34a1171bdf_o.png "gcloud projects list")

# Working with Google App Engine with gcloud

# Working with Google Compute Engine with gcloud

# Working with Google Cloud SQL with gcloud
