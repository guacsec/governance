# GUAC Maintainers Meeting: 2024-10-07

Recording: https://youtu.be/tFj5iu8hqrQ

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him

* Regrets
    * Jeff: I have a conflicting meeting once a month now.

## Agenda
* Deps.dev on ingestion semantics and code drift
    * HasSBOM in IngestPredicates should not be a list due to the processing of included deps/artifacts done as part of assembler (create an issue)
    * To enable patch planning - Ingest only deps.dev packages when the user queries for them…(data on demand)
    * SBOM download during ingestion would be too inefficient
    * Scorecard? Just query scorecard and hasSource at using Deps.dev on ingestion
    * “Advanced” patch planning with deps.dev is NOT v1
* How to get around limitations of graphQL query - without creating a graphql endpoint?
    * Example - query all sboms but filter out a specific collector (not in)
    * RestAPI directly access the backend?
        * This would be dangerous, create custom endpoints for the queries that are needed (needs to be approved by the maintainers)
        * As part of the release export out the postgres schema
* Continue deletion discussion?