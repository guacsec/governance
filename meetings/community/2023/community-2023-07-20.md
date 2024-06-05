# GUAC Community Meeting: 2023-07-20

Recording: https://www.youtube.com/watch?v=uSHrONr8U60

## Attendees

* Mike Lieberman (Kusari)
* Tim Miller (Kusari)
* Dan Perry (Google)
* Jesse White (independent)
* Will Armiros (Protect AI)
* Lindsay Newton (VMware)
* Dejan Bosanac (Red Hat)
* Parth Patel (Kusari)
* Jeff Mendoza (Kusari)
* Sunny Yip (Kusari)
* Rebecca Metzman (Google)
* Shripad Nadgowda (Intel)
* Phil Cattanach (Red Hat)
* Marco Rizzi (Red Hat)
* Brandon Lum (Google)
* Mihai Maruseac(Google)

## Agenda

* Introductions and welcome members!
    * Marco Rizzi from Red Hat
    * Phil Cattanach from Red Hat
    * Lindsay Newton from VMware
    * Amim Knabben from VMware
* Quick update on OpenSSF contribution
* Ent backend presentation (ivan)
    * Using Ent (https://entgo.io/docs/traversals/)
    * Interest in GUAC and don’t quite want to support additional tech so implementing it through ent on postgres
    * Running compose on the feature branch that sets up postgres
    * Running queries through graphQL 
    * Upserting package trees runs in a transaction - have some ideas around doing bulk upserts on the DB
    * Ent will behind the scenes generate the files
    * Ent will also do the schema stuff for you
    * Feedback/Questions
        * Awesome stuff!
        * Put questions in GUAC slack
* Friends of GUAC poll (Brandon)
    * Friends of GUAC markdown on main repo
    * Guacsec org repos with labels: 
        * Different labels
            * Community (Maintained by community)
            * Supported (Maintained by community + GUAC maintainers)
    * Questions:
         * Individual repo vs monorepo with directories
             * graphQL consistency will help with monorepos if there are issues vs repo management
    * Given a lot of GUAC right now is GraphQL API, suggestions on making API queries easier
    * Submodule may be a good way
    * Brandon to create MD file with process
* ArangoDB / Neptune Updates (Parth)
    * Ingest SBOMs, and potentially docs
    * Talk through changes / improvements from backend to get it faster
    * Added bulk ingestion - reduce round trips
    * Search function
        * Higher level CLI functions
* Tilt integration and Gremlin/Tinkerpop backend work (Jesse White) (if he can make it to the meeting)
    * Would be nice to have a conformance test suite
* Office hours time (Dejan, if there’s time)
    * Hard for some EMEA timezones to get to
    * Alternating office hours (Brandon will take this up)
* Large files support (Dejan, if there’s time)
    * Brandon: Is this related to https://github.com/guacsec/guac/issues/731? 
* Brainstorm discussion on higher level CLI (https://github.com/guacsec/guac/issues/1044) 
    * Use-cases: https://github.com/guacsec/guac/blob/main/use-cases.md
* Visualizer (shaffee, if there’s time)

