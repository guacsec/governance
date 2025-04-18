# GUAC Community Meeting: 2025-04-17

Recording: https://youtu.be/OZSPhOlP3Vw

## Attendees

* Ben Cotton (Kusari)
* Dejan Bosanac (Red Hat)
* Michael Lieberman (Kusari)
* Brandon Lum (Google)
* Jeff Mendoza (Kusari)
* Casey Fahey
* Mihai Maruseac (Google)

## Agenda

* Welcome new friends!
* (Ben) ladder climbs
    * Ben Cotton promoted to Reviewer for GUAC Visualizer
* (Jeff) Kubescape collector
    * Introduced in GUAC v0.14.0
    * Jeff and Ben Hirschberg gave a talk at KubeCon Europe ([slides](https://static.sched.com/hosted_files/kccnceu2025/9a/KubeConEU25-GUAC-Kubescape.pdf))
    * Supports “filtered” SBOMs — a custom resource that Kubescape adds. It shows the SBOMs for what is running in the cluster.
        * Regular SBOMs provide a list of packages
        * Filtered SBOMs provide only the packages that eBPF detects are loaded into memory. If a package exists in the filtered SBOM but not in the unfiltered SBOM, it’s not being run
    * Kubescape also supports producing VEX statements for packages it detects are not loaded into memory. Jeff wants to add support for that to GUAC
* [GUAC 1.0](https://docs.google.com/document/d/1bjkxGu1YcMurav5DU-imoKfEN2j-LuNQJFOa__A-m0I/edit?tab=t.0#heading=h.8omn951z7ln6) technical overview and feedback
* Topics being discussed in maintainer meetings
    * GUAC/Trustification community discussion
        * Trustification came from an earlier version of GUAC but kept in the same problem space
        * Looking at combining the two projects under one community in order to tackle common problems and give users an easier way to address their needs at any scale
        * First steps
            * Identify common ground for shared tools/libraries/protocols
            * Brandon: it would be good to think about better support of extension to the data
* KubeCon EU thoughts
    * Mike: CNCF plans to try out using GUAC to do supply chain analysis across all CNCF projects.
        * They have issues with license and vulnerability management. That’s typically left to individual projects, but they want to be able to have a broad-level view to ensure there aren’t issues that projects need to address.
        * Over the next few months, they plan to start looking at this in earnest. Mike is working with them to help build an understanding of their needs and getting them started.
    * Mike: Did a talk with Andrew Martin of ControlPlane about Flux and GUAC. Talked through using GUAC to locate vulnerable packages in Flux-deployed applications. Possible future work to use GUAC as a data source for policy engines on GUAC deployment.
    * Mike: eventually we’ll want to look at supporting OSPS Baseline. The data will probably come in via Scorecard
* Mike: gave a talk at VulnCon. Couldn’t do a demo because it was slides-only.
* Mike: There’s ongoing discussion of what the future of CVEs looks like. Maybe there’s no centralized authority and things are distributed. Similarly, SBOM information and other stuff is decentralized. This could have impacts on how GUAC collectors work.
* Upcoming events (see [OpenSSF calendar](https://openssf.org/getinvolved) for meeting details)
    * Weekly Maintainer Meeting: Mondays
    * Community Meeting: Thursday 15 May
