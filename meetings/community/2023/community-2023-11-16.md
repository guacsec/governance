# GUAC Community Meeting: 2023-11-16

Recording not available

## Attendees

* Parth Patel (Kusari)
* Brandon Lum (Google)
* Mike Lieberman (Kusari)
* Abhishek Reddypalle (Purdue)
* Jeff Mendoza (Kusari)
* Dejan Bosanac (Red Hat)
* Ridwan Hoq (Microsoft)
* Nathan Naveen (Kusari)
* Tim Miller (Kusari)
* Sunny Yip (Kusari)
* Marco Deicas (Google) 
* Kevin Conner (Independent)
* Santiago Torres-Arias (Purdue)
* Dana Wang (OpenSSF)
* Eman Abu Ishgair (Purdue)
* Marco Rizzi (Red Hat)
* Phil Cattanach (Red Hat)
* Max Dessì (Red Hat)

## Agenda

* Introductions and welcome members!
    * Abhishek Reddypalle (Purdue) - student
    * Dana Wang (OpenSSF) - Architect for OpenSSF
    * Jennifer (Kusari)
* Show off Key/Value (redis, TiKV) (Jeff)
    * GUAC has default in-mem backend using internal golang map structs, etc.
    * Allows for plugin key/value stores
    * Demo with redis and TiKV
    * 20 lines of code to add other key/value stores
    * Try etcd next
    * Try performance query testing
* Experimental REST API demo (Nathan)
    * https://github.com/guacsec/guac/issues/1326
    * Feedback on queries, inputs and outputs
* GUAC community feedback on use cases (SBOM, metadata attachment, most critical/actionable dependencies type thing) (Brandon and Parth)
    * https://github.com/guacsec/guac/issues/1483
    * https://github.com/guacsec/guac/issues/1505
    * https://github.com/guacsec/guac/issues/1508
    * Dejan 
        * here is the sbom, give me all vulns
        * Here is vuln, what packages are affected
        * Push upstream in a few months
    * Dana
        * MVP security standards openssf is developing
* Identifier problems (RFI) discussion
    * [Problem statement](https://www.federalregister.gov/documents/2023/10/26/2023-23668/request-for-comment-on-software-identification-ecosystem-option-analysis)
    * [GUAC RFI working doc link](https://docs.google.com/document/d/1h9Ko-myqAfQc-pWlvYay0CENIDhfFHVZdxLY74Jdw9w/edit#heading=h.2l3uzjuzf7tn)
