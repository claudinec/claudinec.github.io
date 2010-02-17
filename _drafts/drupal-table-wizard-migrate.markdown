---
layout: disqus
title: Drupal is my database -- importing 80,000 convicts with Table Wizard and Migrate
---

One of the goals of the [Founders and Survivors](http://www.foundersandsurvivors.org/) project (the one that concerns me the most) is to compile and publish data about the Van Diemen's Land convicts from a variety of sources, and make links or cross-reference between records from different sources that relate to the same individual (or, potentially, the same family). Our [sources](http://www.archives.tas.gov.au/generic/convict_examples) include convict indents carried on the convict ships, conduct records, police gazettes, and registers of births, deaths and marriages. In addition, we have been collecting biographies and family histories submitted by descendants of convicts, which are valuable sources of information about the lives of convicts after they left the penal system.

Biographies have been submitted by members of the public through our Drupal website as a custom content type using the [CCK](http://drupal.org/project/cck) module. The other data exists in paper records which are being transcribed and in some cases photographed. Transcriptions have been entered in a variety of desktop-oriented data collection systems, including Filemaker Pro, Microsoft Access and Microsoft Excel. My goal is to make this data available to other researchers and members of the public in open formats and through the web. As I have got to know Drupal better, I have come to see that it is a powerful way of representing strucutred data as well as free-form documents on the web, and it can also handle the privacy and access control we need to prevent unethical use of data.

The Archives of Tasmania have an online [Index to Tasmanian Convicts](http://portal.archives.tas.gov.au/menu.aspx?search=11) and I was given a copy of this data in Microsoft Access. This index will form the basis of the entire Founders and Survivors database, so that a record of a convict in the index will contain links to all of the other data we have on that individual. After exporting the index data to a comma-separated text file (so that I don't have to touch Access again) I hacked together a Perl script to extract data from this file and insert it directly into the MySQL database used by Drupal. It *looked* as if the script did what I wanted it to do, but I wasn't confident about it and didn't run it on our production database before I left for LCA2010 and DrupalSouth, where Angie Byron gave me [a better solution](http://www.lullabot.com/articles/drupal-data-imports-migrate-and-table-wizard). (Why yes, I *do* lose years off my life every time I attempt a bulk migration!)

Angie's article is a good tutorial on using the Table Wizard and Migrate modules generic data migration process. This is the full process I needed to set up migration for the Archive index (which is still underway -- 80,000 records don't appear instantaneously).



Process:

* create content type; need [Automatic node titles](http://drupal.org/project/auto_nodetitle) to create composite title
* Access/Excel (!) -> CSV -> MySQL (don't mess with the data, just check field types)
* copy MySQL table to Drupal database
* Table Wizard to expose foreign table to Views
* Migrate: map foreign table to content type (need Migrate Extras for CCK) check 'Node: Published'


Access to text to MySQL

Create content type

Rule to change title after creation

Table Wizard

Migrate to map table to content

Published status

Drush


I have a working procedure. Actually importing the data is the time-consuming part now. (`drush migrate` as a cron job)


TODO (another post?):

* references between index records and public submissions
