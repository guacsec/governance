# GUAC Maintainers Meeting: 2025-03-03

Recording: https://youtu.be/RYdB_w65Yv0

## Attendees

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Brandt Keller | brandt.keller@defenseunicorns.com | Defense Unicorns | he/him
| James Fuller | jfuller@redhat.com | Red Hat | he/him
| Eddie Knight | knight@linux.com | Sonatype | he/him

## Agenda

* Welcome new friends
    * James Fuller from Trustify team, want to chat about v2 plans
        * Principal engineer at RH product security, been with trustify team for past 6 months
    * Brandt (defense unicorns)
        * Revisiting past topics on airgapped integrations
* Eddie Knight: tooling for evaluating OSPS Baseline compliance
    * Working on SARIF format
    * Open issue to evaluate guac repo (only main guac repo): https://github.com/guacsec/guac/issues/2526
* Brandt
    * Looking to do a CFP for openssf community days
    & Will post an issue in the guac issues
* James
    * Looking at software metadata
    * Now more than just software transitive dependencies, but how they were created
        * Source>binary rpms
        * Imageindex> image
        * Product>component
        * Upstream
        * How it was built, etc. 
    * Approach, usually start with SQL databases, and start looking into the graph structure
    * The most recent iteration that product security wrote was designed to have a graph databases
    * Worked at DB company for 15 years, most of the core team moved to AWS neptune
    * People use a graph database and have unpredictable performance
    * The one graph index puts complexity into queries (not creating more indexes)
    * The idea with last iteration was to be multimodal
        * Represent tree data structures using graphs
        * A lot on entity data that lives in tables and represent other data that is graph like in a graph
        * For rust, use petgraph (https://docs.rs/petgraph/latest/petgraph/) 
        * Don’t need a full blown graph database, whenever we get an SBOM we never touch it again
        * Mutate/Delete of nodes in a graph database are costly
        * Operational petgraph - if you want to do historical analysis, that’s not the place to do it
        * Separate the runtime operations vs “something else”. AWS neptune has a connector, but can store TBs of stuff in there.
        * [Falkor DB](https://www.falkordb.com/), has bitmaps and are stable
        * Old system (not trustify) has ~10 M sboms in it and 20M components in the SBOMs
            * Postgres is ~1TB after 2 years
        * Context of multiple purls/identifier in multiple SBOMs have to be teased out
        * Source binary relationships, SBOMs (dependencies), and image index in containers
        * The other challenge is operationally, *multiple truth approach*
        * Hard usability problem around which to trust
        * Usability problems
            * False positives and explaining those
        * Data goes in, goes into postgres tables and the graph (the graph is based on the postgres data)
            * Each graph is scoped to an SBOM
            * We shred relationships into postgres table for persistence
        * We’re talking about [trustify](https://github.com/trustification/trustify)
