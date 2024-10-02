# GUAC Maintainers Meeting: 2024-09-30

Recording: https://youtu.be/LFlAdEef-YE

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him

## Agenda

* [Ben] We’ve had a lot of small releases lately. How do we want to handle those announcements?
    * Several small releases over the past couple weeks, do we want to get a blog post out for every one of them so people know they exist
    * Time cadence instead of just releases, since sometimes there’s more releases going on and less sometimes but also adding in additional things like hacktober fest, etc.
    * 2 separate channels:
        * Guac version X has been released, see release notes
        * This month/week in GUAC for community heartbeat
    * We’ll start doing a monthly update post that includes patch releases, new contributors, and other interesting notes.
* Decision on collectsub
    * Csub will not be 1.0, eventually rearchitected to a pubsub queue, etc.
    * For deps.dev this would be integrated into ingestion time
    * For collectors, we would need to figure out how to communicate use, for OCI and github collector for example:
        * 1.0
            * File collector as CLI and daemon 
            * Deps.dev and OSV on ingestion
            * OSV Certifier
        * Not 1.0
            * OCI collector
            * Github collector
* Discuss timestamping on verbs
    * E.g. clearly defined, everytime the certifier runs, it creates a new HasSrcAt node
    * Process running that’s constantly cleaning data out
    * Manage data on (for each predicate)
        * What goes in (how collectors/certifiers behave)
        * What goes out (what gets deleted / soft deleted)
        * What things are queried (what is the query policy, latest only or latest within X time)
    * Follow up with Alastair and see if they’re interesting in working on it 
* Continue backend discussions? 1.0? 
