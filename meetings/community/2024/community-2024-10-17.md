# GUAC Community Meeting: 2024-10-17

Recording: https://youtu.be/gIs2ZffwTOY

## Attendees

* Ben Cotton (Kusari)
* Brandon Lum (Google)
* Jeff Mendoza (Kusari)
* Marco Deicas (Google)
* Shreyas Pandya (Guidewire)
* Parth Patel (Kusari)
* Casey Fahey (NetGoalie)
* Mihai Maruseac (Google)
* Mohamed Chorfa (Thales SA)

## Agenda

* Releases since the last meeting
    * GUAC: [v0.8.7](https://github.com/guacsec/guac/releases/tag/v0.8.7), [v0.8.8](https://github.com/guacsec/guac/releases/tag/v0.8.8), [v0.8.9](https://github.com/guacsec/guac/releases/tag/v0.8.9), [v0.9.0](https://github.com/guacsec/guac/releases/tag/v0.9.0), [v0.9.1](https://github.com/guacsec/guac/releases/tag/v0.9.1), [v0.10.0](https://github.com/guacsec/guac/releases/tag/v0.10.0), [v0.10.1](https://github.com/guacsec/guac/releases/tag/v0.10.1)
        * Upgrades to ent backends and lots of QOL and bugfixes (especially around clearly defined ingestor)
        * In 0.8.9 there was a small compatibility breaking change in the vulnerability query, it is documented in the release notes and on the demo flow.
    * guac-visualizer: [v0.4.5](https://github.com/guacsec/guac-visualizer/releases/tag/v0.4.5)
        * Adds a view of known package information
        * Now with CI builds
* Decisions:
    * We’re deprecating all other backends except for Ent/Postgres, one backend to rule them all
    * Key-value will be testing only
* Heads up on maintainer discussions (on Monday):
    * Discussion on going from GQL → SQL as an interface
* [Ben Cotton] How our demo flow is working
    * GUAC “sizzle reel” (https://www.youtube.com/watch?v=JZOIAfrpKek) 
    * Slides: [GUAC Demo Pages - October 2024](https://docs.google.com/presentation/d/17QlZEjrnU5rvBkm7ekeYe8HWqp-5cI2_4I2DqU8HgvY/edit?usp=sharing)
* Upcoming events (see [OpenSSF calendar](https://openssf.org/getinvolved) for meeting details)
    * [Hacktoberfest](https://guac.sh/blog/2024-09-25-hacktoberfest/) (ongoing through 31 October!)
    * Weekly Maintainer Meeting: Monday
    * SOSS Fusion (Atlanta, GA): 22–23 October
        * Jeff and Mihai will be there
    * GUAC Time office hours: next Friday (25 October)
        * KubeCon NA (Salt Lake City, UT): 12–15 November
        * [Open Source Security on Tap party](https://www.eventbrite.com/e/open-source-security-on-tap-tickets-1039261919377) hosted by Kusari, ActiveState, and ControlPlane
    * Community Meeting: Thursday 21 November
