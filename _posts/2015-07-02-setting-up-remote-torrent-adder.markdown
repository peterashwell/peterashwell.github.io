---
layout: post
title:  "Setting up 'Remote torrent adder' chrome extension with feralhosting"
date:   2015-07-02 12:47:50
categories: remote torrent adder feralhosting seedbox chrome extension torrent
---
<p>I recently got a seedbox with feralhosting. It's a pretty good deal. I was doing some setup to make things easy including installing a slightly dodgy extension that intercepts torrent file downloads and sends them to the rutorrent client.</p>

<p>The instructions are a little vague on how to set up a configuration so I'll just paste my successfully working one in case someone else gets in trouble.</p>

<img src="/assets/seedbox_remote_torrent_adder.png">

<p>Things to note</p>
<ul>
  <li>DO NOT include the protocol (http, https) in the host field</li>
  <li>DO NOT include the trailing '/' in the hostname</li>
  <li>The port is whatever your torrent WebUI is running on. In my case, it is 80 so it doesn't appear at the end as that is the default. Often this will be something different
  and you'll see it after the colon when your webui is open e.g. <pre>http://somehost:&lt;THIS_PORT&gt;</pre></li>
  <li>Check SSL if you are using https when you access your web client.</li>
  <li>If you check SSL, you are using port 443. Change the port to 443.</li>
  <li>DO NOT include the trailing path from your webUI URL. At least the guide is clear on how to do that</li>
</ul>
<p>And it should work. If it doesn't, e.g. if you get the error: <pre>http server returned unexpected status 0</pre> then just carefully check the points above and your configuration<p>
