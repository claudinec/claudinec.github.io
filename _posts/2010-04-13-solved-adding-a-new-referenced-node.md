---
layout: post
title: Solved! Adding a new referenced node
author: claudine
nid: 68
created: 1271148384
---
The solution to [today's problem](/content/current-drupal-challenge-adding-new-referenced-node-without-editing-current-node) was the [Node Reference URL Widget](http://drupal.org/project/nodereference_url). It does exactly what I want: I was able to add a link to the bottom of a convict index node to create an 'additional information', automatically linked to the index node.

![submit additional information](http://farm5.static.flickr.com/4004/4517426588_06abebc476_o.jpg)

![backreference](http://farm3.static.flickr.com/2786/4517429438_107a8189b9_o.jpg)

When the 'additional information' node is created, the reference to the index node and the back-reference from the index node to the additional information node are both visible.

![index reference](http://farm5.static.flickr.com/4044/4516796651_c0fb0c2ed6_o.jpg)

![backreference](http://farm5.static.flickr.com/4064/4516798535_339273c08d_o.jpg)

I was confused at first because I was trying to add the node reference field from the index content type. To create the link in the right direction, I had to add the node reference field to the additional information node instead. Here's the diagram of the relationship between the two content types, managed by the awesome [Node Relationships](http://drupal.org/project/noderelationships) module:

![erd](http://farm3.static.flickr.com/2771/4517538686_ca47d04cfd_o.jpg)

Thanks, [quicksketch](http://drupal.org/user/35821) and [markus_petrux](http://drupal.org/user/39593)!
