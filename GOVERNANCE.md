# Governance

## GUAC community

The GUAC community (including GUAC OpenSSF meetings, website  and [github organization](https://github.com/guacsec/) administration) is home to several projects focused around solving problems related to the consumption and utilization of supply chain metadata at scale. The community contains "Core projects" which emcapsulate large bodies of work where a separate governance of code and process makes sense, while retaining requirements around aspects such as licensing and code of conduct.

Thus the governance is structured into the "GUAC community maintainers" team and "GUAC core projects" maintainers teams.

### GUAC community index

- GUAC Community:
  - governance
  - guac-landing
  - guac-site
  - .allstar
  - .github
- GUAC Core Project: Graph for Understanding Artifact Composition (GUAC) ([MAINTAINERS.guac](MAINTAINERS.guac))
  - guac-docs
  - sw-id-core
  - guac-visualizer
  - guac-data
  - helm-charts
  - guacaidemo
  - guac-test
- GUAC Core Project: Trustify ([MAINTAINERS.trustify](MAINTAINERS.trustify))

Unless specified, all other resources and projects will fall under governance of the broader GUAC community.

### GUAC community maintainers

List of GUAC community maintainers can be found at [MAINTAINERS](MAINTAINERS).

Maintainership is driven by engineering contributions to the project, and a n-1
vote among current maintainers is required to make changes to the list of
maintainers. Should the quorum of necessary maintainers to merge changes be
unmet due to a maintainer’s inactivity for 3 months — without prior notice and
concurrence to the absence — the inactive maintainer will be removed from the
project and the decision documented.

At any one time, there should be at least 3 maintainers, with each core project
represented by at least 1 maintainer.

## GUAC core project governance

- Each core project consists of multiple github repos, that should all live within [the guacsec github organization](https://github.com/guacsec/). This would provide a single organizational home for related projects, simplifying discovery and collaboration.
- Each core project establishes its own project governance and contribution ladders.
- Each core project will have write and admin privileges to individual code repositories.
- Core projects are required to communicate their governance changes GUAC community maintainers.
- Core projects must use licenses which are agreed upon by the GUAC community maintainers.
- Core projects must have code of conduct requirements which are agreed upon by the GUAC community maintainers.
- The scope of each core project is defined within the [GUAC community index](#guac-community-index)

## Code of Conduct

Please refer to the [Code of Conduct](CODE_OF_CONDUCT.md) for full details.

## License

The project will use [Apache 2.0 license](LICENSE) for code.
