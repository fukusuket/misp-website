---
title: MISP 2.4.149 released (Autumn care-package - STIX 2.1 support and Cerebrate integration)
date: 2021-10-11
layout: post
banner: /img/blog/misp-long.png
---

# MISP 2.4.149 released

MISP 2.4.149 released including many bugs fixed along with some new and improved functionalities

# New features

- First stage of a massive rework of our STIX integration
- Various improvements to the integration with Cerebrate

# New STIX libraries

- The first version of a long ongoing project to rework our entire STIX integration has finally been merged, thanks to the tireless work of @chrisr3d
- Our converter libraries have embarked on a path of their own, becoming a standalone repository included by default in MISP, but also serving as a useful tool for anyone looking for a clean way of converting between the [MISP standard format](https://www.misp-standard.org/) and various STIX versions (1.1.1, 1.2, 2.0, 2.1).
- The libraries are still work in progress, but continuously improved, follow [misp-stix](https://github.com/MISP/misp-stix)
- Included is also a detailed documentation, which also serves as a knowledge base for the mapping between the two formats, available under the [documentation](https://github.com/MISP/misp-stix/tree/main/documentation) sub-directory
- From this release on, you have more control over which STIX version is used when exporting STIX data from MISP, by specifying the "stix_version" to be returned (supported versions for STIX 1: 1.1.1 and 1.2. For STIX 2: 2.0 and 2.1)

# Cerebrate integration

- Allow the fetching of sharing group data from Cerebrate instances, our new open source tool in development aiming to solve a host of issues revolving around community management and orchestration. Our first official release of the tool is scheduled for the MISP summit coming up this month
- To follow the cerebrate project, head over to its [github page](https://github.com/cerebrate-project/cerebrate)
- For the MISP summit to be held on the 21st of October, don't forget to watch the [misp-summit](/misp-summit). You can still apply for the [Call-for-Presentation](https://cfp.hack.lu/misp-2021/cfp).

# mail2misp release 1.0

First [official release 1.0 of mail2misp](https://github.com/MISP/mail_to_misp/releases/tag/v1.0), it's a tool to connect your mail infrastructure to MISP to create events based on the information contained within mail. The solution can be also used to feed MISP instance with honeypot receiving emails.

# Various improvements

- A long list of improvements, massive thanks to @JakubOnderka for the continuous stream of improvements and quality of life changes
- Thanks to the work of @righel, our [OpenAPI documentation](/documentation/openapi.html) is becoming more and more complete, now covering a long list of the more exotic endpoints and options

# Acknowledgement

We would like to thank all the [contributors](/contributors), reporters and users who have helped us in the past months to improve MISP and information sharing at large. This release includes multiple updates in [misp-objects](/objects.html), [misp-taxonomies](/taxonomies.html) and [misp-galaxy](/galaxy.html)
.

As always, a detailed and [complete changelog is available](/Changelog.txt) with all the fixes, changes and improvements.
