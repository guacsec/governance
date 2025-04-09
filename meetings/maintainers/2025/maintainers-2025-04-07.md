# GUAC Maintainers Meeting: 2025-04-07

Recording: https://www.youtube.com/watch?v=aBQnIaQQss4

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him

## Agenda

* Community aspects with trustification
    * Everyone is super on board with having a joint community, having related projects converging and solving the similar problem in the same aspects.
    * Let’s set up a meeting to have initial discussions
* What is 1.0? Who is it for and what's our messaging?
* For versioning
    * Should be in lockstep (as far as this client bug is still present)
    * Jeff did some of the graphQL stuff in python, and for that and other languages, any additions SHOULDN’T be a breaking change…
    * Tying the GUAC version to semver for 
        * Minor version will be addition of backward compatible fields and nodes
        * Major version will be removal of fields, rename or change type or semantics. 
        * Behavioral change in resolvers
            * If minor bug, minor version.
            * If change the way retrieval is done, ordering invariants, which will result in different user behavior.
        * Backends will follow graphQL rules as well
* Feedback from MS on API
    * They write their own backend and have their own API versioning, they would need to be able to import the newest GUAC as a library (requiring backward compatibility with their backend implementation)
        * i.e. they would want library updates but their implemented graphQL version may not include new features
        * One proposal was to add a GetBackendApiVersion to the backend, so even if they import the new library, they can say that they only implement a subset of the features (i.e. use v.1.2 for the library for GetBackendApiVersion returns “v1.1” which will be used for documentation of graphql API)
            * Should pair with some conformance testing
            * Mapping of backend versions to GQL versions will need to be shipped with releases
        * The upgrades may not make sense since some of them may require major version feature changes. Thus will create complications with the support of the upgrades… 
        * We could keep a community maintained backport branch, maintainers will help validate PRs that go onto that branch