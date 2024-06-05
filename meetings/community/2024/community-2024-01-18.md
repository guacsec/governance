# GUAC Community Meeting: 2024-01-18

Recording: https://youtu.be/k9Z5A90AUWQ

## Attendees

* Parth Patel (Kusari)
* Brandon Lum (Google)
* Justin Cappos (NYU)
* Jon Zeolla (Seiso)
* Marco Deicas (Google)
* Dejan Bosanac (Red Hat)
* Marco Rizzi (Red Hat)
* Max Dessì (Red Hat)
* Ridwan Hoq (Microsoft)
* Abhishek Reddypalle (Purdue University)
* Jeff Mendoza (Kusari)
* Ed Snible (IBM)

## Agenda

* Introductions and welcome members!
    * Ed - freelancer engineer, been playing around with GUAC
* LFX mentorship https://mentorship.lfx.linuxfoundation.org/project/88e6bd6c-abb1-4910-823a-8f0420fbca90 
    * Useful for new to open source or the field
    * Contributions could be anything -   docs, code, etc. 
* [marco deicas] Quick overview of REST API - https://github.com/guacsec/guac/issues/1544
    * Going to use code generator for server stubs oapicodegen
    * Schema would be  OpenAPI (previously known as swagger)
* [Parth] Custom directives for GraphQL 
    * PURL will show up now when searching for packages
        * Answer questions on what is the PURL
    * Contains/Starts with
        * Is there better way to query graphQL like a submatch like contains or start with
* [Parth] Update to Vulnerability CLI - SBOM URI 
* GUAC 0.4.0 release! All these above are included!
* PURL check update (https://github.com/guacsec/guac/issues/1545) 
* Requirements for v1.0 release - open conversation about https://github.com/guacsec/guac/issues/1436
    * Persistent, can handle large inputs and well tested
    * Having issues with utilizing pubsub with document blobs since they all have limited size, using gocloud library to abstract it away for blob store.
        * Folks have asked can we use other pubsub besides NATS like kafka (gocloud can allow this flexibility)
    * Doing something  akin to case study with an end user as an acceptable criteria for 1.0 
    * Authn/Authz on 1.0?
        * Authz is complicated for graphql
        * A lot of it are paid solutions
        * REST API not tied to 1.0, but likely done before 1.0
    * Raising the bar on API changes as we approach 1.0
* [Mike] - Very quick update on upcoming GUAC webinar
* We provided some feedback on CISA software identifier RFC (https://www.regulations.gov/comment/CISA-2023-0026-0011) 