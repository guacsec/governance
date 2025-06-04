# GUAC Maintainers Meeting: 2025-05-19

Recording: https://youtu.be/AgEazIGmkpE

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him
| Matt Young | halcyondude@gmail.com | CNCF | he/him
| Mario Fahlandt | mfahlandt@pixel-haufen.de | Kubermatic | he/him
| Alastair Turner | alastair.turner@percona.com | Percona | he/him

## Agenda/notes

* Welcome new friends
    * Mario - from kubermatic, doing some work for CNCF currently using GUAC to start a CNCF wide installation for all the CNCF projects get ingested in one GUAC installation. I’m using this CNCF project, what is being used - especially in context for CRA. Especially from a licensing perspective.
    * Alastair Turner - DB specialist, making open source projects work better with postgres.
* [Ben] More permission requests!
    * Triage on helm-charts: https://github.com/guacsec/governance/issues/71
        * Is this better solved by making triage access org-wide? I don’t think we’d want to do that for higher levels, but for triage I don’t see a value in doing it on a repo-by-repo basis.
        * Create triage team and have everyone with reviewer bit on it
        * Triage doesn’t have to be on the ladder formally, create a section (for those that are not on the ladder)
* Write on governance: https://github.com/guacsec/governance/issues/72
    * It would simplify handling notes, etc and the review requirement would keep me from being nefarious.
* [Ben] GUAC 1.0
    * Helm charts moved. It looks like they already have Postgres. Am I reading it correctly?
    * Draft OpenSSF blog post: GUAC 1.0 release announcement
        * We’ll want to do a GUAC post a little in advance so that there’s a link with more technical information that the OpenSSF can use
        * Whose name to put on it?
            * Mike would prefer “Ben and GUAC maintainers” if OpenSSF will work with that
            * Ben is fine with not getting credit if there’s “political” value for it. 
            * Parth should be on there since he’s done a lot of work for 1.0
            * K8s project does on behalf of x,y,z of the kubernetes project. 
    * When can we push the button?
        * We’ll probably want to know the OpenSSF blog post timeline first
        * Keep release in couple of days of each other
        * Having our rescheduled community call on June 12. 
        * Pick which commit to use for the release
        * Github collector fix should be included!
* [Matt] https://github.com/cncf/toc/issues/1709 Seeking guidance/insight on:
    * GUAC scalability, graph db(s) we should consider
    * GUAC Roadmap so we can align our Implementation plans.
    * (futures?) GUAC conformance tests (good case study for an upcoming CNCF Initiative)
* [Brandon] Trustify process (https://github.com/trustification/trustify) 
    * Ben to follow up with LF legal on the donation process.
