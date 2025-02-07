---
title: MISP 2.4.81 released (aka new graphical visualisation and STIX 2.0 export)
date: 2017-09-18
layout: post
banner: /img/blog/misp-small.png
---

A new version of MISP [2.4.81](https://github.com/MISP/MISP/tree/v2.4.81) has been released including a significant rework of the graphical visualisation, support for STIX 2.0 export, multiple bug-fixes and improvements for misp-objects.

The new correlation graph has been improved and now includes the correlation at the galaxy (e.g. threat-actors, tools), taxonomy, attribute and the recently introduced object levels.

The navigation and expansion within the correlation graph has now a series of shortcut keys (`q` and `e`) to quickly navigate within large graphs. There is also a new contextual information pane,
to quickly show the currently selected and hovered nodes. This improves the navigation over large graphs and quickly expands the information from the selected nodes.

![MISP 2.4.81 new correlation graph](/img/blog/correlation-graph.png "{class='img-responsive'}")

STIX 2.0 is now supported as an export format in this release. Even though the STIX 2.0 format is still unpublished and at an early stage, we decided to implement a first export tool to see the gaps of
the format and helps our users to test the export with potential tools which start to support the version 2.0. As MISP commitment is to support the maximum of format, STIX 1.1 has been also expanded
to support the MISP objects in this release. Feedback on the current STIX 2.0 format export is welcome.

The attachment uploader has been updated to align to a consistent model between the standard and the advanced sample upload. The API now includes the support the advanced upload.

Server settings are now accessible via the API. The MISP XML format is now properly sanitised to provide continuous support for users still using the XML format, though we highly recommend to use the MISP JSON format instead. 

This release also includes many bug fixes (especially for misp objects) and a minor security fix. A huge thanks to all the contributors who reported bugs or opened pull-requests to improve MISP.

The full change log is available [here](https://www.misp.software/Changelog.txt). [PyMISP change log](https://www.misp.software/PyMISP-Changelog.txt) is also available.

Don't hesitate to [open an issue](https://github.com/MISP/MISP/issues) if you have any feedback, found a bug or want to propose new features.

Don't forget our [MISP summit 0x3](https://2017.hack.lu/misp-summit/) before the [hack.lu](https://2017.hack.lu/) 2017 conference which will take place from 14:00 to 18:00, Monday 16 October 2017. The core team of MISP will also join the [hack.lu open source security software hackathon 0x2 ](https://hackathon.hack.lu/) which will take place 19-20 October 2017.

A new MISP training will take place in Luxembourg the 21st November 2017, [registration is now open](https://www.eventbrite.com/e/misp-training-november-edition-tickets-36347289722).
