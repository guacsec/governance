# GUAC Maintainers Meeting: 2025-11-03

Recording: https://youtu.be/FOesGOsfqYc

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Brandt Keller | brandt.keller@defenseunicorns.com | Defense Unicorns
| Shreyas Pandya | spandya@guidewire.com | Guidewire |he/him

## Agenda/notes

* Note: meeting is switching to bi-weekly. Next meeting is 17 November
* Shreyas: question about scorecard certifier PR (https://github.com/guacsec/guac/pull/2791) 
    * Was initially designed to have two certifier implementations and switching over when needed
    * Another implementation that will supercede
        * https://github.com/guacsec/guac/compare/main...shreyasHpandya:guac:feat/add-custom-scorecard-certifer-new 
* Update from Brandt: Submitted PR on helm charts for GUAC, approved by Mike
    * Having trouble with DNS resolution in k8s for ocicollector, will open a issue/PR when investigation is done
* ADR: https://github.com/guacsec/trustify/pull/1913 
    * Review docs/adrs/00009-re-process-documents.md
