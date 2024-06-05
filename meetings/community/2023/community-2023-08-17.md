# GUAC Community Meeting: 2023-08-17

Recording: https://www.youtube.com/watch?v=MUXXWAVGUDI

## Attendees

* Parth Patel (Kusari)
* Brandon Lum (Google)
* Jon Zeolla (Seiso)
* Mike Lieberman (Kusari)
* Dejan Bosanac (Red Hat)
* Jeff Mendoza (Kusari)
* Sunny Yip (Kusari)
* Noah Spahn (Open University)
* Tom Hennen (Google)
* Shripad Nadgowda (Intel)
* Bob McWhirter (Red Hat)

## Agenda

* Introductions and welcome members!
    * Noah - security researcher with open university, work at research lab at UCSB, has been looking at GUAC for a bit
    * Ivan Vanderbyl - working on ent backend for postgres SQL
    * Tom - TL for couple SSCI things in Google
* Announce new maintainer: Jeff Mendoza (Kusari)
    * Info on legal information design: https://github.com/guacsec/guac/issues/1014 
* Updates of graphQL API
    * Vulnerability changes (Parth)
        * https://github.com/guacsec/guac/pull/1147 
    * WIP - Quick update on plans to only return IDs for ingestion (Parth)
        * https://github.com/guacsec/guac/issues/1116	
    * WIP - Quick update on plans to add vulnerability metadata/score
        * https://github.com/guacsec/guac/issues/1072 
    * isDependency changes (Brandon)
        * https://github.com/guacsec/guac/pull/1125 
* Show Patch Planning demo (Brandon)
* Visualizer updates (Shafee)
* Storing signatures (Bob/Dejan)
    * https://github.com/guacsec/guac/issues/75
    * Like collectors/certifiers for documents
    * Want to store signature nodes inside GUAC as well
    * https://github.com/guacsec/guac/blob/main/pkg/assembler/graphql/schema/metadata.graphql 
* Compressed files support (Dejan)
    * S3 collector in rust gets file from s3 and puts it in NATS
    * Nice to have interface to ingestor to be raw bytes since other languages have 
    * Add processor for compressed
