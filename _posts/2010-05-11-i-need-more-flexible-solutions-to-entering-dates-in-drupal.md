---
layout: post
title: I need more flexible solutions to entering dates in Drupal
author: claudine
nid: 70
created: 1273565184
---
The [Founders and Survivors](http://www.foundersandsurvivors.org/) website has to cater for users with a wide range of technical skills, though the primary audience is genealogists (who I think are largely self-taught, in terms of both historical research and computer skills). The data we collect has to conform to the expectations of this audience, but I also have to be able to generate data dumps (currently in raw XML format) that meet the needs of our researchers (who also come from a broad range of technical and disciplinary backgrounds).

I am currently being driven up the wall by challenges in date input. I should write up some proper issue reports for the [Date](http://dgo.to/date) project but for now I'm just trying to explain the issues to myself.

For our mostly Australian and British users, entering a date as day, month and year is natural and intuitive. However, any of the following could be natural and intuitive:

* 11 April 2010
* 11 April, 2010
* 11 Apr 2010
* 11 Apr, 2010
* 11/04/2010
* ...

It doesn't appear to be possible, at the moment, to allow different formats -- Date expects the admin to enforce one format for each field. This does not assist me in my goal of making the site easy for non-technical, non-documentation-reading users.

The help text uses the current date as an example. For a month that is spelled out rather than numeric, 'May' is ambiguous -- is it a three-letter abbreviation or a full month?

In historical and genealogical research, we must be able to accommodate approximate dates: the month or day might be unknown, or a user might not even have an exact year, only a decade. There is a [patch](http://drupal.org/node/259308#comment-2722636) to Date to allow flexible granularity (leaving out the day or month), but so far this only appears to work with y-m-d format. The geeks on the project understand y-m-d, but this may not be easy for our ordinary users.

One alternative to specifying a text input format would be to use the popup widget, but this is not really helpful because: (1) no one will want to click the left arrow >150 times to get back to the 19th century, where the majority of dates belong; (2) the date is filled in in m/d/y format which is really not helpful for our audience or project.

And I don't know PHP (or have the time to learn it) well enough to find and fix these issues myself.
