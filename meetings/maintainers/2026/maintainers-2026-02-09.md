# GUAC Maintainers Meeting: 2026-02-09

Recording: https://youtu.be/epjgNNgAbJ0

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Brandon Lum | lumb@google.com | Google | he/him
| Ruben Romero Montes | rromerom@redhat.com | Red Hat | he/him
| Brandt Keller | brandt.keller@defenseunicorns.com | Defense Unicorns | he/him
| Michelle DiPalma | | Red Hat | she/her
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Rajan Ravi | rravi@redhat.com | Red Hat | he/him
| Gagan H R | ghr@guidewire.com | Guidewire | he/him

## Agenda/notes

* Welcome new friends
    * Gagan (Guidewire) - use GUAC to ingest SBOM for images for SBOMs 
    * Michelle - Trusted Product analyzer
    * Rajan Ravi (RedHat) - Working on Trustify
    * Ruben (Redhat) - works on dependency analytics project
    * Brandt (Defense unicorns) - works on Zarf, for airgap deployments
    * Dejan (RedHat) - works on trustify and TPA
* Triage reviews/issues requiring attention
* Brief overview of Trustify 0.5.0 roadmap
    * Planned for late April to May timeframe
    * SBOM groups - support managing products in trustify (define products and product versions and be able to group their SBOMs)
        * ADR is here (https://github.com/guacsec/trustify/blob/main/docs/adrs/00013-sbom-groups.md) 
    * Improve how to deal with advisories and information
        * Store and present CVSS scoring (support version 4)
        * Provide a better view to understand vulns
    * AI
        * Include AI Boms (CDX 1.6)
        * How to manage external references
        * AI Boms may be mutable??
        * CBOMs being talked about due to PQC
        * Reporting incidents against AI Boms (still a bit further away)
* [Brandt] Advocate for any assistance required for getting open PR’s merge-ready
    * Testing and blockers?
    * Brandon Lum to set up some time with Gagan + 1 maintainer to get through the PRs to fix CI and work on Brandt’s 2 PRs
    * Brandon Lum set up a systems for each meeting in agenda to go through to review PRs
* [Gagan] Improvements to scorecard certifier in GUAC, need reviews on this PR
    * https://github.com/guacsec/guac/pull/2815 needs review
    * https://github.com/guacsec/helm-charts/pull/74 needs review
    * PR in the GUAC helm chart to add support to common labels
