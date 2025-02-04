# GUAC Maintainers Meeting: 2025-02-03

Recording: https://youtu.be/CAPtGvQLW-Q

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him

## Agenda

* [Ben] Work with [Minder](https://stacklok.com/minder) team to evaluate GUAC against [OpenSSF Baseline](https://baseline.openssf.org)?
    * Ossf working group that is creating the openssf security baseline, criteria that projects should follow, driven by CRA.
    * We have several repositories on the guacsec org that aren’t following the same configuration
    * Minder reached out to Mike to let them help us out with getting minder set up on guacsec to help evaluate the baseline (i.,e., use GUAC as a pilot project to test-fly minder). 
    * There’s an opportunity to ingest data from minder (e.g., the has source at node would be useful for guac scans) 
    * Santiago: two aspects
        * Integrating with minder for project health
        * Ingesting minder data in GUAC
    * Parth, Santiago: It’d be useful to know the delineation between Baseline, Best Practices, Allstar etc.
    * Brandon: w/ regards to Minder, it’d be interesting to reason about having Minder produce attestations that we can then evaluate within guac to ensure that baseline is met.
* GUAC 2.0 
    * Dejan: 2.0 would like to have all the guac community working but modify e.g., the asembler and the database to support trustify usecases as well. We want to identify what were these usecases and see what is different from trustify to inform the new guac schema
    * Work on replacing the gql to the json/proto ontology (and make it fit the data model of trustify as well)
    * Parth: Replacing the cli tools is not a blocker, as long as we provide a migration tool.
    * Dejan: migration may not be the best idea, but re-consume is advisable as it’d be less problematic.
    * Ben: re-ingesting is good, but we may need to have a second option to regenerate the sbom from guac to re-ingest it. 
        * The blobstore keeps the original document, however, so this may not be needed
        * We need to document this a bit better to make sure people know this is an option/the right way to use guac 
