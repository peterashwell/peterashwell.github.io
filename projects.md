---
layout: page
title: Projects
permalink: /projects/
---

<h1>Peter's parking project</h1>
<a href="http://petersparkingproject.com">petersparkingproject.com</a>
<p>A smart city project using computer vision and networked cameras to eliminate the pain of parking forever. Constructed a prototype with some basic computer vision techniques for the city of Borgholm. Unfortunately prototype performs poorly as environmental conditions (locations of parking spot, seasons) have changed since it was built and optimised. More to come.</p>

<h1>TrackerKeeper</h1>
<em></em>
<a href="http://trackerkeeper.co">trackerkeeper.co</a>
<p>A website for keeping track of the multimedia links one consumes day to day, sharing them with others, and organising them into playlists. Prototyped in four hours using google forms and some hacky jquery.</p>

<h1>Basil Framework</h1>
<em>August 2013 - January 2014</em>
<a href="http://basilframework.com">basilframework.com</a>
<p>A backend as a service that aims to make web development better by providing typical web application components, such as chat, login and file uploading as interfaced components that can link to both the backend and frontend of your application.</p>

<p>There is an absurd amount of replicated code in the world. A quick examination of any popular set of applications or websites reveals that they are all offering very similar functionality, and yet the code providing the functionality is virgin. Login, logout, linking social accounts, uploading and viewing images and files, permissions systems, search functions, and so on. Proof of the problem is in the popularity of the various services that attempt to provide this functionality out of the box. Rails is probably the best for attempting to address the problem, but the quality of Gems in security and functionality is not always good. Parse, AppBuddy, Firebase and many others attempted to address the same problem for mobile companies, where the narrow scope of functionality found in an app makes the issue of duplication even more painfully obvious. These companies have done well (I believe they've all been sold to various BigCorps now), but I believe they lack appeal in building business applications, or anything more serious than a lame social app because they don't guarantee they won't shut down one day (FireBase, Parse soon), may own your data, and because it's not easy to extend their functionality into your own backend.</p>

<p>Basil aims to combine the strengths of these two approaches. It is a software package, available for free, with minimal configuration providing gem-style functionality as a thrift service to your application. When you are ready to scale, the software package can be exported to an online service with minimal effort.</p>

<h1>Harvest</h1>
<em>Early 2012</em>
<p>Harvest was a machine learning platform where you could upload your feature vectors and have a classification algorithm applied to them much faster than using a desktop application. The idea got as far as me implementing a threaded random forest in C++, and spending a lot of time reading about all the hot-shot companies around the world who were just appearing doing the exact same thing.</p>
<p>
During my honors thesis I undertook to apply time series classification techniques to astronomical data. This involved running long machine learning experiments to explore the classifiation problem and verify my results. Although I could undertake other tasks, the turnaround time on the experiments was long enough to be disruptive to my thinking and attempting to solve the problem. I was using Weka, a machine learning toolkit written in Java and produced by the University of Waikato. All credit to the Waikato guys, but Weka's algorithms are mostly for learning and lightweight experimentation, and they do not scale well. Frustrated with the slowness of my tools, I wondered at the potential of a cloud based service to make machine learning research faster. Machine learning classification algorithms have various strengths and weaknesses, but the structure of the input for most popular algorithms is almost the same.
</p>
<ul>
    <li>Input consists of a vector of features either nominal or real valued. Nominal values e.g. 'A', 'B', 'C' can be represented by numbers in certain algorithms</li>
    <li>Output consists of a nominal class label</li>
</ul>
<p>
    So regardless of which algorithm you intend to use, for whatever reason (usually a trade of of speed, accuracy, tendency to overfit and other classifier characteristics pertinent to the problem space), you may simply upload your input, apply the algorithm and download the output (or a report of the performance). That was the objective with Harvest.
</p>

<p>
<h1>Men's Style Forum Analysis</h1>
<a href="https://bitbucket.org/urbanophile/sfscraper">bitbucket.org/urbanophile/sfscraper</a>
<p>Collaborated with <a href="https://bitbucket.org/urbanophile">urbanophile</a> to scrape the complete post history of <a href="http://www.styleforum.net">men's style forum</a>. Data cleaning has been done with some analysis and insight extraction still to come.</p>

<h1>4chan Analysis</h1>
<a href="https://bitbucket.org/peterashwell/4chan-analysis/src">bitbucket.org/peterashwell/4chan-analysis/src</a>
<p>Scraped several months of popular 4chan board /b/ with the objective of filtering out the typical low-quality content and extracting creative and interesting posts. Culminated with me having 3 months of images and posts on disk, and unfortunately I never found time to try to rank and filter them.</p>

<h1>2011 Google AI Challenge - Ants</h1>
<a href="http://ants.aichallenge.org/profile.php?user=12556">ants.aichallenge.org/profile.php?user=12556</a> - my bot, 'antsbot', in action
<p>Built a successful AI bot in python for the 2011 Google AI challenge, a simple RTS game played against other people's programs from around the world. The bot was based on a simple diffusion field algorithm with some performance tweaks. It performed well, placing 308 out of 7897 entrants.</p>
