---
title: MISP 2.4.86 released (aka sharing groups improvement, large information sharing communities support and more)
date: 2018-01-16
layout: post
banner: /img/blog/misp-small.png
---

A new version of MISP [2.4.86](https://github.com/MISP/MISP/tree/v2.4.86) has been released including improvements to the sharing groups and their respective APIs, granular access control of MISP-modules at an instance-level along with the usual set of bug fixes.

There are different use-cases of MISP especially when it comes to large information sharing and exchange communities such as those of ISACs (e.g. [X-ISAC](https://www.x-isac.org/) or similar organisations. Two main new features were introduced to improve the support of such scenarios:

- An optional feature to limit the visibility of organisations has been added where only site admins and sharing group editors can see the full organisation lists. This is an option that is disabled by default but can be enabled on-demand, if it is required in your use-case. Keep in mind sharing group editors can still see the full list of organisations (it's by design as it is an inherent requirement to expand and create sharing groups).
- An additional setting in the modules (expansion, import, export) allows limiting the accessibility to specific modules to a single organisation. This is quite useful when specific expansion services are limited to a single organisations such as services restricted due to API key restrictions or access to specific sensitive services (e.g. ticketing systems, SIEMs lookup,...)

Sharing groups are now manageable via the API opening up the possibility of creating and managing sharing groups via other applications.

A significant performance improvement (a gain of 50% is quite common) has been incorporated in the latest release when importing large batches of attributes into MISP via the UI or the API. Performance gains have also been made for the attribute index and attribute search, improving lookup times by a factor of 10, due to some silly MySQL indexing behaviors.

Many bug fixes and improvement were introduced in this version.

The full change log is available [here](https://www.misp.software/Changelog.txt). [PyMISP change log](https://www.misp.software/PyMISP-Changelog.txt) is also available.

In addition, [MISP dashboard](https://github.com/MISP/misp-dashboard) has been significantly improved and can be installed in junction with one or several MISP instances.

PyMISP has been refactored and improved. The PyMISP documentation has been updated [PDF](https://media.readthedocs.org/pdf/pymisp/latest/pymisp.pdf).

MISP [galaxy](/galaxy.pdf), [objects](/objects.pdf) and [taxonomies](/taxonomies.pdf) were notably extended by many contributors. These are also included by default in MISP. Don't forget to do a `git submodule update` and update galaxies, objects and taxonomies via the UI.

MISP trainings are foreseen the 17/01 and 18/01 in Luxembourg including a full-day API and extension hands-on session. [For more information and registration](https://www.circl.lu/services/misp-training-materials/). We have also many other trainings (Vienna in February) and events foreseen in 2018, [for more information](/events/)

