# GUAC Maintainers Meeting: 2025-07-28

Recording: https://youtu.be/1cBcqLROOsI

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Jens Reimann | | Red Hat | he/him
| Michelle DiPalma | | Red Hat | she/her
| Ruben Romero Montes | rromerom@redhat.com | Red Hat | he/him

## Agenda/notes

* Welcome new friends
    * Michelle: product manager for Red Hat product based on Trustify
    * Jens: software engineer working on Trustify/Trustification, mostly on managing advisories and SBOM data
    * Ruben: software engineer that joined the team a few months ago. Works on dependency analytics
* Trustify Dependency Analytics Demo (currently downstream-only)
    * Originally conceived as a IDE extension, but can be added to CI pipelines
    * Scans for vulnerabilities in dependencies across several ecosystems
    * Next version will support multiple sources (currently uses OSV via Trusted Profile Analyzer: Red Hat’s product based on Trustify)
    * Red squiggly line: vulnerabilities exist
    * Blue squiggly line: no vulnerabilities, but Red Hat provides a version
    * Provides quick fix recommendations in a tooltip
    * HTML report includes a list of vulnerabilities with details
        * Includes count of direct and transitive dependencies
    * What’s next:
        * AI model cards (POC coming in August)
            * provide metrics for LLMs used in the application
            * Will recommend guardrails so that users can make informed decisions
        * IDE Chat integration/MCP server (pre-POC)
            * “Fix in chat” prompts
            * Collect vulnerability data and identify how vulnerabilities affect the code/configuration
            * Apply remediations or workarounds, recommend upgrades