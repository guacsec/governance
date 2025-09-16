# GUAC Maintainers Meeting: 2025-09-15

Recording: https://youtu.be/kotNCDe10f8

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Petr Toman | ptoman@redhat.com | Red Hat | he/him
| Ruben Romero Montes | rromerom@redhat.com | Red Hat | he/him
| Pavel Sedlak | psedlak@redhat.com | Red Hat | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him

## Agenda/notes

* [SBOM minimum elements](https://www.cisa.gov/resources-tools/resources/2025-minimum-elements-software-bill-materials-sbom) response from GUAC community
    * Held back information - how to encode
    * Distribution - making it sharable
    * Hash information is important
        * Opinionated hashes for matching
    * License is good
    * Tool name is important
    * Generation context
    * Version as hash
        * Container images
        * Considering the date, wouldn’t be enough
        * Clarify the purpose of the hash, checksum of the content vs identifier
            * E.g. for OCI images, by content
    * Depth of major version update
        * Indirect, direct or unknown
    * Timestamp - separate timestamp from the content
        * If the content is the same, what is the timeline
        * Have a timestamp envelope with the content, so that it makes it easier to compare the data in them.
        * Timestamps are still important
        * Maybe an attestation on what is the “best goto SBOM”
    * If uploading an sbom that is already there, for an artifact with a certain commit or hash, regardless of timestamp, you should not be able to replace it by something newer. 
    * Having a history of dependencies over time, even for unreleased artifacts are useful (internally for trend detection)
* Trustify migration status
    * In a good place for important repos are there, things are working normally and enabled most of the bots
    * Currently created one team with active committers, and start proper governance
    * Next is to tackle dependency analytics 
    * Utility repos
