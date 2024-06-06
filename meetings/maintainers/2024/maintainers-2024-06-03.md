# GUAC Maintainers Meeting: 2024-06-03

Recording URL: https://youtu.be/iJC8eqknBoA

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Fotis Georgatos | kefalonia@gmail.com,fotis@cern.ch | CERN |he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Narsa Chelluri | narsa@kusari.dev | Kusari | he/him
| Soham Arora | arora106@purdue.edu | Purdue | he/him
| Brandon Lum | lumb@google.com | Google | he/him

## Agenda

* Guacanalyze PR Feedback on https://github.com/guacsec/guac/pull/1809
* Identifier discussion

## Meeting notes

* PR/issue discussion:
    * Fix generate code for linter [#1940](https://github.com/guacsec/guac/pull/1940)
    * add ability to have search depth in query known [#1692](https://github.com/guacsec/guac/pull/1692)
    * remove GetMatchFlagsFromPkgInput helper as it was not needed for isDependency [#1933](https://github.com/guacsec/guac/pull/1933)
    * Different changes to pagination and whatnot
* After these are merged, shall we release:
    * Version considered 0.7<x<1.0
* Brandon: Process-wise question
    * Should we define rules/checklist for verbump or so whenever graphql features change
    * Ideally, there should be some automation around it
    * PR Checkbox: code is generated and there’s a new graphql operation
