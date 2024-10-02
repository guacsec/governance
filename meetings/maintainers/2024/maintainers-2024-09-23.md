# GUAC Maintainers Meeting: 2024-09-23

Recording: https://youtu.be/3lRE1MpPbco

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Soham Arora | arora106@purdue.edu | Purdue |

## Agenda

* [Ben] Request to be promoted to Reviewer in Docs: https://github.com/guacsec/governance/issues/32
    * Related: Is guac-data a part of the Docs area? Ben thinks it should be
        * General consensus is: yes
* Reviews needed:
    * [Ben] Demo re-org: https://github.com/guacsec/guac-docs/pull/147
* [lumb] Gql backends usage
    * Guidewire has issues with running arango since it doesn’t support their use cases and we no longer maintain it
    * How to run this as a production thing? Helm chart and compose are helpful but no writeup on how it should be run in a prod type environment
        * How about certifiers, how do you set up ingestors, etc.
        * Would be good to have people contribute blog posts for this, as docs can get out of date quickly
    * Feedback from OSS EU: found certain things difficult to run with GUAC
        * Running demo is difficult, folks then think running in prod is difficult
        * On the docs right now, we only have the demo setup, we tried to make the demo simpler by taking out the ingestor/nats portions of it, we don’t currently have a replacement for that more detailed deployment tutorial
            * We should have a non-demo compose guide - with ingestor/nats/blob
            * More filled up description of what each binary does
            * Guide for starting up a helm chart
    * Should we remove all other backends and just offer one
        * Some of the stuff is in GUAC is too complicated
            * Folks are given too many options
        * REST API can be the mainly exposed endpoint to most people
        * GraphQL is the “advanced” mode, we expect only a small number of users to be utilizing this
        * 2 ppl had said for a canned graphql query, register it with REST API, and replacement, etc.
            * The https://docs.guac.sh/guac-graphql/ guide shows using a .gql file with saved named queries and parameters.
            * Ex: `cat demo/graphql/queries.gql | gql-cli http://localhost:8080/query -o PathQ1 -V subject:5809 target:6721 | jq`
            * This is buried under “Developing tools on top of GUAC”
            * Should this be more prominent?
        * Most people have problems with interaction with the GraphQL api queries
        * Even if wrapping GraphQL with REST API, it would still expose ontology complexities
    * Mike met Alistair in europe, and mentioned that there are challenges with how graphQL and ent are set up which could impact performance and other considerations.
    * Decisions:
        * We’re deprecating all other backends, one backend to rule them all
        * Keyvalue will be testing only
* [Jeff] Discuss: https://github.com/guacsec/guac/issues/2127
    * [bug] Ingesting SBOMs results in license error
    * Some CDX SBOMs do not have license text for custom licenses
    * What should GUAC do in this case?
    * Document some of these edgecases in the graphQL documentation and rest API endpoints