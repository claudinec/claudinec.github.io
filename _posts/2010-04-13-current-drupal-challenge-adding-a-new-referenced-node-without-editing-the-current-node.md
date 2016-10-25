---
layout: post
title: 'current Drupal challenge: adding a new referenced node without editing the
  current node'
author: claudine
nid: 67
created: 1271121818
---
The Founders and Survivors project is giving me plenty of challenges and opportunities to learn more about Drupal (not to mention challenges of other kinds). This morning's challenge is:

We have a view of the [Archives of Tasmania convict index](http://www.foundersandsurvivors.org/convindex) and a new, improved form for users to submit additional information on convicts, such as dates and places of birth and death. I have added an 'additional information' field to the convict index content type, which is a node reference to the 'additional information' type. I want users to be able to add an additional information node which is referenced from the relevant index node, without having to edit the index node.

The **[node_widget](http://drupal.org/project/node_widget)** module looks like part of the solution: it allows you to add or edit the additional information node within the convict index node (which simplifies the process for non-tech users) **but** (1) it doesn't include multigroup fields and (2) the user still has to edit the node, which I think is a stumbling block for our target audience.

I'm seeing responses coming in to my queries on [identi.ca](http://identi.ca/conversation/28261961#notice-28309106) and [twitter](http://twitter.com/claudinec/status/12075633421) but I'm also posting here to help clarify things in my own mind and as a reference in case I do find a solution.
