---
layout: post
title: Edison Project Update
---

![Alt](/images/logo-debian.png)  

So my dad informed me that in addition to acting as a print server, he would like for the Intel Edison to act as a mini-NAS (network attached storage) box.
OK. Well turns out that Samba, the software I will be using to connect the Edison with out Windows PC's, also has NAS functionality. Great!  

However I did run into a small roadbump in the project. Apparently Yocto, the version of Linux provided by Intel for the Edison, is a rather
stripped down OS meant for IoT. Mainly, it doesn't have a package manager like apt-get which will be needed to install Samba and other necessary packages.
But no need to fear, Debian is here! It's available in the form of [Ubilinux](http://www.emutexlabs.com/ubilinux), a custom Linux image created for the Edison.  

To flash Ubilinux, just follow [this guide](https://learn.sparkfun.com/tutorials/loading-debian-ubilinux-on-the-edison) made by Sparksfun.
**Note:** for some reason I was not able to successfully flash on Windows, it had issues installing rootfs, and had to run the flash on Ubuntu. I suspect there is
something wrong with the windows batch script, and switching to the bash script worked. Your mileage may vary.  

That's all for now!
