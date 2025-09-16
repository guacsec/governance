# GUAC Maintainers Meeting: 2025-09-08

Recording: https://youtu.be/a9MT5vk4IWA

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Jens Reimann | | Red Hat | he/him
| Ruben Romero Montes | rromerom@redhat.com | Red Hat | he/him
| Pavel Sedlak | psedlak@redhat.com | Red Hat | he/him

## Agenda/notes

* Welcome new friends
    * Pavel: Engineer on trustify at RedHat, especially on testing side
    * Rajan: Engineer on trustify team based on india
* Moving repositories: status and open questions
    * Moved bots with developer accounts
    * Most of main repos are now being transferred
    * DCO app that GUAC org is using for signed commits
    * One team with all the trustify maintainers
* OpenSSF day happenings
    * CRA interest, combining with work in Trustify and GUAC
        * What do my dependencies look like, how do i make sure i’m compliant with the CRA
        * When something goes wrong, what are the issues that I need to fix (under my responsibility vs others)
            * Mike had a talk on that 
        * SBOM related stuff
            * CISA released minimum elements
        * CRA about organizational challenges was top of mind
            * Role play scenario responding to a security incident
            * [AIxCC Results and New Open Source AI Projects To Help Secure Open Source Software](https://www.youtube.com/watch?v=MMZnU743gPI) - Jeff Diecks
        * CRA:
            * Better SBOMs, enrich it and generate a new SBOM
                * Composite SBOMs
            * For stewards under CRA, OpenSSF and LF will be considered stewards, if an organization wants to use an open source project sells something they are responsible, but LF will create requirements around security baseline
            * If i want to use an openSSF project that’s graduated, it should have some level of baseline security
* SBOM minimum elements response from GUAC community
