# GUAC Community Meeting: 2024-07-15

Recording: https://youtu.be/skcO66K-Q_g

## Attendees

* Narsa Chelluri (Kusari)
* Jeff Mendoza (Kusari)
* Ridwan Hoq (Microsoft)
* Parth Patel (Kusari)
* Soham Arora (Purdue)
* Ben Cotton (Kusari)
* Tim Miller (Kusari)
* Sunny Yip (Kusari)


## Agenda

* Reminders
    * [Mailing lists are moving](https://guac.sh/blog/2024-06-21-mailing-list-move/). Should we mass-migrate everyone?
* Introductions and welcome members!
* [Ben Cotton] Community updates
    * Stats from the last quarter
        * 6 first-time contributors
        * 2 contributor ladder promotions
        * 7 non-maintainers joined the Maintainers Meetings, representing 5 different affiliations
    * Goals for this quarter
    * 6 first-time contributors
    * 2 contributor ladder promotions
    * Add 1 major company or FOSS project as a reference user
* [Ben Cotton] web & marketing updates
    * New [Why GUAC? page](https://guac.sh/why-guac/) to help with messaging
    * GUAC added to the [OpenSSF SBOM Catalog](https://sbom-catalog.openssf.org/catalog/)
* What are the maintainers working on?
* Vuln scan on ingestion (not certifier)
    * Ridwan: can Deps.Dev be done at the same time to fill out the entire tree at time-of-ingestion?
        * Parth: It’s possible, but it adds a lot of latency to the ingestion. Deps.Dev runs as a collector-subscriber so it’s not waiting on an interval. Once the SBOM is ingested, the Deps.Dev request gets queued, so you’ll get the data in (probably) a few minutes.
        * Ridwan: Should the vulnerability certifier then be done the same way?
        * Parth: Collector-subscribers only run once, but certifiers run at an interval. We want vulnerability info to be updated if new vulns are discovered. It’s not using ingestion data, it’s using graph data.
* Delete HasSBOM HasSLSA and CertifyVuln
* [Nathan Naveen] end-to-end testing updates
    * We’ll wait until next month when Nathan can present
* Upcoming events (see [OpenSSF calendar](https://openssf.org/getinvolved) for meeting details)
    * GUAC Time office hours: tomorrow! (EMEA & eastern Americas)
    * Weekly Maintainer Meeting: Monday
    * GUAC Time office hours: 2 August (Americas) 
    * Community Meeting: 15 August