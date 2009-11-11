---
layout: default
title: About
---

I am a research assistant at the University of Melbourne, working on a number of historical projects including [Founders and Survivors: Australian Lifecourses in Historical Context](http://www.foundersandsurvivors.org/).

Upcoming presentations:

* [Unlocking the ivory tower](lca2010/), LCA2010

Recent presentations:

* [Public
  history in the digital age](http://www.slideshare.net/claudinec/public-history-in-the-digital-age-presentation), presentation at
  `linux.conf.au` Free as in Freedom miniconference, January
  2009.

* [Digitising
  the paper panopticon](http://www.slideshare.net/claudinec/digitising-the-paper-panopticon-presentation), presentation at `linux.conf.au`
  LinuxChix miniconference, January 2009.

* [The
  Digital Humanities: A brief introduction](http://www.slideshare.net/claudinec/the-digital-humanities-presentation), presentation at
  AussieChix microconference, October 2008.

Although I now work mostly with Macs, I support the movements to promote free and open source software, and open access content.  I am a member of [AussieChix](http://au.linuxchix.org/), the Australian chapter of [LinuxChix](http://www.linuxchix.org/).

I am Anglican, and in my 'other life' I study theology at the [United Faculty of Theology](http://www.uft.edu.au/) and [Trinity College](http://www.trinity.unimelb.edu.au/theological_school).

I would love to hear from anyone who can tell me more about [my surname or family history](famhist.html).

I can also be found on <a  href="http://identi.ca/claudine/all">identi.ca</a>, <a href="http://www.flickr.com/photos/claudine/">Flickr</a>, <a href="http://www.linkedin.com/in/claudinec">LinkedIn</a>, <a href="http://www.dopplr.com/traveller/claudine/public">Dopplr</a> and <a href="http://www.facebook.com/claudine.chionh">Facebook</a>.

----

{% for post in site.posts limit:5 %}
  - <a href="{{ post.url }}">{{ post.title }}</a>
	  *Posted on {{ post.date | date_to_long_string }}.*
{% endfor %}

