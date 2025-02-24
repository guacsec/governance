# GUAC Community Meeting: 2025-02-20

Recording: https://youtu.be/4wCFLl-1UNk

## Attendees

* Ben Cotton (Kusari)
* Mihai Maruseac (Google)
* Dejan Bosanac (Red Hat)
* Ria Farrell Schalnat (Hewlett Packard Enterprise)
* Arnav Joshi (Akamai)
* Craig Pearce (AWS)
* Parth Patel (Kusari)
* Michael Lieberman (Kusari)
* Casey Fahey (Net Goalie)

## Agenda

* Welcome new friends!
    * Craig was recently geeking out over GUAC and Sigstore
    * Ria is interested in the ClearlyDefined integration and learning more about GUAC generally
    * Arnav has general interest in the software supply chain space. Attended meetings a few months ago
* Releases since the last meeting:
    * [GUAC v0.13.0](https://guac.sh/blog/2025-01-17-guac-v0.13.0/) (and 0.13.1 and 0.13.2)
        * Adds support for OpenTelemetry
    * Upcoming work
        * Continuing to work on defining the feature set for 1.0. We’re close to getting it ready for that
        * Also working on improving the usability with design changes, etc for “GUAC 2.0”
        * Folks from Microsoft are working to unify SBOM representation across multiple image registries (issue 2387)
* FOSDEM recap (1-2 Feb in Brussels)
    * Jeff and Michael attended attended fringe event: [FOSS license and security compliance tools workshop](https://workshop.aboutcode.org/) (31 Jan)
    * Lots of discussion of CycloneDX and SPDX formats. SBOMs are starting to hit a critical mass. People are now looking to do useful things like that, and therefore need tools (like GUAC!)
        * Looking for vulnerabilities, license issues, etc
        * Also a view over time as new versions are developed
    * Talks
        * Brandon Lum & Marco Deicas: “[A retrospective on Google’s SBOM implementation](https://fosdem.org/2025/schedule/event/fosdem-2025-6074-a-retrospective-on-google-s-sbom-implementation/)”
        * Jeff Mendoza & Qing Tomlinson: “[Discover Dependency License Information Using SBOMs and ClearlyDefined](https://fosdem.org/2025/schedule/event/fosdem-2025-5839-discover-dependency-license-information-using-sboms-and-clearlydefined/)”
        * Michael Lieberman: “[T]he Breadth and Depth of SBOMs](https://fosdem.org/2025/schedule/event/fosdem-2025-6164-the-breadth-and-depth-of-sboms/)”
            * How do you get from zero to full end-to-end visibility?
    * CRA discussions:
        * Some conversations about SBOMs and how tools like GUAC can help folks understand risk and compliance
* [Ria] Using GUAC to improve license compliance
    * At the CISA community meeting, Ben presented on GUAC, with a discussion of the ClearlyDefined support. Opened her eyes as to how ClearlyDefined could be a more scalable resource for day-to-day input to her process.
    * At an SPDX general meeting, there was discussion of Snyk’s parlay tool. Parlay uses a different information backend (ecosyste.ms)
    * More confidence in the ClearlyDefined data, but parlay has a useful feature to her: ingesting and then producing an improved SBOM.
    * The goal is to reduce the number of “NO ASSERTIONS” in the dependency graph.
    * Mini test: one SBOM went from 35 NO ASSERTIONS down to 25. That’s a material improvement.
    * Wants to use guacone to decorate the SBOM or produce a decorated SBOMs. Is this something that GUAC would consider?
        * Michael: open question is where that integration lands. For example, OpenSSF’s bomctl is intended to be an SBOM improver, with integration into tools like GUAC
        * Parth: the goal for GUAC was always to take the information you have and add data from the outside to make it better. Then we could support getting it back out to an SBOM or however you need to consume it.
    * Another area for improving the SBOM is creating an attribution document for complying with licenses that require it. Ria would like to see SBOM and attribution merged together into one machine-readable whole.
* Upcoming events (see [OpenSSF calendar](https://openssf.org/getinvolved) for meeting details)
    * Weekly Maintainer Meeting: Mondays
    * Community Meeting: Thursday 20 March
    * KubeCon Europe (1-4 April in London)
        * Michael Lieberman is presenting a keynote “[Cutting Through The Fog: Clarifying CRA Compliance in Cloud Native](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” with Eddie Knight
        * Jeff Mendoza is presenting a talk “[Why Don’t We Have Both? Track Build- and Run-time Information for Security With Kubescape and GUAC](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” with Ben Hirschberg
        * Michael Lieberman is presenting a talk “[Bridging Supply Chain Policy with Git-less GitOps and GUAC](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” with Andrew Martin.
