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

#### Rules

The steering committee will consist of the following seats:
- 3 general seats
- 1 seat per core project (core project seat)

The general rules and restrictions on the seats are:
- The steering committee must be represented by at least 2 different employers
- Each change in seat is decided by majority vote of the steering committee
- Inactivity of a member for >3 months will result in removal
- There must be at least 3 active steering committee members at any time
- There is no limit on member terms

##### General seat

There are no restrictions on who can occupy this seat.

##### Core project seat

The person that occupies this seat must be a maintainer on the respective core project.

#### Process

To establish a change in steering committee members:
1. A proposal is made by a steering committee member by opening up an issue in [GUAC governance](http://github.com/guacsec/governance/)
1. The proposal needs to be communicated on all [supported community channels](https://guac.sh/community/)
1. Steering committee members can approve the proposal by providing a +1 on the issue
1. Any member of the community can comment on proposals
1. After 2 weeks upon communication of the proposal, and with majority steering committee member approvals, the change in steering committee members will be in effect

##### Process exceptions

- In the case where there isn't a quorum for a steering committee that meets the [rules](#rules), steering committee membership will be bootstrapped and proposed for [OpenSSF TAC](https://github.com/ossf/tac) approval
- Failing resoultion by the steering committee, any issues related to steering committee membership and process can be escalated to the [OpenSSF TAC](https://github.com/ossf/tac)

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
