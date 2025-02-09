---
title: MISP 2.4.114 released (aka the community care package release)
date: 2019-08-31
layout: post
banner: /img/blog/community-view.png
---


# MISP 2.4.114 released

A new version of MISP ([2.4.114](https://github.com/MISP/MISP/tree/v2.4.114)) with some new features supporting collaboration and a list of fixes and small improvements. We strongly recommend to update to this version.

## Letting the world know about your community

One of the most common questions we get from users is whether we can point them to a community that would fit their profile and needs. This is something that often leaves as stumped. Being an open source project, we only really know the part of our user-base that we directly interact with and even if they do, the question of whether we should point users in their directions in the first place is often a puzzling one.

We've decided to make everyone's life just a tad bit easier. By incorporating an in-application registry of known communities, we not only allow organisations that run an ISAC or other sharing community to let potential new community members know that they exist in the first place, but also we also allow anyone with a MISP installation to conveniently send requests to communities for access.

Simply go to sync actions -> communities, browse the communities vetter or at least known by the MISP project and pick the ones that you consider yourself a good fit for. The system allows you to describe who you are and why you feel that you'd be an asset to the given community and send a request directly to the administrators of the instance.

The list of communities for now is rather brief, if you would like your community to be listed, get in touch us at the MISP project, or create a pull request describing your community.

## Keeping an eye on incoming delegation requests

As with all new features in MISP, we often struggle with anticipating the interest a new system would generate, often under-estimating the volume of data that they would generate. When we first implemented the delegation system, we expected it to be more of an edge-case scenario. We were obviously wrong, several communities out there rely quite heavily on being able to pseudo-anonymously publish data.

This is especially the case in ISAC/ISAO driven communities, where a central trusted authority ensures both the quality of the data produced as well as protecting the identity of those that wish to remain unknown when disclosing information that could be considered a successful intrusion.

We have now added an interface that allows users to search both received and issued delegation requests in a more convenient manner.

## Quality of life improvements for administrators

Added a new diagnostic tool that allows administrators to keep track of the database table sizes in MISP along with the potentially recoverable space by optimising the table.

## Taxonomies improved with the addition of an Industrial control systems and operational technology (ICS/OT) Taxonomy

Industrial control systems and operational technologies (ICS/OT) are often the target of threats, intrusions and attacks. The [FIRST.org Cyber Threat Intelligence SIG](https://www.first.org/global/sigs/cti/) did a tremendous work of documenting these into a series of taxonomies. To support and actively test the use of the ICS/OT taxonomy, the [ics taxonomy](/taxonomies.html#_ics) is now part of the default MISP taxonomy library. We also encourage any ICS/OT operators to contribute back to the [ics taxonomy JSON file](https://github.com/MISP/misp-taxonomies/blob/master/ics/machinetag.json) in order to improve the taxonomy based on their experiences. By being a taxonomy in MISP, this allows all ICS/OT users to directly tag and contextualise information shared within MISP instances and communities to describe their domain specific incidents and reports along with the related industrial threat intelligence.

## Fixes and improvements

- [contact reporter] Various fixes ensuring that the right users can be contacted
- [API] A long list of fixes ensuring consistency and proper responses for the less used endpoints, based on [@rafiot](https://github.com/rafiot/)'s exhaustive test suite
- [API] Fixed output of the attribute histogram. No more STIX-ish barf inducing numeric string keys for dictionaries
- [Feeds and warninglists] A long list of fixes tuning the performance of said subsystems
- [PostgreSQL] A list of fixes, making MISP work on psql
- [Import modules] Ensuring that the new, object supporting import modules can be called via the API
- [other] Various other fixes touching a long range of features, such as UI issues, object merge problems, invalid links and many more

We would like to thank all the [contributors](/contributors), reporters and users who have helped us in the past months to improve MISP and information sharing at large.

Special shout-outs to Jakub Onderka ([@JakubOnderka](https://github.com/JakubOnderka)) for the tireless work around tuning the warninglist systems and fixes all around, to Pierre-Jean Grenier ([@zaphodef](https://github.com/zaphodef)) for the massive list of fixes ensuring that our APIs behave more sanely and Beckhalo Evgeny ([@4ekin](https://github.com/4ekin)) for taming the beast that is PostgreSQL support.

We would also like to make a special dedication to the funding support of [CIRCL](https://twitter.com/circl_lu) and [INEA](https://twitter.com/inea_eu) under the CEF Telecom [2016-LU-IA-0098 grant](https://ec.europa.eu/inea/sites/inea/files/cef_telecom_supported_actions_november_2018.pdf).

As always, a detailed and [complete changelog is available](/Changelog.txt) with all the fixes, changes and improvements.

