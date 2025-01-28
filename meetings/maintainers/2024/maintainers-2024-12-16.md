# GUAC Maintainers Meeting: 2024-12-16

Recording: https://youtu.be/y4EpSe-6ENw

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Matt Young | halcyondude@gmail.com | TAG Observability | he/him
| Kris Borchers | kborchers@linuxfoundation.org | OpenSSF | he/him

## Agenda

* Welcome new friends
    * Matt Young: Met with Mike on Friday and talked about observability and using GUAC in a couple different context such as the landscape-graph , covers quite a bit such as artifacts, commits, blogs, books, tech talks (videos), etc.
        * CNCF effort on ontology for kubernetes
        * Understanding open source project health & ecosystems
    * Kris Borchers: OpenSSF TPM listening in
* [Nathan] “Unblock Included a Handler for CycloneDX Version Ranges” ([guacsec/guac#1789](https://github.com/guacsec/guac/pull/1789))
    * Store certifyvex at package with empty string
    * Store the version range as part of statement
    * Remove graphql
    * At query time, use the version range to validate with the purls
* [Ben] Meeting next week (23 Dec) and week after (30 Dec)?
    * Will cancel both of those
* [Ben] [Agenda items](https://docs.google.com/document/d/1ImSlr_t3WNZ3zWqpmfqkw1mi6_nkv3enkQ7snWDomKA/edit?tab=t.0#heading=h.a89kkjlbgpca) for Thursday’s community meeting?
    * Expected low turnout, so will cancel
* [Parth] Discussion on issue: https://github.com/guacsec/guac/pull/2370
* [Parth] Is the SPDX SBOM valid in this issue? https://github.com/guacsec/guac/issues/2369
