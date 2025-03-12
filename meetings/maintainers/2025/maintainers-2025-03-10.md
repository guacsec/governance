# GUAC Maintainers Meeting: 2025-03-03

Recording: https://youtu.be/sxubpk-WOOk

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Santiago Torres-Arias | santiagotorres@purdue.edu | Purdue | he/him
| Brandt Keller | brandt.keller@defenseunicorns.com | Defense Unicorns | he/him

## Agenda

* [Michael] With things like Trustification/Trustify, is there a good way to have “levels” of GUAC?
    * For example:
        * In-memory guacone for basic functionality
        * Then docker-compose for more robust use
    * Do we have a list of use cases? (e.g. ClearlyDefined, log4j, etc) These are supported by a different complexity of deployment. With a list of use cases, we could tell people what complexity they need to meet their use cases.
        * ACTION: Ben to start drafting a use cases doc
        * Jeff: at some point, we might want to use GitHub discussions. We also haven’t gone through the issues to triage them in a while.
    * Someone at Akami mentioned they were checking GUAC out internally. Others have said they looked at it and struggled with the complexity.
    * Brandt: was looking at the experimental Helm chart. There are some gaps to fill, etc, but it was well-positioned when he wanted to turn things off when he didn’t want to run the full suite. A “GUAC lite” that can redeploy to add a new collector, etc. Is the Kubernetes best effort or something active?
        * Jeff: Nothing is set in stone. In the past, we thought about how much do we want to work on options or a system to manage individual collectors and came to the idea we don’t want to build a new workload management tool. We don’t have good examples on how to add a new collector, etc.
        * Jeff: On the “GUAC lite” site, my idea is to have a single binary, but it could run a single collector in-process.
* [Michael] People are asking how GUAC can help LF (e.g. as an integration to LFX). Asking for two separate things:
    * A per-project GUAC (or subset of GUAC)
    * LF’s foundations want a holistic view of their projects to better react to things like log4j
    * Ben: I think we want to have at least 1.0 before LF does integration work. And if 2.0 is going to break compatibility majorly, we might want to wait for that
    * Jeff: This might be a question of use cases. There’s ongoing debate about whether what we have now is 1.0 or not.
* [Michael] OSPS Baseline. We should check if we’re meeting it. It will probably eventually be what LF projects are measured against. There’s still some ambiguity about what “secret” means in different contexts. There’s talk about producing in-toto attestations for Baseline and it would be good to include those in GUAC itself.
    * Santiago: Cascading Baseline would be a cool GUAC query
    * Talking to maintainers about Baseline is that it felt more opt-in compared to Scorecard. More maintainers are engaged when they can self-attest.
