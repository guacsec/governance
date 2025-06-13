# GUAC Maintainers Meeting: 2025-05-19

Recording: https://youtu.be/hRcBOBGWHt4

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Nathan Naveen | nathan@kusari.dev | Kusari | he/him

## Agenda/notes

* Community merge
    * Red Hat legal did not have any questions for Dejan
    * No updates from OpenSSF
* GUAC 1.0
    * Blog process initiated
    * Who can move the helm charts repo out of Kusari’s org?
* How do we handle new releases of experimental repos?
    * Can Ben, as a Reviewer of guac-visualizer, publish a new release or does it require Owner/Maintainer?
    * Mike: Full-fledged GUAC releases should require a higher level of privilege. But experimental repos could have a lower bar.
    * Ben: guac-visualizer is in kind of a weird exception state. It’s not actively developed, and I don’t have the technical expertise to ask for Owner permission.
    * Mike: it’s worth thinking through if our ladder still makes sense in the long term. Short term, reviewer might make sense, but long term we need other ideas. We don’t have multiple backends, etc.
    * Jeff: (agrees with Mike). Even in the current situation, it makes sense for Ben to be owner of guac-visualizer, at least for now.