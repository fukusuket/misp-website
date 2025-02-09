---
title: MISP 2.4.144 released (Document all the things!)
date: 2021-06-07
layout: post
banner: /img/blog/misp-openapi.png
---

# MISP 2.4.144 released

MISP 2.4.144 released including a massive update to the documentation along with [CyCAT.org](https://www.cycat.org/) integration, improvements and fixes  including security related fixes.

# OpenAPI integration

We have a new core team member at MISP Project, Luciano (@righel), who kicked off his tenure with an impressive mapping of all the most important endpoints of MISP to OpenAPI. As of this release, the API documentation is directly available in MISP, along with example payloads and responses. You can also find [this information directly on the misp-project website](/documentation/openapi.html). To all integrators and developers wrangling with the API, we highly recommend you take a look at the API menu in MISP and we wish you happy and headache-free hacking!

# New diagrams and descriptions

Thanks to the thorough investigations of @mokaddem, we now have the entire synchronisation and authentication flows of MISP mapped in an easy to understand graph - both of these are included as of now directly in your MISP installation, so if you're in doubt about what's going on under the hood, but don't feel adventurous enough to replace your night time reading materials with a hefty chunk of PHP code, have a look at the new graphs!

- [Authentication Diagram](https://github.com/MISP/MISP/tree/2.4/docs/generic/Authentication%20Diagram)
- [Data visibility for Sync-users and MISP synchronisation](https://github.com/MISP/MISP/tree/2.4/docs/generic/Synchronisation)

# CyCAT integration v1

![MISP and CyCAT integration](/img/blog/cycat-misp.png)

CyCAT is a new initiative built by a group of individuals with the aim of cataloguing all the techniques and libraries around cyber-security, mostly with the selfish desire to make their own confusing lives easier (along with all those that are in a similar situation). As of this release, you'll be able to enable a first version of the CyCAT integration in MISP directly, allowing you to directly see relations to your galaxy clusters via CyCAT's own relationship system, giving you an extra layer of background information with the clusters already in use.

If you are interested in CyCAT and what it can do for you, head over to the [CyCAT website](https://cycat.org/).

To enable the CyCAT integration, got to the Plugin settings ![](/img/blog/cycat-enabled.png) and enable the feature.

# Improvements

- Various quality of life improvements and bug fixes, related to synchronisation, sharing groups, event reports and more!
- A security fix that would under certain circumstances result in attributes of an object being misassociated to the wrong sharing group after synchronisation. A massive thank you to Jeroen Pinoy for his diligent work in uncovering this issue!

# Acknowledgement

We would like to thank all the [contributors](/contributors), reporters and users who have helped us in the past months to improve MISP and information sharing at large. This release includes multiple updates in [misp-objects](/objects.html), [misp-taxonomies](/taxonomies.html) and [misp-galaxy](/galaxy.html)
.

As always, a detailed and [complete changelog is available](/Changelog.txt) with all the fixes, changes and improvements.

