# GUAC Community Meeting: 2024-06-20

Recording: https://youtu.be/JWs6-fb_zo8

## Attendees

* Ben Cotton (Kusari)
* Marco Rizzi (Red Hat)
* Narsa Chelluri (Kusari)
* Jeff Mendoza (Kusari)
* Dejan Bosanac (Red Hat)
* Parth Patel (Kusari)
* Ridwan Hoq (Microsoft)
* Alex Feng
* Sunny Yip (Kusari)

## Agenda

* Introductions and welcome members!
* V0.7.0 ([blog post](https://guac.sh/blog/2024-06-04-guac-v0.7.0/))
    * Include Pagination for KeyValue
    * Added annotate-metadata command via guacone CLI (Experimental)
    * WIP for Get Next Actionable Critical Dependencies (Experimental - REST API)
    * Improved CDX parsing for transitive dependencies
    * GraphQL - Expose all client queries (paginated and non-paginated)
    * [ENT] Controlled and automated schema version migration via Atlas
    * Update certifiers to use paginated query for package and source
    * Update S3 collector to support collecting from a directory within the bucket
*  [Ben Cotton] assorted updates!
    * [Blog posts](https://guac.sh) are now individual files
    * Blog now has an [RSS feed](https://guac.sh/blog/index.xml)
    * Old meetings are now on the [YouTube channel](https://youtube.com/@guacsec) with notes in the [governance repo](https://github.com/guacsec/governance).
    * Moving the mailing list to lists.openssf.org ([governance#6](https://github.com/guacsec/governance/issues/6))
* [Ben Cotton] Proposal to add additional topic areas to the contributor ladder ([guac#1935](https://github.com/guacsec/guac/pull/1935))
* What are the maintainers working on section
    * [Parth] Expose certifier and deps.dev batch size and add optional latency
    * [Parth] Query OSV during ingestion for vulnerability feedback
        * Mention the pubsub idea to get feedback, and get folks to join this call if they’re interested 
    * [Brandon] Golang PURL trickiness
        * Ben: Brandon mentioned [ECMA TC54-TG2](https://ecma-international.org/task-groups/tc54-tg2/) should we have a maintainer join that?
* Next meetings
    * GUAC Time office hours: (EMEA & eastern Americas) tomorrow!
    * Weekly Maintainer Meeting: Monday
    * GUAC Time office hours: (Americas) Friday, July 5
    * Community Meeting: Thursday July 18