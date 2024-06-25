# GUAC Maintainers Meeting: 2024-06-24

Recording: https://youtu.be/tjDIXDElhd4

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari |he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Narsa Chelluri | narsa@kusari.dev | Kusari | he/him
| Soham Arora | arora106@purdue.edu | Purdue |he/him
| Brandon Lum | lumb@google.com | Google | he/him

## Agenda

* [Parth] https://github.com/Percona-Lab/pg_tde
    * https://www.percona.com/blog/adding-transparent-data-encryption-to-postgresql-with-pg_tde-please-test/
    * https://www.percona.com/blog/why-postgresql-needs-transparent-database-encryption-tde/
* [Parth] Deletion of nodes discussion [low priority] 
    * Context around OSV certifier, keep on creating certifyVuln nodes, keep creating things, might need to handle to prevent churn in unused nodes.
    * Created a quick POC here: https://github.com/guacsec/guac/compare/main...pxp928:poc-delete-node?expand=1
    * Delete certifyVuln, hasSBOM (and all predicated below it) and hasSLSA

## Opens (pending)

* Create a list of topics/issues for Percona to help us with (Postgres/ENT)
    * How to archive data efficiently
    * Implement PG TDE
    * Can postgres keep track of mutations?
        * For example, deletion
* [Parth] Included a Handler for CycloneDX Version Ranges
    * https://github.com/guacsec/guac/pull/1789
    * Handle version range resolution without querying graphQL on ingestion
* Authentication/Authorization on graphQL
* CSUB re-architecture? 


