# GUAC Maintainers Meeting: 2024-08-05

Recording: https://youtu.be/TOUnHyIpa80

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him

## Agenda

* Community meeting this week
    * Demo SBOM latest and vuln retrieval https://github.com/guacsec/guac/pull/2064 (Nathan)
    * Demo ClearlyDefined integration (Jeff/Parth)
    * User Journey interviews and looking for participation (Abhisekh / Brandon+Ben backup)
    * Shout out on new contributor ladder (Ben)
    * Breaking change in Ent databases (https://github.com/pxp928/guac-update-db)
        * If re-ingesting an existing SBOM
    * What are users expecting for ingestion time?
* Requirements for v1.0 release - open conversation about https://github.com/guacsec/guac/issues/1436
    * Persistent, can handle large inputs and well tested
        * What is a acceptance criteria (How big, could be informed by user studies, both new and existing)
        * Test that criteria
    * Having issues with utilizing pubsub with document blobs since they all have limited size, using gocloud library to abstract it away for blob store.
        * Folks have asked can we use other pubsub besides NATS like kafka (gocloud can allow this flexibility)
    * Doing something  akin to case study with an end user as an acceptable criteria for 1.0
        * E.g. nisha
        * Brandon Lum to reach out to Abhishek Reddypalle to figure out the questions
    * Resolve IsDependency GraphQL issue (pkgName or pkgVersion mapping) - change to only pkgVersion -> pkgVersion isDep
    * Figure out and implement a collectsub stability story (lossy, temporal, playbook to fill gaps)
        * Collectsubscriber may need to be re-architected 
    * Raising the bar on API changes as we approach 1.0
        * Defining process for API stability
            * Create stages for REST API stability (alpha, beta, v1, etc.) - Marco Deicas will look at this! (and create a PR)
        * Create a release candidate for the API and see if they meet user requirements and case studies (for X weeks)
        * Check against backward compatibility and how they move with version upgrades (What version changes and schema changes result in different actions by users) jeff@kusari.dev
            * Graphql client issue is actually a bug in the generator??
            * What is the deployment upgrade story