# GUAC Maintainers Meeting: 2024-07-01

Recording: https://youtu.be/KepqEzFkoZ8

## Attendees 

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Parth Patel | Parth Patel | Kusari | he/him
| Soham Arora | arora106@purdue.edu | Purdue | he/him
| Brandon Lum | Brandon Lum | Google | he/him
| Karla Obermeier | koberme@purdue.edu | Purdue | 
| Tobias Heldt | | |

## Agenda

* Welcome new friends
    * Tobias Heldt - Security economics researcher building a tool to identify risk in SBOMs, interested in GUAC
* Collect Opens
* [Ben Cotton] Adding GUAC to [LFX Insights](https://insights.lfx.linuxfoundation.org/foundation/openssf/projects) platform that provides community statistics, etc.)
    * This would give us some helpful metrics on community, etc
    * Bennett Pursell can add himself as an enterprise owner and make the necessary GitHub changes, but wants permission first.
    * Maintainers say that the access should only be temporary 
    * Ben will figure out how long access is needed and a maintainer will give access and create a calendar invite to remove access
    * Maintainer LGTMs: Brandon, Mike, Jeff (want to ensure permissions to be closely monitored/locked down), Parth
    * Also potentially adding GUAC metrics into LFX
        * For license and vulnerability use cases
* Talking points from CNSCon
    * Deployment chaining (meeting with MS)
    * Helm chart SBOM
    * Deployment metadata
    * Schedule a weekly follow up with them
* [Mike] AI + GUAC
    * If we have a large dataset in GUAC, we should be able to train the datasets to find the shape of malicious supply chains
    * Met DigitalOcean, Zara, Professor at University of Arizona (AI), familiar with network AI, setting up a call in the next few weeks, may have students who are interested in poking around with GUAC
* We got multiple shoutouts at CNSCon at the keynotes
    * Marina Moore gave a keynote shoutout to GUAC and other projects in the cybersecurity/supply chain security space
    * Puerco@ gave a shoutout to GUAC in his keynote on VEX and how different tools are ingesting VEX and doing some analysis
    * A few talks that involved GUAC at CNSCon
    * Mike and Jeff at the booth know about GUAC
* Review open PRs: https://github.com/guacsec/guac/pulls?q=is%3Apr+is%3Aopen+label%3Aneeds-review
    * gcr.io/distroless/static
    * https://github.com/GoogleContainerTools/distroless/tree/main/base
    * Following up with clearly defined certifier for license information, right now will use output of clearly defined but will eventually be based on intoto attestation when that goes through
        * Design doc: [Legal information in GUAC](https://docs.google.com/document/d/1NmLlU5wuP2X9CK7QCWZkkOciNn1QFLKQCFCW9CEI8HQ/edit#heading=h.uuq58ag8nrfy)
Information may change due to improvements in the results, so a certifier makes sense since their lifecycle is more frequent
* [Ben Cotton] (time allowing) Please promote me 🙂 https://github.com/guacsec/governance/issues/15
