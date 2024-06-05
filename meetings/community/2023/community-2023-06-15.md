# GUAC Community Meeting: 2023-06-15

Recording: https://www.youtube.com/watch?v=qsURRAK3d8s

## Attendees

* Jeff Mendoza (Kusari)
* Dan Perry (Google)
* Tim Miller (Kusari)
* Mike Lieberman (Kusari)
* John Kjell (VMware)
* Dejan Bosanac (Red Hat)
* Parth Patel (Kusari)
* Marcela Melara (Intel)
* John Andersen (Intel)
* Nick Vidal (ClearlyDefined, Open Source Initiative)
* Jacques Chester (independent)
* Sunny Yip (Kusari)
* Jesse White (independent)

## Agenda

* Introductions and welcome members!
    * Nick Vidal - ClearlyDefined community manager
        * Part of OSI, looking to see how can work together
    * Dan Perry - looking to contribute, docs mostly
    * John Andersen - looking to engage, works with Marcela
* General Project Updates
    * [Mike Lieberman] - Submission to OpenSSF
* [ArangoDB](https://github.com/arangodb/arangodb) work [Parth]
* [Ent](https://github.com/ent/ent) / SQL DB work [Jeff]
* Product identifiers question [Dejan]
* S3 collector update [Dejan]
* Docs - where can i support to get started?
    * (Tim M) - The doc site is here if you’d like to take a look:  https://docs.guac.sh/
* How do I get events on GUAC
    * Tightly coupled, part of GUAC: collector-subscriber interface, current certifiers and collectors use this (OSV, deps.dev, etc.)
    * Loosely coupled: not yet, looking to design and figure out how to integrate with “cloud event” type things, cdevents, etc. https://github.com/guacsec/guac/issues/460 
* Any community experts in graph databases, or similar technologies?