# GUAC Community Meeting: 2024-05-16

Recording: https://youtu.be/haTT5MonTA0

## Attendees

* Jon Zeolla (Zenable)
* Ben Cotton (Kusari)
* Jeff Mendoza (Kusari)
* Narsa Chelluri (Kusari)
* Sunny Yip (Kusari)
* Ridwan Hoq (Microsoft)
* Alex Feng (Microsoft)
* Tim Miller (Kusari)
* Marco Rizzi (Red Hat)
* Arnav Joshi (Akami)
* Parth Patel (Kusari)
* Michael Lieberman (Kusari)
* Soham Arora (Purdue)
* Hari Kunduru (ARA)

## Agenda

* Introductions and welcome members!
    * Ben just joined Kusari as the Open Source community lead
    * Welcome Ben!
* Announce new community promos (mdeicas)
    * Congrats to Marco D, Dejan, and Marco R!!
* Guacanalyze (soham)
    * Command addition to guacone
    * Unified tree diff between two sboms
    * Union as well as intersect
    * Demo: guacone analyze diff –uri –sboms=<sbom1>,<sbom2>
    * Differences are shown
    * Code is in PR currently: https://github.com/guacsec/guac/pull/1809
* V0.6.0 Release and blogpost (Jeff)
    * Support for ENT (Postgres) and KeyValue (inmem)
    * https://guac.sh/blogs/
    * https://github.com/guacsec/guac?tab=readme-ov-file#graphql-backends
    * https://github.com/guacsec/guac/releases/tag/v0.6.0 
* New contributors recognition
    * https://github.com/guacsec/guac/pulls?q=is%3Apr+author%3Arakshitgondwal
    * https://github.com/guacsec/guac/pulls/Yaxhveer
    * https://github.com/guacsec/guac/pulls?q=is%3Apr+author%3Anchelluri+is%3Aclosed (Narsa)
    * https://github.com/guacsec/guac/pull/1779 (ribby bibby)
* Proposal for IsRunning nodes (Alex and Ridwan)
    * Usecase - you have log4j running, where is it?
    * Inventory where a vuln is running is a hard problem
    * Need to have more discussion about what the IsRunning node consist of
    * Will this be complimentary to IsDeployed?
    * What about shadow IT? A deployment occurs without following the proper procedure
    * The discrepancy between what is running and what is not?
        * One cause for this could be the isRunning may not be up to date with the attestation
* [Mike] Update to meetings
    * Now that GUAC is growing, should we meet more frequently for working group meetings?
    * Ben suggests no, since video meetings can be exclusive. Let’s focus on async conversation in Slack and GitHub until we reach a point where we consistently can’t cover the full agenda in meetings
* Pick facilitator for next time June 20th
    * It’s Ben!
* Upcoming events
    * GUAC Time office hours: 24 May at 1300 UTC
    * [OpenSSF Tech Talk](https://zoom.us/w/94532244491?tk=rX2ZHRNzC9JGGL7q49MtlfqIW_6HxE-OR_Y1I49o39A.DQYAAAAWAo-UCxY5cWo3dW5KM1FpcUU3QlNEQkdwMkNnAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA&uuid=WN_jxAYJJieTVel2bdwzd3Aag): 6 June at 1700 UTC
    * [CNCF Live](https://community.cncf.io/events/details/cncf-cncf-online-programs-presents-cloud-native-live-guac-101-dip-into-the-delicious-world-of-software-supply-chain-security/): 11 June at 1600 UTC
