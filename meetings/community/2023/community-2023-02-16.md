# GUAC Community Meeting: 2023-02-16

Recording: https://www.youtube.com/watch?v=fTrIV6I3zSA

## Attendees

* Jon Zeolla (Seiso)
* Brandon Lum (Google)
* Mihai Maruseac (Google)
* Parth Patel (Kusari)
* Tim Miller (Kusari)
* Dejan Bosanac (Red Hat)
* Rob Honeybul (Snyk)
* Dan Perry (Google Cloud)
* Hemil Kadakia (Yahoo)
* Jacques Chester (Shopify)
* Verónica López (PlanetScale)
* Mike Lieberman (Kusari)
* Kevin Conner (Red Hat)
* Randall T. Vasquez (Gentoo/SKF/LF)
* Raj Krishnamurthy (ComplianceCow)
* Eman Abu Ishgair (Purdue University)
* Furkan Türkal (Trendyol)
* Leo Alvarez (Baker Tilly)

## Agenda

* Introductions and welcome members!
* Sharing workshop notes (5 mins)
    * [GUAC 2023 Q1 Summit Notes - SHARED EXTERNALLY](https://docs.google.com/document/d/15Kb3I3SWhq-9_R7WYhSjsIxn_FykYgPyFlQWlLgF4fA/edit) (available on README.md)
* Demo of GraphQL interface (10 mins)
    * [[External] Refactoring the GUAC Assembler](https://docs.google.com/document/d/1yZ3-ZcfnRDWgw9uZlPuLmIHS9pNMr3DO_AEbHsDXmN8/edit)
    * Qualifier ontology to include semantic
    * https://github.com/guacsec/guac/pull/454 , https://github.com/guacsec/guac/pull/457, https://github.com/guacsec/guac/pull/452, https://github.com/guacsec/guac/pull/451, https://github.com/guacsec/guac/pull/447, … More PRs being made this week and next (WIP)
* Demo of Collectsub service (10 mins)
* Highlight SETUP.md (5 mins)
* Issues for community engagement:
    * https://github.com/guacsec/guac/issues/281
    * https://github.com/guacsec/guac/issues/443 
    * https://github.com/guacsec/guac/issues/250 
* Open discussion
    * Signaling containment
        * Container image container layers
        * Layers contain files
        * Also ruby gems, and the physical identity of gem file, etc.
    * System dependencies across teams, across departments and also across systems
        * From a framework/infrastructure/productivity, help internal releases, etc.
        * For legal and operational perspective
    * Policy engine a bit more focused than OPA
        * https://github.com/seedwing-io/seedwing-policy
             * Query all the attestations and use it to make policy decisions
        * https://github.com/seedwing-io/seedwing-proxy
             * Proxy between build process and package manager (Secure Ingestion)
    * GUAC as policy information point to enrich and inform to do decisioning and enforcement
    * Risk Management, similar to VEX work to make sure something is OK or not OK