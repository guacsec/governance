# GUAC Maintainers Meeting: 2025-10-20

Recording: https://youtu.be/B9PQ7_5bFuc

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him

## Agenda/notes

* [Dejan] Trustify updates
    * Governance should be up to date
        * MAINTAINERs which should have admin to repos
        * Contributors which have write priv
        * Triage for managers and folks managing issues
        * Carlo is maintain on UI
        * Reuben is maintain on dependency analysis
    * Privileges on creating PRs on org level for java releaser integration
        * Have to allow on the project level and the repo level
        * The bot does bumping of versions and updating documentation: https://github.com/guacsec/trustify-da-api-spec/pull/46/files	
        * Permissions is enabled here: https://github.com/organizations/guacsec/settings/actions 
    * Created a guacsec maven namespace for central repository
        * Created a temporary project in the organization for verification in maven central
        * So github.com/guacsec is the owner of the repository
    * Minor release soon that will be posted on slack with more information 🎉
    * Ready to set up an OpenSSF webinar! Dejan to reach out to Ben to set this up.
* [Santiago] Software identifiers discussion