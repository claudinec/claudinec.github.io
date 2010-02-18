-*- markdown -*-

---
layout: disqus
title: Drupal Table Wizard and Migrate modules
---

[webchick's tutorial](http://www.lullabot.com/articles/drupal-data-imports-migrate-and-table-wizard)

Process:

* create content type; need [Automatic node titles](http://drupal.org/project/auto_nodetitle) to create composite title
* Access/Excel (!) -> CSV -> MySQL (don't mess with the data, just check field types)
* copy MySQL table to Drupal database
* Table Wizard to expose foreign table to Views
* Migrate: map foreign table to content type (need Migrate Extras for CCK)
* Rules: set node title after saving node

TODO (another post?):

* references between index records and public submissions
