# GUAC Community Meeting: 2023-10-19

Recording: https://www.youtube.com/watch?v=cQMT9G-bZd0

## Attendees

* Parth Patel (Kusari)
* Nathan Naveen (Kusari)
* Kevin Conner (independent)
* Shafee Ahmed (Kusari)
* Mike Lieberman (Kusari)
* Marco Rizzi (Red Hat)
* Phil Cattanach (Red Hat)
* Massimiliano (Max) Dessì (Red Hat)
* Tim Miller (Kusari)
* Naveen Srinivasan
* Jeff Mendoza (Kusari)
* Sunny Yip (Kusari)
* John Kjell (TestifySec)
* Marcela Melara (Intel)

## Agenda

* Introductions and welcome members!
    * Marcela (intel) - research
* OpenSSF Incubation (Mike)
    * OpenSSF Zoom, new community meeting notes
    * Paperwork still needs to be signed
    * Neutral governance
    * Funding and support from the OpenSSF
    * Working with other projects within the OpenSSF
* Inmem Key/Value store changes/demo (Jeff)
    * Can we use that implementation and store that on disk
    * Issue: https://github.com/guacsec/guac/issues/1406
    * Interface implementation - swappable with other
    * Question: do keys not need pagination?
        * Yes, that will be added.
    * Testing with Redis, bblot
    * A disadvantage is that this is not a full-fledged database. We do not get the benefits of querying and traversal..etc.
* Updates on Ent (Marco)
    * All the queries and ingestion for software trie and evidence trie are implemented!
    * Path, nodes, and neighbors query WIP
    * Optimization phase after that
* Updates on Arango (Parth)