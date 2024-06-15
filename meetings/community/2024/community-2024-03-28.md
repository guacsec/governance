# GUAC Community Meeting: 2024-03-28

Recording not available

## Attendees

* Parth Patel (Kusari)
* Mike Lieberman (Kusari)
* Jeff Mendoza (Kusari)
* Tim Miller (Kusari)
* Marco Deicas (Google)
* Dejan Bosanac (Red Hat)
* Nathan Naveen (Kusari)
* Marco Rizzi (Red Hat)
* Ridwan Hoq (Microsoft)
* Alex Feng (Microsoft)
* Casey Fahey (NetGoalie)
* Yotam Perkal (Rezilion)

## Agenda

* Introductions and welcome members!
    * Narsa - new engineer at Kusari
    * Yotam - joining from Rezilion
    * Nick - From OSI and ClearlyDefined
    * Casey Fahey @ NetGoalie, long time listener first time caller, I am a dev and consultant in New York City
    * Welcome all !!
* [Parth] Rolling community promotion recognitions
    * [Contributor ladder](https://github.com/guacsec/guac/blob/main/CONTRIBUTING.md#contributor-ladder)
    * Dejan Bosanac (https://github.com/dejanb) +reviewer:ingestion 
        * SPDX and CDX parser additions [1,2,3,4]
        * Fix: s3 collector [1]
        * TLS for servers [1,2]
    * Marco Rizzi (https://github.com/mrizzi), +owner:backend
        * Foundational in creation and development of the Ent backend! (https://github.com/guacsec/guac/pulls?q=is%3Apr+author%3Amrizzi+is%3Aclosed) 
* [Parth] Ent optimization demo
    * Started at 10min for ingestion of “guac-data/docs”
    * Now at 29 seconds
* [Parth] Discussion and feedback on proposal for focusing on backends
    * GraphQL interface has an abstraction to work with multiple backends
        * Ex: neo4j/opencypher, gremlin, etc.
    * Looking to focus on KV and Ent backends
        * Keyvalue + inmemory storage
        * Ent + Postgres
    * Discuss mechanics of other backends - move to other repositories, separate ownership, etc.
        * Open an issue to gather feedback
        * Could you BYO Go package in a separate repo?
* [Parth/Dejan] OPA Gatekeeper / GUAC Demo (from Kubecon)
    * Current location: https://github.com/dejanb/guac-provider
    * Planning to move to GUAC org, need some changes in upstream GUAC first
    * Some work needed to make it more generic
    * Can this policy-as-code pattern be used outside k8s? Ex: on package download
        * GUAC can be used as a source for these types of policy decisions
        * Depend on how the tool is able to ingest this information
        * OPA outside of gatekeeper? Are there other enforcement mechanisms that others are aware of?
        * Kyverno is another option for k8s
        * Some interest in an Identity Aware Proxy use case - not sure which exact proxy
        * OPA is general purpose, all we need for this implementation is the image digest, could be used as an input to other systems
* Opens
* [IsDeployed discussion](https://github.com/guacsec/guac/issues/1777)
    * Overall, do we feel that this is in the scope of GUAC?
    * Mike: yes in the scope of area. Folks want to know “where is that deployed” in supply chain. Is this something that goes in GUAC or is something where GUAC is compared to a known state.
        * If it does belong in the graph, how granular does it go. GUAC doesn’t become a “monitoring system”
    * Do want to explore this space and figure out where we land
    * Look into other tools as well (OpenClarity)
    * Tim: Biggest request at KubeCon EU - need to know “what is running”
        * Need to sort out how to answer this question, not sure if it is in graph or now
    * Mike: ran a script of osquery to query against GUAC,
    * Jeff: “HasSBOM” can represent source, build, or deploy currency. Could be that or a new node. The node should be an “attestation” that X was deployed by foo at this time
    * Ridwan: Also would want an “X was un deployed” as well with timestamp
    * Parth: Also inToto attestations can be used for deployment