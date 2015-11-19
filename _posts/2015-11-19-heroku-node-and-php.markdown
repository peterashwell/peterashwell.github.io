---
layout: post
title:  "Building client side assets in heroku"
date:   2015-11-19 17:04:15
categories: heroku javascript client side build gulp grunt php
---

I've been building a PHP (yes) app in Heroku in a project recently. There is a client side component and I needed
to set up a javascript build process as part of the app. It wasn't immediately obvious how to do this and google
searches for

 - "Build client side assets heroku"
 - "Build javascript assets after deploy with gulp heroku"
 - "Run gulp after deploy heroku"

were surprisingly unhelpful, unless you were actually running a nodejs application.

So I'm a noob with Heroku - I admit that. Heroku is generally very good for noobs and it was still a little hard to figure out. I ended
up making the assumption that the instructions for nodejs would also work in other applications, crucially

 - Add the 'nodejs' buildpack to your app, along with whatever else (e.g. PHP)
 - Heroku will run npm install if you have a package.json in your app root
 - Heroku will run the "postinstall" script in your "scripts" block in package.json if it is there

Adding environment variables was easy to figure out so I added one for the app. The gulpfile can access those (even in postinstall).
I wrote the gulpfile and after a few silly mistakes saw my assets getting built correctly after deploy.

Thanks to <a href="http://stackoverflow.com/questions/24504476/how-to-deploy-node-that-uses-gulp-to-heroku">this stackoverflow question</a> and the <a href="https://devcenter.heroku.com/articles/nodejs-support#customizing-the-build-process">heroku nodejs guides</a> for being pretty clear.
