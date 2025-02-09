---
title: MISP 2.4.99 released (aka API/UI fixes and critical security vulnerability fixed)
date: 2018-12-06
layout: post
banner: /img/blog/misp-small.png
---

A new version of MISP ([2.4.99](https://github.com/MISP/MISP/tree/v2.4.99)) has been released with improvements in the UI,  API, STIX import and a fixed critical security vulnerability.

Thanks to Francois-Xavier Stellamans from NCI Agency Cyber Security who reported a critical vulnerability in the STIX 1 import code. The vulnerability allows a malicious authenticated user to inject commands via an incorrectly escaped variable name (the original name of the STIX file). We strongly urge users to update their MISP instance to the latest version. We also replaced the mechanism of storing the original uploaded files on ingestion with a standardised function that will process the files without passing them to external tools - this reusable system will avoid any similar issues in the future if new similar mechanisms are introduced. [CVE-2018-19908](https://cve.circl.lu/cve/CVE-2018-19908)

This release includes the following changes:

- The following attribute types were added x509-fingerprint-md5 and x509 -fingerprint-sha256 to the network activity category.
- A new CLI interface to cleanup the brute-force protection entries from MISP.
- Some warning messages inconsistencies were fixed in the UI.
- Added a warning when a site administrator is trying to edit an event not belonging to the organisation of the site admin.
- [API] Object edit has been fixed to return the object in the correct format.
- When editing an object to add new attributes, correctly set the default distribution if nothing is set.
- Many fixes and improvement in the STIX 1 and STIX 2.0 import.
- XML MISP export has been fixed.

We would like to thank all the contributors, reporters and users who helped us in the past days to improve MISP.

MISP [galaxy](/galaxy.pdf), [objects](/objects.pdf) and [taxonomies](/taxonomies.pdf) were extended by many contributors. These are also included by default in MISP. Don't forget to do a `git submodule update` and update galaxies, objects and taxonomies via the UI.

A detailed and [complete changelog is available](http://www.misp-project.org/Changelog.txt) with all the fixes, changes and improvements.

Don't hesitate to have a look at our [events page](http://www.misp-project.org/events/) to see our next activities to improve threat intelligence, analytics and automation.

