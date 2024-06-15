#GUAC Community Meeting: 2024-04-24

Recording: https://youtu.be/KLrTDIkb4to

## Attendees

* Mike Lieberman (Kusari)
* Parth Patel (Kusari)
* Alex Feng (Microsoft)
* Brandon Lum (Google)
* Marco Deicas (Google) 
* Narsa Chelluri (Kusari)
* Tim Miller (Kusari)
* Jeff Mendoza (Kusari)
* Arnav Joshi (Akamai)
* Casey Fahey (NetGoalie)
* Ridwan Hoq (Microsoft)
* Yotam Perkal (Rezilion)
* Brandon Whitfield (Kusari)
* Sunny Yip (Kusari)
* Ed Snible (IBM)
* Nathan Naveen (Kusari)

## Agenda

* Introductions and welcome members!
    * Arnav here as an observer
        * Welcome Arnav!!
    * Yotam - research for startup in israel called Rezilion, tricky time for meeting
        * Welcome Yotam!!
* [Brandon] SBOMs and SLSA talk (from Kubecon)
    * [Lessons Learned from Generating 100M SBOMs: Google’s Approach to SBOM Compliance](https://youtu.be/ZYsUbN6oT7Q)
    * https://static.sched.com/hosted_files/kccnceu2024/1c/KubeCon%20EU%202024_%20Lessons%20Learned%20from%20Generating%20100m%20SBOMs%20%281%29.pdf
    * Questions on intoto attestations passed alongside sboms to add additional information
* [Parth] Fully functionality via ENT(running the guac demos)
    * Ent/Postgres is complete
    * About ready to do a release as fully supported
    * Demo of docs examples all working on ent
* [Parth] Pagination Demo for ENT and InMem
    * Queries return a “list” object that contains objects with “cursor” and “node”
    * Pageinfo object will have end cursor and next page bool
    * SBOMS > 50MB cause problems with postgres, but GUAC will handle it
    * Total count is number of all nodes that meet the filter
    * Are any queries particularly slow?
        * SBOMs are large, but not otherwise
    * List queries are being created separately to not break current integrations 
        * When all list queries are done, we will break and change the api and replace the current queries with the paginated ones
* [Marco] Transitive dependencies endpoint demo 
    * Added to REST api to traverse graph and return all transitive deps of a given package
    * Demo:
        * run graphql and rest api
        * Ingest some sboms - sandwich
        * Get /query/dependencies endpoint - give purl query param
        * Get the components
        * Bread has its own sbom - ingest that
        * Contains flour and nuts, these were not shown in original query
        * Now run original, and see nuts
        * Can also search by digest instead of purl
        * linkCondition specifies what relationships to observe between nouns
            * Name to assume packages with same name are equal
            * Digest to only search if artifact digests are the same
* Would it make sense to try both name and digest traversals at the same time?
    * Depends on way hassbom is attached to pkg or artifact
    * May be tricky
* Does spdx provide digest for top-level package being described?
    * Syft is not filling this out - all zeros - https://github.com/anchore/syft/issues/1256
    * New minimal elements may? Require this
    * We do need this data
    * Currently hassbom is only being attached to package, even if we have digest for subject