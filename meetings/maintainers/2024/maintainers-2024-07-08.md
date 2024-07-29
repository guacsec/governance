
# GUAC Maintainers Meeting: 2024-07-08

Recording URL: https://youtu.be/UGAULQiTbWk

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Soham Arora | arora106@purdue.edu | Purdue | he/him
| Brandon Lum | lumb@google.com | Google | he/him

## Agenda

* [parth] Is https://github.com/guacsec/guac/issues/1734 still needed or is it superseded by https://github.com/guacsec/guac/issues/1952?
    * GraphQL is hard to use - is there a way to make usability easier?
    * Get user requests and figure out what’s a good next step to create better UX
    * Design a user focus group session
    * Who are the users
        * MS, RH, Guidewire (not the target)
        * Other new users (target, fresh set of eyes)
            * Nisha
            * (find more)
    * High level things
        * Make it clear that there are no presumptions, what do you want to see
        * What are the things you are trying to achieve
    * Experiment design
        * Target: New users that do not have a deep understanding of GUAC
        * Pre-requisites: Read the landing page of GUAC
        * Questions:
            * What 
* Chat through what is required for 1.0 and start to measure that in github project
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
        * Having issues with utilizing pubsub with document blobs since they all have limited size, using gocloud library to abstract it away for blob store.
            * Folks have asked can we use other pubsub besides NATS like kafka (gocloud can allow this flexibility)
        * Doing something  akin to case study with an end user as an acceptable criteria for 1.0 
        * Create stages for REST API stability (alpha, beta, v1, etc.)
        * Resolve IsDependency GraphQL issue (pkgName or pkgVersion mapping) - change to only pkgVersion -> pkgVersion isDep
        * Figure out and implement a collectsub stability story (lossy, temporal, playbook to fill gaps)
        * ~~Authn/Authz on 1.0?~~
            * Authz is complicated for graphql
            * A lot of it are paid solutions
            * REST API not tied to 1.0, but likely done before 1.0
        * Raising the bar on API changes as we approach 1.0
        * Collectsubscriber may need to be re-architeching 
    * From milestone
        * API stability 
            * track based on days since API change, and when that hits 3 months without a change, we can consider it stable for a v1.0 release
        * At least 1 supported and recommended persistent and optimized, backend
            * Tested on small, medium, large datasets on some standardized hardware
            * track performance on highly used queries (TBD) and determine the acceptable time to completion
        * Upgrade path to 2.0 when it is out (how to get the data out to a 2.0 instance)
        * Ingestors - EITHER OR
            * Have a test suite for X documents that are generated from Y tooling/pipelines
            * Solve the NATS issue where we would have a centralized ingestor
        * Some set of use cases satisfied (TBD)
