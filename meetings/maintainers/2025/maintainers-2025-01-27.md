# GUAC Maintainers Meeting: 2025-01-27

Recording: https://youtu.be/NR2SZQ9zi40

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
| Damian Vicino | damian.vicino@datadoghq.com | DataDog | he/him

## Agenda

* Microsoft Meeting
    * Brandon met with Alex and Robbie
    * Build SBOM - associate SBOM with image, image mirrored across registries
    * Cannot plug into mirror service
    *  OCI collector to get more information about this
    * How to communicate this information?
        * Image association
        * SBOM association
        * SBOM association attestation (in-toto attestations)
    * Certifier to create this predicates for us
    * OCI registry certifier - 
        * Generate a attestation URI points to this Hash
            * IsOccurance (URI points to this Hash) and HasMetadata (this information was found via crawling the registry - customer facing, internal image…etc)
    * (Not for 1.0) Need generic attestation ingestion such that we do not need to re-compile or keep supporting new predicate types
        * Where do we store unknown attestations?
            * Create and send to archive queue
            * Store into hasMetadata
* 1.0 discussion
    * Csub will not be 1.0, eventually rearchitected to a pubsub queue, etc.
        * Remove CSUB, deps.dev collector from docker-compose
        * Updates to the demos that rely on some deps.dev data (mostly around the patch planning)
        * Clean out all non supported backends (neo4j, neptune, and arangodb)
        * Create a tag to archive the backends