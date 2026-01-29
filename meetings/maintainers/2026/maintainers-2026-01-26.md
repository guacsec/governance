# GUAC Maintainers Meeting: 2026-01-26

Recording: https://youtu.be/ciao_e3lB54

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ruben Romero Montes | rromerom@redhat.com | Red Hat | he/him
| Brandt Keller | brandt.keller@defenseunicorns.com | Defense Unicorns | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Michelle DiPalma | | Red Hat | she/her
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him

## Agenda/notes

* [Jens] Trustify SBOM groups feature discussion (https://github.com/guacsec/trustify/pull/2209)
    * Original idea was to group SBOMs by product, etc, but that’s complicated because what a “product” is varies from org to org
    * Taking a step back, the approach is to group in a folder-like structure
        * Different from a filesystem because an SBOM can be in zero or multiple groups
    * Initial state of existing Trustify setup is for SBOMs to be ungrouped
    * Adds granular permissions to manage groups
    * Future tasks:
        * UI
        * Postgres ltree to speed up operations 
[Dejan] [qodo.ai](http://qodo.ai) tool usage
    * Currently using [Sourcery.ai](http://Sourcery.ai) to review PRs, etc
    * Investigate [Kusari Inspector](https://www.kusari.dev/developers) as well

