---
layout: post
title:  "Network Manager on Arch Linux"
date:   2015-07-03 21:25:20
categories: network manager nm-applet arch linux
---
<p>Network manager automatically connects to networks for you, just like every other operating system wow!</p>
<p>Lots of pain and gotchas here</p>
<ul>
    <li>Obliterate every trace of netctl, netctl profiles, or any other network managers you are using or you'll get weird issues</li>
    <li>Try rebooting in between major changes e.g. enabling network manager</li>
    <li><code>nmtui</code> is basic ui for Network Manager and very helpful for figuring out what the fuck is going on</li>
    <li><code>network-manager-applet</code> package installs <code>nm-applet</code> which has a nice GUI for seeing networks</li>
    <li>My nm-applet did not come with an autostart script so I added it to my bash profile manually</li>
</ul>
<p>Main thing is to get rid of every trace of other network manager and to try rebooting. And be patient</p>
