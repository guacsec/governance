# GUAC Maintainers Meeting: 2025-05-12

Recording: https://youtu.be/wHGqIQySV6A

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Dejan Bosanac | dbosanac@redhat.com | Red Hat | he/him
| Aditya Sirish A Yelgundhalli | aditya.sirish@nyu.edu | New York University | he/him

## Agenda/notes

* Community meeting on Thursday
    * Cancel this month and move next month from 19th to 12th June
* [Ben]: I’m going to ask OpenSSF ops to remove the #guac-maintainers channel since no one uses it and I don’t want to confuse people. Object now!
    * No objections registered
* [Aditya]: Pilot using gittuf
    * More information: https://github.com/gittuf/github-app/blob/main/docs/getting-started.md
        * Aditya suggests using the lightweight application and generating applications to start using code reviews. We can keep the conversation going and in a few months he can start working on a gittuf->GUAC importer.
    * Where do attestations get stored?
        * In the repo itself (git reference in `refs/gittuf`)
        * The app needs push access to the repository
    * It collects information about required approvals. Does it follow the GitHub settings?
        * Policy defines approvals for committing to protected branch and also release tags
gittuf doesn’t use any metadata like the email address, but uses the associated signing keys or an identity like <GitHub user name>+<string>
        * This policy configuration is separate from GitHub repository settings. gittuf would like to eventually query GitHub to populate those rules.
    * Is the policy also on a timeline?
        * Yes. This is where the “tuf” part of the name comes in: it was inspired by TUF. There’s a root of trust file signed with sigstore.
    * How would GUAC users consume this? How would they benefit?
        * Maintainers could use this as a secondary mechanism to ensure that controls are enforced. Users can then prove for themselves that we did the things we said we did.
        * Thinking about how exporting these values would work. For example, could these be exported directly into GUAC itself? Could tie this back into SLSA build provenance or SBOM attestation
        * gittuf has a mentorship program proposal to create a lightweight visualizer for fetching and viewing attestations from a repository
    * How is the trust boostrapped?
        * First option is the root of trust file in the repo bootstrapped out of band. Afterward, people can rotate in and out of the repository.
        * Second option is trust-on-first-use. Thinking about having other gittuf repositories witnessing a new gittuff repository like a web of trust, but that’s in the early ideation phase.
    * How long does it take to get started with the light version?
        * Just go to the GitHub Marketplace and install it to the repository
    * Brandon Lum to work on getting https://github.com/gittuf/github-app/blob/main/docs/getting-started.md set up on guac-docs repo
* Next steps for community
    * trustify openssf process
        * Ben reached out to OpenSSF and Naomi washington and kate powell are working with legal team to get the process started (heard back on Friday afternoon)
        * Dejan reached out to legal and waiting on feedback
    * GUAC Community meeting definition
        * Brandon Lum will create an initial definition 
    * OpenSSF blogpost
        * ben@kusari.dev will reach out to them about the blog post
