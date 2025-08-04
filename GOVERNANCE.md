# Governance

## GUAC community

The GUAC community is home to several projects focused around solving problems related to the consumption and utilization of supply chain metadata at scale. The community contains "Core projects" which emcapsulate large bodies of work where a separate governance of code and process makes sense, while retaining requirements around aspects such as licensing and code of conduct.

Thus the governance is structured into the "GUAC Steering Committee" team and "GUAC Core Projects".

### GUAC community index

- GUAC Steering Committee
  - governance
  - guac-landing
  - guac-site
  - guac-docs
  - .allstar
  - .github
- GUAC Core Project: Graph for Understanding Artifact Composition (GUAC) ([MAINTAINERS.guac](MAINTAINERS.guac))
  - guac
  - sw-id-core
  - guac-visualizer
  - guac-data
  - helm-charts
  - guacaidemo
  - guac-test
- GUAC Core Project: Trustify ([MAINTAINERS.trustify](MAINTAINERS.trustify))

Unless specified, all other resources and projects will fall under governance of the broader GUAC community.

### GUAC steering committee

List of GUAC steering committee members can be found at [STEERING_COMMITTEE](STEERING_COMMITTEE).

#### Responsibilities

The steering committees' responsibilities include

- Define Core Projects in the GUAC community and which projects should be in their respective core project
- Define focus of the group, including topics to tackle and technical direction
- Identify and create opportunities for GUAC projects to work with each other, and with other projects in the OpenSSF and beyond
- Resolve conflicts in the GUAC community and escalate to the OpenSSF where appropriate
- Adminstration of GUAC OpenSSF meetings, website  and [github organization](https://github.com/guacsec/)

#### Process

Membership is driven by engineering contributions to the project, and a n-1
vote among current member is required to make changes to the list of
members. Should the quorum of necessary members to merge changes be
unmet due to a member’s inactivity for 3 months — without prior notice and
concurrence to the absence — the inactive member will be removed from the
project and the decision documented.

At any one time, there should be at least 3 member, with each core project
represented by at least 1 member.

## GUAC core project governance

- Each core project consists of multiple github repos, that should all live within [the guacsec github organization](https://github.com/guacsec/). This would provide a single organizational home for related projects, simplifying discovery and collaboration.
- Each core project establishes its own project governance and contribution ladders.
- Each core project will have write and admin privileges to individual code repositories.
- Core projects must have at least 2 maintainers
- Core projects are required to communicate their governance changes GUAC community maintainers.
- Core projects must use licenses which are agreed upon by the GUAC community maintainers.
- Core projects must use the OpenSSF code of conduct
- The scope of each core project is defined within the [GUAC community index](#guac-community-index)

## Code of Conduct

Please refer to the [Code of Conduct](CODE_OF_CONDUCT.md) for full details.

## License

The project will use [Apache 2.0 license](LICENSE) for code.
