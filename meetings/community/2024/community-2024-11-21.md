# GUAC Community Meeting: 2024-10-17

Recording: https://youtu.be/yQnqpAAKDRo

## Attendees

* Ben Cotton (Kusari)
* Brandon Lum (Google)
* Mihai Maruseac (Google)
* Brandt Keller(Defense Unicorns)
* Lukas Hoehl (STACKIT)
* Dejan Bosanac (Red Hat)
* Casey Fahey (NetGoalie)
* Tim Miller (Kusari)
* Marco Deicas (Google)
* Alex Feng (Microsoft)
* Parth Patel (Kusari)
* Ridwan Hoq (Microsoft)
* Hari Kunduru (ARA)

## Agenda

* Welcome new friends!
    * Lukas: based in Germany working for STACKIT. Has been watching the GUAC repo for a year.
    * Brandt: works for Defense Unicorns (large focus on public sector). Sees a lot of the problems that GUAC helps solve. Met with Kusari team at KubeCon
* Releases since the last meeting:
    * GUAC: [v0.10.2](https://github.com/guacsec/guac/releases/tag/v0.10.2), [v0.11.0](https://github.com/guacsec/guac/releases/tag/v0.11.0), [v0.11.1](https://github.com/guacsec/guac/releases/tag/v0.11.1), [v0.11.2](https://github.com/guacsec/guac/releases/tag/v0.11.1)
        * Adds HTTP handler to display version string
        * Add batch querying for isDependency, CertifyVuln and CertifyLegal via Package Version ID
* Decisions:
    * We’re canceling the GUAC Time office hours due to low attendance
        * Weekly Maintainer Meetings are still public
* [Brandon Lum] Update on [GUAC refactor](https://docs.google.com/presentation/d/1OaP-h9h6QIEHFO7zpUyR5VeoLEMuLL4EoFc6zkWsWfo/edit#slide=id.g30b6c3a5123_0_149)
    * At recent Maintainer Meetings, we’ve been chatting about lessons learned and feedback on GUAC. The goal is to make GUAC easier to use for people. For example, GraphQL is hard to get started with. People want an easier way to get started
    * Making a shift in the audience we’re serving as a project. Initially, the idea was an all-in-one where you put in documents and get insights. But we realized there are more audiences and some of them (e.g. Kusari and Red Hat products) would like to use parts of GUAC with their own interfaces
    * Three main areas
        * Easy to build solutions on top of GUAC
        * Easier on-ramp to see what GUAC can do without having to get deep into graph database
        * Foster an insights/policy building community around the project
    * GUAC = Aggregation + Synthesis
        * guac-ingest: How do I make meaning out of metadata? This can be a starting point for basic users.
        * guac-graph: How do I create a scalable supply chain knowledge graph (this is what current GUAC is). More advanced users can integrate this into their infrastructure.
        * guac-insights: Insights for policy checks, patch planning, etc
        * Ben: How much work will this take and what help do we need?
            * There’s some work to split up the current project into more modular pieces. In particular, converting the GraphQL schema to Protobuf. We could use community feedback in how people want to use the graph interface and how we can design it better.
    * Rough roadmap
        * Graph v1, which exposes ent SQL and hides GQL interface, for Q1 2025
        * Ingest v2 ontology (protobuf/json ontology) worked on in parallel for Q3 2025
        * Graph v1.x compatible with both ent and GQL, in Q3-4 2025
        * Insights, continual experimentation (not looking to create specific versions yet). Not looking to package yet
    * What does this actually look like?
        * Guac-ingest: CLIs that allow converting metadata files into a guactology JSON, piping output into JQ and a query language
* KubeCon NA recap
    * Parth & Mihai presented “[Papers, Please: Scrutinizing AI Model Creation](https://www.youtube.com/watch?v=uqU3fnmK0BA)” at SigStore Con
    * GUAC got mentions in three separate keynotes:
        * [Open source security is not a spectator sport](https://youtu.be/tqvjzsNmJZ8?si=aCYCgyMXofRZkQKh)
        * [A developer's guide to securing your software supply chain](https://youtu.be/YQuzhSGGPNk?si=i-49TqYtmoZrKzr6)
        * [Cloud Native's next decade: stable, secure, and ready for disruption?](https://youtu.be/gMIhdUiHPps?si=OI9qQp0Jy4uI8u9a)
* [Lukas Hoehl] Ingesting trivy SBOMReports into guac
    * https://github.com/hown3d/guac-trivy-operator-webhook
    * Background: using the trivy operator in a lot of clusters. Using collectors like s3 buckets is not easy because it would need to be pull from trivy into the s3 bucket first. But the trivy operator has a webhook, so he can use that to ingest documents into GUAC
    * Parth: is the trivy scan giving a runtime SBOM?
        * If there’s no SBOM attached, it will generate a new one by scanning the image. If there’s an SBOM in the registry, it will use that.
    * Parth: we also chatted with Kubescape (has similar functionality to trivy) maintainers, which generates a runtime SBOM and a network report of ingress/egress traffic. One thought we were having is to use that to implement isDeployed support. With that info, GUAC could do analysis for difference between build- and run-time dependencies. Produces VEX docs that indicates if a dependency is not being used in runtime.
    * Hari: uses both trivy and GUAC. Does this bridge the gap between the trivy operator and GUAC?
        * Yes
* Cool in-progress contributions:
    * Feat/registry collector cli additions #2241
        * https://github.com/guacsec/guac/pull/2241 
    * Collect additional metadata for vulnerabilities from OSV #2219
        * https://github.com/guacsec/guac/pull/2219 
        * OSV has more information than we currently use. Created an option to include additional metadata like severity, so users can filter out lower-severity vulns to help with prioritization
* [Brandt] Airgap Support
    * https://github.com/guacsec/guac/issues/2294 
    * In talking with others at KubeCon, there’s a lot of nuances to running GUAC in air-gapped environments. For example: accessing data. But we have tools like zarf that can help. Wants to start discussion about how this could work.
    * Availability survey: https://whenisgood.net/air-guac
* Upcoming events (see [OpenSSF calendar](https://openssf.org/getinvolved) for meeting details)
    * Weekly Maintainer Meeting: Monday
    * Community Meeting: Thursday 19 December
