# GUAC Maintainers Meeting: 2025-04-14

Recording: https://youtu.be/1xDrsWon97Y

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him

## Agenda

* (Ben) [Community Meeting](https://docs.google.com/document/d/1ImSlr_t3WNZ3zWqpmfqkw1mi6_nkv3enkQ7snWDomKA/edit?tab=t.0#heading=h.pgycmargwoj2) is Thursday!
* (Ben) Status update on 1.0 messaging
    * In progress, should have something to show later this week
* (Brandon) [1.0 technical overview](https://docs.google.com/document/d/1bjkxGu1YcMurav5DU-imoKfEN2j-LuNQJFOa__A-m0I/edit?tab=t.0#heading=h.8omn951z7ln6)
* (All) GUAC/OpenSSF Community discussions
    * Initial discussions
        * Define the new evolved community as it will exist in OpenSSF with the aim to create a larger community towards solving "Supply Chain Knowledge Graph" problems (consumption of SSCI metadata at scale).
        * The long term goal for this community is to ensure **alignment and interoperability** in solving "Supply Chain Knowledge Graph" problems through **shared architecture, methodologies, data models and standards.**
        * The GUAC project and Trustification projects "as is" today, will remain separate projects aimed at different users, but should in the long term adopt compatible standards and interfaces developed by the group
    * Good feedback on
        * Better tooling for collecting, parsing, ingesting supply chain metadata
        * Mike: Having a “generic” data model that can be used in multiple contexts can be useful
            * Graph itself may not be as relevant today compared to more simple understanding of metadata directly
            * A lot of projects is unfamiliar with knowing how to parse an SBOM, a lot of folks fork GUAC parsers since its useful but doesn’t directly meet their use cases
            * Different uses
                * A lot of tooling that look at individual SBOMs
                    * OSV-scanner
                    * Bomctl
                * Across multiple SBOMs
                    * GUAC
                    * Trustification
                * Across years of data or 100s of projects 
                    * GUAC
                    * Trustification
            * How do we make it simpler?
            * Should tooling for individual metadata scanners be part of community as well?
                * Mike: Yes. Modeled around “how should we view the supply chain”.
                * Folks need to know “how do i do this with 10 SBOMs” vs “1000 SBOMs”. 
                    * Bomctl has some stuff that overlaps with larger supply chain (e.g. augment SBOM) 
        * Dejan: Having a good home for shared libraries (via a registry?)
            * Libraries are all over the place
                * Mike: some of the parsers guac has should be able to be lifted to a library
                * With a standard data model, make it easier to consume across different tooling
            * Maintain list of “good” libraries 
            * Maintain a list of “good resources”
        * Dejan: RH folks are all enthusiastic about donation of trustification to the GUAC community.
        * Next meeting: get some proposals on the table for the next GUAC maintainers meeting
* (All) Kubecon takeaways
