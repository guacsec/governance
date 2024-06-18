# GUAC Maintainers Meeting: 2024-06-18

Recording: https://www.youtube.com/watch?v=Lts4NjHqKIw

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Narsa Chelluri | narsa@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Reden Martinez | rmartinez@linuxfoundation.org | Linux Foundation | he/him

## Agenda

* Welcome new friends
* Collect Opens
* Next community meeting (look at community meeting notes)
* [parth] Deps.dev not resolving properly (purl spec) [google/deps.dev#93](https://github.com/google/deps.dev/issues/93_
    * Deps.dev api purl calls its old API and so there will never be a good path
    * Issue with the PURL spec - let others say that they define how their packages work but then don’t support casing - which is opinionated.
    * If a new package ecosystem comes out - Foo vs foo
    * If PURL is a subset of RFC 39XX, and URL RFC says its case sensitive, then PURL won’t be compliant with the RFC
    * A little surprised to be case sensitive, then they are using a URL which is case insensitive.
    * Can we move case sensitive aspects to query params so that they are case sensitive? (only preserving domain as the namespace)
        * E.g. pkg:golang/github.com/pkgname&pkgPath=Go/antlr
    * Deps.dev also runs into issues with purl adoption due to this golang ecosystem issues
    * PyPI weirdness in _ vs - vs .
    * PURL spec does not fully match what the ecosystem is trying to represent
    * PkgEqual predicate will not work since the SBOM should have PURL and it would maybe eventually become lower case
    * Spec vs ecosystem vs tooling inconsistency
    * What to do?
        * Short term
            * Try and follow what the spec does in PURL v1.0 - is the library doing the canonicalization?
        * Long term
            * Find a few more folks that are having these issues
                * Writing a blog to highlight the problem (brandon, parth, santiago)
                    * > To avoid ambiguity when serving from case-insensitive file systems, the $module and $version elements are case-encoded by replacing every uppercase letter with an exclamation mark followed by the corresponding lower-case letter. This allows modules example.com/M and example.com/m to both be stored on disk, since the former is encoded as example.com/!m. this is just randomly in the go modules spec (as part of GOPROXY), not sure why it wouldn't be a good idea to use the same approach for module/package paths overall
            * Sending this out to ecosystem friends 
* [Mike] Make API docs better?
    * Does graphql have something like openapi
    * Our current stuff isn’t as simple/easy to use as Swagger/OpenAPI
    * Our current graphql setup is a few dozen files.

## Opens (pending)

* [parth] Deletion of nodes discussion [low priority] 
    * Context around OSV certifier, keep on creating certifyVuln nodes, keep creating things, might need to handle to prevent churn in unused nodes.
* [parth] Included a Handler for CycloneDX Version Ranges
    * https://github.com/guacsec/guac/pull/1789
    * Handle version range resolution without querying graphQL on ingestion