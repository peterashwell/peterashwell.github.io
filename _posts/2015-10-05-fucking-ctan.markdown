---
layout: post
title:  "Fucking CTAN"
date:   2015-10-05 19:12:50
categories: ctan latex xelatex
---

So it's been a long time since I've done any latex work, and now (or maybe for a while?) there's this thing called CTAN which is a package manager for latex stuff, like, the tabularx or enumitem packages that you always need.

This is great, but how the fuck do you install things using this on Arch Linux, or any other linux? It is terribly confusing and I could not find clear answers anywhere on the internet. The utilities I did find did not appear to be maintained or did not work.

Here's how you do it

 1. Create a folder called `texmf` in your home directory like ~/texmf
 2. When you need something from CTAN, get the `.tds.zip` file. These are special archives that autoexpand and create the right directory structures for latex to lookup packages in
 3. Unzip the `.tds.zip` inside the `texmf` folder, and the package will be installed
 4. Run a program called `texhash` or `mktexlsr` somewhere. You will need to run it with sudo. It will update your latex indices so that it knows how to find your new files

Now you can return to torturing yourself with vspaces and hbox overflows and regretting choosing latex for this project, again.
