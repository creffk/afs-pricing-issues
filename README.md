# afs-pricing-issues
Using phpMyAdmin and SQL to identify and isolate API pricing Issues

I managed a web develoment project have a client that owns multiple storage unit facilies across the United States. Hey had a website, between technology issues of their current provider's out-of-the-box soluiton that was insufficiently customizable and poor support, they had a very poor conversion/checkout rate. They wanted to build a new website that was easy to use, attractive, could conduct A/B tests for CRO and that would allow them to have a hosted checkout process to process storage unit move-ins.

We worked with a 3rd party business solution that managed the move-ins, inventory and pricing. We used an API to sync inventories and prices.

After we launched the site we discovered that there were some pricing issues where some locations didn't have upgrade options and some units had the wrong pricing. 

As part of setting up the API, we created a copy of the units for each location into the website database, and instead of syncing all data, we only conducted a sync of the relevant data we needed. So this meant, if there was a pricing issue on the website, we could query the database to identify and isolate the locations, sizes, floors and units that the issues applied to in order to adjust the site programing for bug fixes. 

With the help of my development team, we developed a base SQL query that we used and modified to browse the database to inspect unit pricing. See "base-query".
