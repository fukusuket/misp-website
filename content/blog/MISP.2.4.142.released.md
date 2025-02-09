---
title: MISP 2.4.142 released (with new correlation features, UI sync functionality improved and new dashboard widgets)
date: 2021-04-27
layout: post
banner: /img/blog/new-ransomware-1.png
---

# MISP 2.4.142 released

MISP 2.4.142 released including many new features, a security fix and a long list of quality of life improvements.

# Correlation changes

One of the most annoying bottlenecks in how we use MISP currently is caused by low quality correlations, both in terms of usability and having a clear view on relevant relationships among data-points. These very often come from either sub-optimal strategies chosen on data creation/ingestion for certain types of attributes, but very often also on edge cases.

With the current release we've included two main tools to combat this:

### Correlation exclusions

We can now remove individual values from ever correlating again, so if you come across some typical noisy values (such as empty file hashes, registry values of 000000, internal IPs recurrinly encoded by your sandbox), you can add those to the exclusion list.

Once added, you can execute the cleaning of the existing correlations, to retroactively execute your exclusion rules. This is a background processed task and depending on the amount of correlations you have may take quite some time (it took us around 30 minutes on 25M correlations), so just fire it off and check back later whether the job has completed.

You can also comment your reason for removing an entry. In the future we plan on publishing community maintained default exclusion lists.

![Correlation exclusion in MISP](/img/blog/correlation-exclusion.png)

### Top correlations

List the most correlating values in your instance - in order to evaluate which the most problematic correlations are, simply have a look at the most noisy correlations. We've had some surprising entries in our communities, so perfect time to do some spring cleaning.

Just hit the delete button on a correlation and it will add a rule to your correlation exclusion list - just don't forget to run the historic cleanup from the correlation exclusion index to remove already existing correlations matching your newly added rules.

# Server sync rule management rework

![MISP server sync rule management](/img/blog/pull-rules.png)

One of the more painful aspects of managing servers has been the historically bad UI used to manage filter rules. This has now been completely revamped, both with a new look but familiar look and feel as well as some clever new tools to make it more usable.

For example, when creating pull filters, your instance will now attempt to contact the remote instance to retrieve a list of available tags, so that you no longer have to manually enter all of the filters when creating pull rules. The JSON rule field allowing custom filters now also uses a handy JSON parsing text entry, allowing you to avoid potential mistakes.

# New dashboard widgets

Thanks to Jeroen Pinoy, we have some new dashboard widgets meant to give you better oversight over how your instance is being used, showing some usage statistics as well as tools to monitor the growth of the user base of the community.

![](/img/blog/evolution-usercount.png)

# A bunch of other fixes including security fixes

We have also a [security](/security/) issue (CVE-2021-31780) causing a potential misalignment of sharing groups on synced attributes, so we highly encourage everyone to update their MISP instance.

Besides that we have introduced a long list of quality of life improvements as well as [many fixes](/Changelog.txt).

# Acknowledgement

We would like to thank all the [contributors](/contributors), reporters and users who have helped us in the past months to improve MISP and information sharing at large. This release includes multiple updates in [misp-objects](/objects.html), [misp-taxonomies](/taxonomies.html) and [misp-galaxy](/galaxy.html)
. The MISP galaxy includes a major update in the Ransomware galaxy which now includes more than 1600 documented ransomware.

As always, a detailed and [complete changelog is available](/Changelog.txt) with all the fixes, changes and improvements.

