---
layout: page
title: Projects
permalink: /projects/
---

<h1>Peter's parking project</h1>
<em>January 2014 - ongoing</em>
<br />
<a href="http://petersparkingproject.com">petersparkingproject.com</a>
<p>A smart city project using computer vision and networked cameras to find spots and elminate parking pain forever. Constructed a prototype with some basic computer vision techniques for the city of Borgholm. The prototype does not perform well right now as environmental conditions (locations of parking spot, seasons) have changed since it was built and optimised.</p>
<p>
    <a href="{{site.url}}/assets/dawn_filling_golden.png">
        <img width="150" style="float:left; padding:10px" src="{{site.url}}/assets/dawn_filling_golden.png">
    </a>
    <a href="{{site.url}}/assets/dawn_vacant.png">
        <img width="150" style="float:left; padding:10px" src="{{site.url}}/assets/dawn_vacant.png">
    </a>
    <a href="{{site.url}}/assets/day_busy.png">
        <img width="150" style="float:left; padding:10px" src="{{site.url}}/assets/day_busy.png">
    </a>
    <a href="{{site.url}}/assets/very_full.png">
        <img width="150" style="float:left; padding:10px" src="{{site.url}}/assets/very_full.png">
    </a>
    <div style="clear:both"></div>
</p>
<p>The next version includes 7 webcams from across the world, and more advanced computer vision which will improve accuracy substantially.</p>


<h1>TrackerKeeper</h1>
<em>May 2014 - ongoing</em>
<br />
<a href="http://trackerkeeper.co">trackerkeeper.co</a>
<p>A website with the objective of being a single place for keeping track of the multimedia links one consumes day to day, sharing them with others, and organising them into playlists.</p>
<p>Currently live is a website I prototyped in about four hours using google forms and some hacky jquery, which was a fun and very rewarding experience. It also inspired <a href="https://github.com/cmiceli">Chris Miceli</a> to build the terrifying and aptly named <a href="https://github.com/cmiceli/sheetyfs">SheetyFS</a>, a file system built out of Google Spreadsheets.</p>
<p>The next steps for the tool are replacing google forms with a backend that can fetch metadata from youtube and soundcloud, which should improve the user experience a lot. That will also mean it will have a real auth system. Along with that would be simple playlist management and some performance tuning.</p>

