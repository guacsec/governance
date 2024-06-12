# GUAC Maintainers Meeting: 2024-06-10

Recording: https://youtu.be/qp1EwXQXXcM

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Marco Rizzi | mrizzi@redhat.com | Red Hat | he/him
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Narsa Chelluri | narsa@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Reden Martinez | rmartinez@linuxfoundation.org | Linux Foundation | he/him
| Karla Obermeier

## Agenda
* [bcotton] Contributor ladder amendments [governance#8](https://github.com/guacsec/governance/issues/8)/[guac#1935](https://github.com/guacsec/guac/pull/1935)
    * Actions: maintainers to review
* [bcotton] Can we put some love into the roadmap [milestones](https://github.com/guacsec/guac/milestones) (particularly around what’s needed for 1.0)?
    * Mrizzi is interested in this, RedHat is using GUAC in a project, waiting on v1.0 (using a fork of an old version for stability for now, plan to upstream)
    * 1.0 Discussion (based on milestone text)
        * API stability 
            * track based on days since API change, and when that hits 3 months without a change, we can consider it stable for a v1.0 release
            * UX around REST API vs GQL
        * how do we delete stuff? 
            * Accidentally put information in
            * Churn of predicates over time (OSV certifier)
            * Delete old builds over time (retention policy)
                * What is the motivation? Data and compliance policy vs ease of use / performance / growth concerns 
                * (seems like more of UX/growth concerns)
        * GOOD ON THIS - At least 1 supported and recommended persistent and optimized, backend
            * Tested on small, medium, large datasets on some standardized hardware
            * track performance on highly used queries (TBD) and determine the acceptable time to completion
        * Ingestors - EITHER OR
            * Have a test suite for X documents that are generated from Y tooling/pipelines
                * We support X document Specs 
                * We’ve run this on Y tools, as an ADOPTERS.md type file
            * Solve the NATS issue where we would have a centralized ingestor
        * Some set of use cases satisfied (TBD)
        * Upgrade path to 2.0 when it is out (how to get the data out to a 2.0 instance)
* [Mike] REST API from GraphQL (https://github.com/Urigo/sofa) (https://the-guild.dev/graphql/sofa-api) 
    * Async API is probably not suitable (unified way to handle other type of event based APIs), seems not to be mature enough for what we need
    * Some folks want to not want to dive too deep into GraphQL, sofa provides a way to translate graphQL to rest API
    * May be a good thing for contrib type repo
    * For prod usecases, simple queries on gql api would not be sufficient, simple rest apis queries would not suffice, so more complex queries should still go into the REST API
    * Should be READ only,  should not do mutation
    * Need to make sure contrib like visualizer must stay in sync with GQL API
    * Mike to create the issue on this 
* [parth] https://github.com/guacsec/guac/issues/1947 discussion 
    * Diamond dependencies… ahhhh!!
    * Scorecard API only has top X repositories. Still have some usecases around private repos and not top repos
    * The proposal from nathan only says delete the code, contrib repo would be good to move this to. 
    * We’re getting a lot of scorecard information from deps.dev
    * Replied to https://github.com/guacsec/guac/issues/1947
* [parth] Deletion of nodes discussion [low priority] 
    * Context around OSV certifier, keep on creating certifyVuln nodes, keep creating things, might need to handle to prevent churn in unused nodes.

## Opens (pending)
* [parth] Deletion of nodes discussion [low priority] 
    * Context around OSV certifier, keep on creating certifyVuln nodes, keep creating things, might need to handle to prevent churn in unused nodes.
