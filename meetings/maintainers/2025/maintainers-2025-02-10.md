# GUAC Maintainers Meeting: 2025-02-10

Recording: https://youtu.be/RcAvmGiOVyU

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him

## Agenda

* [Ben] Followup: Work with Minder team to evaluate GUAC against OpenSSF Baseline?
    * If no one from Minder is able to attend today, let’s collect our questions and I’ll get those worked on asynchronously
    * Action: Ben to create a doc to collect questions
* [Ben] Any updates for the Supply Chain Integrity WG quarterly update?
    * List recent releases, including EOL certifier, OCI collector, OTel support, Datadog malicious packages certifier
    * Mention KubeCon keynote references
    * Include 2024 in review post
    * Upcoming: still working toward a 1.0 release and a rearchitecture
* [Ben] Meeting next week? (U.S. President’s Day holiday)
    * Agreed: no meeting next week
    * Action: Ben to coordinate with OpenSSF Ops
* [Jeff] Staff is asking for projects to submit to https://events.linuxfoundation.org/openssf-community-day-north-america/
    * June 26, 2025 Denver, Colorado
    * CfP closes March 23 (for Open Source Summit NA, it’s Feb 15)
* Trustify schema discussion
    * Brandon was curious about relationships like “variant of”. Wanted to understand better where those relationships come from and what’s the mapping from what’s in the SBOM to what the variants are.
        * Dejan can invite the colleague who did a lot of the relationship work to join the meeting in two weeks.
        * Trustify is using OSV as a data service. Packages are transformed to a pURL. Affected package ranges have a type and events: introduced and fixed.
        * In the database, there are relations to three tables: base_purl, qualified_purl, versioned_purl. version_range table includes low_ and high_ version and whether or not the bounds are inclusive.
        * Q: Are versions always in SemVer?
            * A: no, it supports a variety of version schemas
    * Divided entities of vulnerability and advisory for the vulnerability. Vulnerability is the ID (e.g. CVE) which could have multiple advisories (e.g. GHSA and RHSA). All of these can be linked to purl_status. From a vulnerability, you can go through the qualified_purl to find the base_purl and get the status.
        * Q: Would this handle the case of a vulnerability having two version ranges?
            * Yes
        * Q: What happens if the version range is open?
            * It should match
* Trustify CPE matching
    * product_status table has a package field
    * Instead of a pURL, Red Hat’s advisories often have a component name
    * Very crude logic to match what’s reported in the advisory to what’s listed in the SBOM
* Going from data files to OSV as a service
    * Even a small set of SBOMs could result in many pURLs, which can overwhelm OSV
    * Pulling data files can result in stale data
* Next time:
    * Talking through the graph
    * How updates to the database are handled
