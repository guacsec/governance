# GUAC Maintainers Meeting: 2025-06-30

Recording: https://youtu.be/KZgIDOKBbpU

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him

## Agenda/notes

* Open Source Summit NA recap
    * Met with Brandt Keller, who did a presentation on Zarf with GUAC
        * Everything needed to make it work wasn’t in the code, needed a few tweaks
            * A few CLI changes on GUAC to specify address and use http vs https
            * Built a GUAC Zarf package (something we can consider throwing into a makefile to make a zarf package too)
            * How to get everything that needs to be deployed into GUAC
            * Ended up using the OCI registry, zarf command happens even before guac is up and running
            * Zarf has an offline OCI registry
    * Few talks on merging GUAC and AI
        * Someone asking if GUAC can have a public instance for all of projects
        * With trustify and larger ecosystem should have appetite for that
        * Using GUAC to model AI supply chains
            * SLSA for ML is not that usable - can use github actions but not the main dev flow for most 
            * The plan 2nd half of this year to get more adoption of SLSA AI
            * Once you get into one of these tools you get into others
    * Staff was looking to record interviews with folks from each project
        * Want to do it on zoom
            * Introduce yourself
            * What is the project, how is it useful
            * Where can ppl find it/participate
* Discussion around graphQL query being weird
* [Ben] Should we continue monthly Community Meetings?
    * Had less attendance in community meetings over past year and 1.0 being out, may be a good marker for community meeting
    * With public maintainer meetings, folks usually come to maintainer meetings
    * We can do it when we need it - announce it once in a while
* [Dejan] Trustify donation IP issues
    * Moving trustification/trustify to guacsec
    * Hypothesis: If we just move things that are useful would be easier for IP perspective
    * Need to donate all IP trustification/trustify, if just move the repos cant use those names for those repos without transferring IP. For the repos that are existing, we need to ask openSSF for permission to use the IP.
    * For domain names, what to do with it?
        * Domains are being used in github actions, etc.
        * We don’t have a time where it doesnt affect those processes
        * No direct concern with domains
    * Decision: just dump all repos into the GUAC repo and donate the IP as a whole to OpenSSF
* Kusari inspector installed on guacsec/guac
* CI issues
    * Make e2e tests optional
    * Integration tests for deps.dev
    * Action: Brandon to follow up with deps.dev on the [issue](https://deps.dev/go/github.com%2FMakeNowJust%2FHeredoc)
