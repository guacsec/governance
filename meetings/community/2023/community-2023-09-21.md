# GUAC Community Meeting: 2023-09-21

Recording: https://www.youtube.com/watch?v=gKpt0iw_Inc

## Attendees

* Parth Patel (Kusari)
* Brandon Lum (Google)
* Dejan Bosanac (Red Hat)
* John Kjell (TestifySec)
* Jeff Mendoza (Kusari)
* Shafee Ahmed (Kusari)
* Nathan Naveen (Kusari)
* Tim Miller (Kusari)
* (Max) Massimiliano Dessì (Red Hat)
* Marco Rizzi (Red Hat)
* Ridwan Hoq (Microsoft)
* Toddy (Microsoft)
* Jeremy Rickard (Microsoft)
* Sajay Antony
* Marco Deicas (Google)

## Agenda

* Introductions and welcome members!
    * Andre, works with Ridwan on container registry
    * Marco D, works with Brandon on GUAC
    * Nathan, intern at Kusari, working on GUAC
    * Toddy, works with Ridwan and Andre on Azure container registry
    * Max, works with Dejan and Marco R
* Guac-ai-mole demo!! 
    * https://github.com/sozercan/guac-ai-mole 
    * UI to query GraphQL api using LLM
    * Sample questions: “What are the deps of x?”
    * “Which images contain vuln id x?”
    * Can shell out to kubectl to see what is running in a cluster, and cross reference with guac output
    * Put whole GQL schema from GUAC into LLM
    * Reference the runtime info from call out to a kubectl command to the cluster
* OCI registry collector demo 
    * Today GUAC support colelcting from single OCI repo, however, only support “registry fallback” artifacts
    * Should look towards using OCI referrer artifacts to allow an artifact to be attached to another one.
    * New command “guacone collect registry” Ingests sboms across the entire registry
    * Dev feedback: Need to read the makefile to get up and running locally
         * Have a contributor guide
         * Guide to dev-loop, what to have running 
         * Postgres was running locally, but not being used
         * What is the difference between guacollect and guacone collect
* OpenVex demo (Nathan/Parth)
* Recognizing contributors
    * Marco R
    * Soham
    * https://github.com/guacsec/guac/blob/main/CONTRIBUTING.md#contributor-ladder 
* CDX VEX implementation question (if time)
    * Currently “CertifyVEX” points to a “package-version”
    * CDX VEX uses version ranges, may not be a specific “package-version” in GUAC to point to
    * We can change “CertifyVEX” to also point to a “package-name” optionally
    * It will need to include a “VersionRange”.
    * What to do about multiple “VersionRange”s, a list? Or multiple “CertifyVEX” nodes?
    * Clients will need to map version range in CertifyVEX to specific versions of a package
* Base images - Dejan (if time)
    * Anyone have any experience providing container images for a project with multiple base images?
    * alpine/ubi/wolfi, etc. 
* Should we have snapshots between releases?
    * What about patch releases?
    * Should have something that is lower effort - not guaranteed to be stable
    * Have nightly now
    * Jeff to create issue
* Understanding plans to enforce authenticity of calls like certify. [sajay]
    * API/CLI can “certify” a package, what is the authenticity?
    * https://github.com/guacsec/guac/issues/75