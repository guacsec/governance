# GUAC Maintainers Meeting: 2024-07-29

Recording: https://youtu.be/17CP2ubythA

## Attendees 

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Alastair Turner | alastair.turner@percona.com | Percona |
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Shreyas Pandya | spandya@guidewire.com | Guidewire | he/him
| Abhishek Reddypalle | | Purdue |

## Agenda

* Welcome new friends
    * Shreyas Pandya (Guidewire)
    * Abhishek Reddypalle - student at purdue (working with santiago and soham)
    * Alastair Turner (Percona) – DB engineer
* [Ben Cotton] Unclear licensing for GUAC Docs: [guacsec/guac-docs#136](https://github.com/guacsec/guac-docs/issues/136)
    * Leave workflow files under apache license
    * Code is under MIT
    * Content is CC-BY
* [Ben Cotton] Pending requests
    * Promote me to Owner for Web & Marketing: [guacsec/governance#15](https://github.com/guacsec/governance/issues/15)
        * N-1 maintainer votes received
        * Create groups and provide permission
            * Use Pulumi for access right groups
    * Add contributing page: guacsec/guac-landing#48
* Open questions from others on the call?
    * More information on the various binaries created by GUAC
little bit here:
        * https://github.com/guacsec/guac/blob/main/cmd/README.md
        * https://docs.guac.sh/guac-components
    * Helm support
        * https://github.com/kusaridev/helm-charts/tree/main/charts/guac
* Continue chat on requirements for GUAC v1.0 
* What does 1.0 mean?
    * You can start investing in GUAC - we’re not going to make you do something that you need to start over
        * Being able to update to later major versions via deployment without breakage
            * Database changes shouldn’t break database, only add nullable fields
            * Components need to have stable interfaces
                * Collectors
                    * -> CollectSub (relied on by OCI, Deps.dev)
                    * -> Ingestor
                * Ingestor (stable)
                    * -> Assembler
                    * -> CollectSub
                * Assembler
                    * -> GraphQL API
                * Client (not part of deployment) -stable within minor versions
                    * -> GraphQL API
                    * -> RestAPI
                * Certifier
                    * -> GraphQL API
                    * -> Ingestor
                * GraphQL API
                    * -> Backend
                    * -> User
                * Rest API - has its own lifecycle
                    * -> GraphQL
                    * -> Backend
                    * -> User
                * CollectSub
                    * -> Ingestor
        * Some things across major versions that you’d have to change (v1.2 -> 1.3) - continue discussing this
            * Across major versions
                * CLI changes
                * Minor GraphQL API changes (naming, etc.)
            * Changes required by users should be <5 mins 
            * Major version once every 6 months
            * Not supporting branched patches on old major versions
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
        * Collectsubscriber may need to be re-architeching 
    * Raising the bar on API changes as we approach 1.0
        * Defining process for API stability
            * Create stages for REST API stability (alpha, beta, v1, etc.) - Marco Deicas will look at this!
        * Create a release candidate for the API and see if they meet user requirements and case studies (for X weeks)
        * Check against backward compatibility and how they move with version upgrades (What version changes and schema changes result in different actions by users) jeff@kusari.dev
            * Graphql client issue is actually a bug in the generator??