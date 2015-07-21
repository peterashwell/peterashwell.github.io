---
layout: post
title:  "NPM will not install on VirtualBox mounted folders"
date:   2015-07-21 17:41:30
categories: network manager nm-applet arch linux
---

VirtualBox mounted folders do not allow for the creation of symlinks, so if you try to run `npm install` you will get a wall of errors a mile long. Good news though, there a couple of solutions!

- `npm install --no-bin-links` - Tell npm not to use symlinks. Don't know what kind of weirdness this does. Probably some incredible inefficiency of space use. Some npm packages (`gulp-jsdoc`) still failed when using this.
- Tell VirtualBox to allow symlinks for your particular shared folder - <a href="http://ahtik.com/blog/2012/08/16/fixing-your-virtualbox-shared-folder-symlink-error/">documented more here</a>. The command is `VBoxManage setextradata YOURVMNAME VBoxInternal2/SharedFoldersEnableSymlinksCreate/YOURSHAREFOLDERNAME 1`. You need to *restart virtualbox* to get this to start working. I did this and it worked for me.

These answers came from <a href="http://stackoverflow.com/questions/8232778/nodejs-npm-installing-modules-on-ntfs-partition">this SO question</a>
