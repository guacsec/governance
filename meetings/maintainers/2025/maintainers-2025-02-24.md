# GUAC Maintainers Meeting: 2025-02-24

Recording: https://youtu.be/odzeHsqTGac

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Anirudh Edpuganti | | Guidewire | 

## Agenda

* Folks still trickling into the GUAC channel
* Mihai had a chat with Parth on GUAC, follow up conversations from sigstore con
* Mike: Can we pull in the folks from HPE to chat a bit more about how they are using GUAC. At the community meeting, someone from HPE was using GUAC internally to understand their license risk. They were using GUAC + Clearly defined integration. 
    * One of the things they’d like is to create a “NEW” sbom - maybe corrections, fixes, etc.
    * How do you collect up a group of nodes and make an SBOM out of it
    * Completeness is important because for legal use case, lawyers are looking at the entire view. (almost like a spreadsheet)
    * Only things that are linked to the lifecycle of an artifact (things that don’t change)
    * SBOM generation would not be part of GUAC core but as an adjacent helper tool to export it to SBOM format
* Update on proposed changes to OCI collector
* “Aggregate” tables