# GUAC Maintainers Meeting: 2025-07-14

Recording: https://youtu.be/oE8s20jrBeM

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him

## Agenda/notes

* [Dejan] Trustify donation - discuss first steps
    * Good news agreement being signed 🎉, should be completed soon
    * https://docs.google.com/document/d/18ECugArG7MT4baRHE6KrvdRoTCx99kNedGvyOJEDpYA/edit?tab=t.0 
    * Next steps
        * Establish the initial joint governance structure: Implement the proposed changes to the community's leadership and decision-making processes.
        * Plan initial joint community events and collaboration opportunities: Organize meetings, workshops, or coding sprints to foster interaction and collaboration between the previously separate communities.
        * Redo docs side to do rearranging
* [Santiago] Software Identifier update 
    * Last time did not have data of Sw identifiers in the wild
    * Collecting SBOMs from different ecosystems (docker hub, maven, etc.), put them through identifier parsing pipelines
    * Found a couple on Red Hat PURLs
        * Red Hat makes them one way
        * And other tools that make Red Hat purls do it in another way
        * Couple things including definitions of purl formats (including channels, etc.)
    * Wanted to use the SW ID core tool and carving out an MVP, and pulling in full of GUAC may be daunting, may have a separate stripped down version
    * Realized recently that disambiguation can be a simple mechanism, or can something that uses embeddings or entity resolution
    * Could move a bunch of the identifier libraries to be more generic, talked about having the guac generated APIs be its own repo or more simply its own golang module within the repo so it can be separately depended upon
    * Useful: turn gql models into protos (good starting point for 2.0) 
* [Ben] Are we interested in participating in the upcoming [Immutable Releases preview](https://www.linkedin.com/posts/kristinaheidinger_big-milestone-to-share-after-lots-of-work-activity-7348231481292394497-x1cB?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAAOuMkB7siGlYHoQHsuDSFFnuSrly3L4zA)?
    * Would be interesting to check out
    * Start with GUAC visualizer if we want to test it out
    * dejan@ can help make some connections with Kristina 
