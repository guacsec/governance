# GUAC Community Meeting: 2025-01-16

Recording: https://youtu.be/ZbeDw9RAeng

## Attendees

* Ben Cotton (Kusari)
* Mihai Maruseac (Google)
* Brandon Lum (Google)
* Narsa Chelluri (Kusari)
* Jeff Mendoza (Kusari)
* Parth Patel (Kusari)
* Alex Feng (Microsoft)
* Casey Fahey (NetGoalie)
* Michael Lieberman (Kusari)

## Agenda

* Contributor ladder climbs
    * Robbie Cronin:
        * Reviewer for CLI
        * Reviewer for Collectors
    * Nathan Naveen
        * Reviewer for CLI
    * Ben Cotton
        * Owner for Docs
* Releases since the last meeting:
    * [GUAC: v0.12.0](https://guac.sh/blog/2024-12-12-guac-v0.12.0/)
        * New certifier for EOL.date (Thanks Robbie!)
        * New collector for OCI registry (Thanks Robbie!)
        * Improvements to OSV certifier
        * Deps.dev scanner on ingestion
* Cool new features
    * Datadog dataset certifier
        * https://github.com/guacsec/guac/pull/2366 
        * Brandon: this shows how simple it is to add additional certifiers for datasets. This is a nice PR to use an example if anyone wants to add a new certifier.
* Blog post on 2024 looking back
    * https://github.com/guacsec/guac-landing/issues/122
    * Brandon: thanks for joining us in 2024, Ben
* What to do about 1.0? What should go in it? Should we jump directly to the refactor?
    * Update on that discussion
        * Reviewing with Red Hat folks on their data model and experiences with using GUAC
        * Google work on mapping internal supply chain to GUAC ontology
    * Brandon: For 1.0, we want to know what parts users want to be stable
    * Mihai: We’ve experimented a lot with the current setup (DB backends, etc). Now it’s time to settle on an architecture that works for users
    * Parth: Original architecture may have been too ambitious, trying to please everyone and became too pluggable. Now that the supply chain space has evolved and it’s become more stabilized in terms of what people want. From a developer standpoint, how do we make this easier for someone to pick up and use on their own project? Right now it’s very scalable, great for enterprises, but doesn’t address the small developer & easy adoption. How do we go about that?
    * Jeff: I support calling what we have here 1.0. There’s some worry that it’s an “empty promise” since we’re not going to continue it as it is exactly. It’s essentially a complete idea that could be used and picked up, so we should put a stamp on it. “2.0” might be called something else that makes it more clear that it’s different and we could have, for example, “GUAC Monolith” and “GUAC components”
    * What is in scope of 1.0?
        * Parsers
        * Collectors
            * File, OCI, etc.
        * Ingestor
        * Postgres backend
* [Alex] How should we represent/ingest multiple instances of the same image? 
    * https://github.com/guacsec/guac/issues/2387
    * Current backend assumptions
        * Can’t trust SBOM contents subject, which GUAC relies on.
            1. SBOMs should be created at image build time and should follow across registries
            2. SBOMs should be signed, which means you can’t regenerate when moved across registries
    * Considering an option to override the subject at ingestion time
        * In the graph, should there be a node for the digest that other objects are connected to?
    * Brandon: in the HasSBOM, we could create a predicate that connects it to the artifact hash, which would solve the problem of moving the image to another registry.
        * Jeff: the ontology supports SBOM on the artifact, but the parsers don’t
        * Parth: it will do it on artifact first, if it’s not there, it will do it on the package. So if the SBOM contains the proper digest for the image, it will behave correctly
        * Brandon: this section from a previous talk may be helpful: https://youtu.be/ZYsUbN6oT7Q?feature=shared&t=1431 
    * ACTION: Alex to set up a follow-up meeting with Brandon, Parth
* Upcoming events (see [OpenSSF calendar](https://openssf.org/getinvolved) for meeting details)
    * Weekly Maintainer Meeting: Mondays, but cancelled next week
    * Community Meeting: Thursday 20 February
    * FOSDEM (1-2 Feb in Brussels)
        * Several contributors attending fringe event: [FOSS license and security compliance tools workshop](https://workshop.aboutcode.org/) (31 Jan)
        * Brandon Lum & Marco Deicas: “[A retrospective on Google’s SBOM implementation](https://fosdem.org/2025/schedule/event/fosdem-2025-6074-a-retrospective-on-google-s-sbom-implementation/)”
        * Jeff Mendoza & Qing Tomlinson: “[Discover Dependency License Information Using SBOMs and ClearlyDefined](https://fosdem.org/2025/schedule/event/fosdem-2025-5839-discover-dependency-license-information-using-sboms-and-clearlydefined/)”
        * Michael Lieberman: “[The Breadth and Depth of SBOMs](https://fosdem.org/2025/schedule/event/fosdem-2025-6164-the-breadth-and-depth-of-sboms/)”
* KubeCon Europe (1-4 April in London)
    * Michael Lieberman is presenting a keynote “[Cutting Through The Fog: Clarifying CRA Compliance in Cloud Native](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” with Eddie Knight
    * Jeff Mendoza is presenting a talk “[Why Don’t We Have Both? Track Build- and Run-time Information for Security With Kubescape and GUAC](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” with Ben Hirschberg
    * Michael Lieberman is presenting a talk “[Bridging Supply Chain Policy with Git-less GitOps and GUAC](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” with Andrew Martin.
