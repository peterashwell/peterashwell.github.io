---
layout: post
title: "Webpack as proxy for doing API development"
date: 2015-06-05 09:48:00
categories: webpack, proxy, api, development
---
<p>You can find out how to do this <a href="http://webpack.github.io/docs/webpack-dev-server.html">here</a></p>

<p>It comes down to a config block that looks like this:</p>

<pre>
  devServer: {
    /* Send API requests on localhost to API server get around CORS */
    proxy: {
      '/<api_base_url>/*': 'http://<some_server>:<some_port>'
    }
  }
</pre>
