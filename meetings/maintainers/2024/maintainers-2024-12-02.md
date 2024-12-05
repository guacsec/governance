# GUAC Maintainers Meeting: 2024-12-02

Recording: https://youtu.be/-e5xLAOONA0

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari |he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him

## Agenda

* Guac v2.0 feedback (from dejan)
    * Lessons learned
        * Wanted to start of as a SBOM graph db
        * They started with a POC with neo4j and the project pivoted from graph DB to graphql api, and defining ontology
        * This put things in a bad spot, since it was trying to productize things that was in a POC state.
        * At that point, no search capabilities, just basic ontology, querying was hard
        * Needed some other services which couldn’t get from guac such as:
            * Searching, full text search
            * Had to convert between many systems and interfaces
            * Internal things written in rust, managing microservices, etc.
            * There was a lot of internal conversation about how to proceed since there were a lot of struggle with infrastructure, (fighting with infrastructure, etc.)
            * Team decided to rewrite everything from scratch, instead of using microservices arch
            * Want to use postgres, and model it to do what we need
            * Wanted to start with guac schema, but was easier to just recreate their own schema
        * Parth: Developer experience is also something that we’d need to consider
        * Mike: feedback is that people are still elementary with SBOM, just want the sbom store
    * Demo from dejan
    * Wasn’t any DB implementation initially, which was hard
    * No full text search  / query
    * Couple missing things from ontology
        * Not only purls, a lot of CPEs need to be handled for products
        * Advisories can be pretty vague, they can only talk about a product. Advisory is a living object, evolves over time.
    * Brandon:
        * Seems like the need to have a 2 stage data model, one for events and things that come in and one which aggregates (e.g. for advisory)
        * The UI makes orchestration of the system very easy, we should make it such that what the community builds - e.g. a OCI collector to be an easy inclusion in that list of importers.
    * Mike:
        * Having a staged analysis is useful , doing more with less.
    * Dejan:
        * One colleague played with graph analysis to create an on demand graph in memory. His initial report says it worked pretty well for large SBOMs, or 1000s of SBOMs.