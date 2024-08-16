# GUAC Community Meeting: 2024-08-15

Recording: https://youtu.be/S-oHYvoBx70

## Attendees

* Ben Cotton (Kusari)
* Jeff Mendoza (Kusari)
* Nathan Naveen (Kusari)
* Dejan Bosanac (Red Hat)
* Brandon Lum (Google)
* Marco Deicas (Google)
* Mike Lieberman (Kusari)
* Narsa Chelluri (Kusari)
* Parth Patel (Kusari)
* Nick Vidal (Open Source Initiative)
* Alex Feng (Microsoft)
* Arvind Singharpuria
* Tim Miller (Kusari)
* Sunny Yip (Kusari)

## Agenda

* Welcome:
    * Arvind, joining back after a long time! Recent college graduate! Looking to contribute.
* [Ben Cotton] Contributor ladder updates: https://guac.sh/contributing/#contributor-ladder 
* [Nathan Naveen] rate limiting for Deps Dev, OSV, and ClearlyDefined
    * Don’t want to hit external APIs too much and get blocked
    * Currently open PR
    * 2 limiters
        * HTTP - for osv and clearly defined
        * GRPC limiter - deps.dev
* [Nathan Naveen] REST endpoints to find the latest SBOM as well as the vulns and licenses in the latest SBOM
    * Do we want to have an endpoint that lists all of the packages that match a specific query? For example “list all versions of Log4j/core”. Brandon suggested something like the “[Terror of cURL](https://www.kusari.dev/blog/terror-of-curl)” blog post.
    * ACTION: Mike to open an issue to discuss the specific use case
* [Nathan Naveen] end-to-end testing updates
* [Jeff/Parth] Demo ClearlyDefined integration
    * Included in v0.8.0. See the blog post: https://guac.sh/blog/2024-08-01-clearlydefined/
    * ClearlyDefined provides “discovered” licenses beyond just the declared license of a package
    * Includes attribution information
* [Parth Patel] Breaking change in Ent databases if re-ingesting existing SBOMs: https://github.com/pxp928/guac-update-db
    * Due to `IsDependency` being changed in v0.8.0 to only version-to-version, not package name
    * With existing databases, upgrades from <= 0.7.2 to 0.8.0 will break.
    * Parth’s script will check the database and fix the relationships if run prior to the upgrade.
* [Abhisekh / Brandon] User Journey interviews and looking for participation
    * [GUAC user journey study](https://docs.google.com/document/d/18D0B0pjNu4bbeu_emzKdwGby4ci7Hi8gjJ6aZsjmud4/edit#heading=h.pcq73hkmltrn)
* What are users expecting for ingestion time?
* Upcoming events (see [OpenSSF calendar](https://openssf.org/getinvolved) for meeting details)
    * GUAC Time office hours: tomorrow! (EMEA & eastern Americas)
    * Weekly Maintainer Meeting: Monday
    * GUAC Time office hours: Friday 30 August (Americas) 
    * Community Meeting: Thursday 19 September