<h1>Basil Framework</h1>
<em>August 2013 - January 2014</em>
<br />
<a href="http://basilframework.com">basilframework.com</a>
<p>Basil is a backend as a service that aims to make web development better by providing typical web application requirements such as login, file uploading, and permissions, as interfaced components that can link to both the backend and frontend of your application.</p>
<p>I was selected to pitch Basil as a finalist at the USYD <a href="http://sydney.edu.au/business/genesis">Genesis business plan competition</a> in 2013 using <a href="https://docs.google.com/presentation/d/1qvK_DkQNHDPEPnQEfzBCNRcQYrxYQczjk0oZCzjtjXU/edit#slide=id.g10ee3a0fc_20">this slide deck</a>.</p>
<p>I spent a lot of time learning about CORS, thrift, ORMs, and designing the platform but have not had time to get to version 1 (preferring other projects).</p>
<p>There is an absurd amount of replicated code in the world. A quick examination of any popular set of applications or websites reveals that they are all offering very similar functionality, and yet the code providing the functionality is virgin. Login, logout, linking social accounts, uploading and viewing images and files, permissions systems, search functions, and so on.</p>
<p>Proof of the problem is in the popularity of the various services and tools that attempt to provide such usefulness out of the box. Rails is probably the best for attempting to address the problem, but the quality of Gems in functionality and security is not always good. Parse, AppBuddy, Firebase and many others attempted to address the same problem for mobile companies, where the narrow requirements found in across apps makes the issue of duplication even more painfully obvious. These companies have done well (I believe they've all been sold to various BigCorps now), but they lack appeal in building business applications. They don't guarantee they won't shut down one day (like FireBase, Parse soon), may own your data, and it's not easy to extend their functionality in your own backend.</p>
<p>Basil aims to combine the strengths of these two approaches and mitigate the weaknesses. It is a software package, available for free, with minimal configuration, and available as a thrift service to your application. When you are ready to scale, you can export the service with one click to the cloud.</p>

<h1>Harvest</h1>
<em>Early 2012</em>
<br />
<p>Collaborated with <a href="https://github.com/jsom">https://github.com/jsom</a> to design Harvest, a machine learning platform where you could upload your feature vectors and have a classification algorithm applied to them much faster than using a desktop application such as Weka. The idea got as far as us implementing a fast threaded random forest in C++, and spending a lot of time reading about all the hot-shot companies around the world who were popping up doing the exact same thing, like <a href="http://www.skytree.net/">SkyTree</a>, <a href="http://azure.microsoft.com/en-us/services/machine-learning/">Microsoft Azure</a> and <a href="https://bigml.com/">BigML</a></p>
<p>During my honors thesis I undertook to apply time series classification techniques to astronomical data. This involved running long machine learning experiments to explore the classifiation problem and verify my results. Although I could do other work while waiting for programs to finish, the turnaround time on the experiments was long enough to be disruptive to my thinking and attempting to solve the problem.</p>
<p>I was using Weka, a machine learning toolkit written in Java and produced by the University of Waikato. All credit to the Waikato guys, but Weka's algorithms are mostly for learning and lightweight experimentation, and they do not scale well. Frustrated with the slowness of my tools, I wondered at the potential of a cloud based service to make machine learning research faster. Machine learning classification algorithms have various strengths and weaknesses, but the structure of the input for most popular algorithms is almost the same.</p>
<ul>
    <li>Input consists of a vector of features either nominal or real valued. Nominal values e.g. 'A', 'B', 'C'. Input is separated into training, testing and unseen data (when applying the algorithm)</li>
    <li>Output consists of a class label applied to each vector</li>
</ul>
<p>So regardless of which algorithm you intend to use you may simply upload your input, run it through the platform, and download the output or a performance report.for whatever reason (usually a trade of of speed, accuracy, tendency to overfit and other classifier characteristics pertinent to the problem space), you may simply upload your input, apply the algorithm and download the output (or a report of the performance).</p>
<h1>Men's Style Forum Analysis</h1>
<em>September 2013 - ongoing</em>
<br />
<a href="https://bitbucket.org/urbanophile/sfscraper">bitbucket.org/urbanophile/sfscraper</a>
<p>Collaborated with <a href="https://bitbucket.org/urbanophile">urbanophile</a> to scrape the complete post history of <a href="http://www.styleforum.net">men's style forum</a>. Data cleaning has been done with some analysis and insight extraction still to come. Here are a few ideas we want to pursue:</p>
<ul>
    <li>Extracting fashion 'facts', e.g. pants and belt must match, from the text, using a fact extraction tool</li>
    <li>Doing basic analysis like watching certain categories of clothing change in popularity of seasons, mentions of color, or dominant colors in uploaded images</li>
    <li>Developing an impression of the favourite stores on the website, and brief summaries of their most liked products (e.g. Loake brand brogue shoes)</li>
</ul>

<h1>4chan Analysis</h1>
<a href="https://bitbucket.org/peterashwell/4chan-analysis/src">bitbucket.org/peterashwell/4chan-analysis/src</a>
<p>Scraped several months of popular 4chan board /b/ with the objective of filtering out the typical low-quality content and extracting creative and interesting posts. Culminated with me having 3 months of images and posts on disk, and unfortunately I never found time to try to rank and filter them. I'm still interested in long-term archivial of internet communities and will probably revisit this at some point.</p>

<h1>2011 Google AI Challenge - Ants</h1>
<a href="http://ants.aichallenge.org/profile.php?user=12556">ants.aichallenge.org/profile.php?user=12556</a> - my bot, 'antsbot', in action
<p>Collaborated with <a href="https://github.com/jsom">https://github.com/jsom</a> to build a successful AI bot in python for the 2011 Google AI challenge, a simple RTS game played against other people's programs from around the world. The bot was based on a simple diffusion field algorithm with some performance tweaks. It performed well, placing 308 out of 7897 entrants.</p>
