# GUAC Maintainers Meeting: 2025-06-09

Recording: https://youtu.be/BaF1T02v3ds

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him

## Agenda

* [Ben] GUAC + Trustify community merge update
    * LF sent some questions last week, which I shared with maintainers
    * I sent the answers on Friday
* [Ben] GUAC 1.0 update
    * GUAC blog post drafted: https://github.com/guacsec/guac-landing/pull/145
    * OpenSSF blog post with OpenSSF. They said they should be able to publish prior to our community meeting on Thursday
    * Are we ready to push the big, red button?
        * ACTION: Parth will push the big, red button after we take care of the dependabot updates for go mods
            * There was a dependabot update that was too big. Mihai closed it and opened the flakyness PRs. Dependabot should catch updates today, we hope.
* [Ben] Community meeting on Thursday: [GUAC Community Meeting Notes](https://docs.google.com/document/d/1ImSlr_t3WNZ3zWqpmfqkw1mi6_nkv3enkQ7snWDomKA/edit?tab=t.0#heading=h.486a3akal6g9)
* [Mihai] PRs for CI flakyness
    * https://github.com/guacsec/guac/pull/2667: use separate cache for jobs
    * https://github.com/guacsec/guac/pull/2656: ungroup gomod deps
