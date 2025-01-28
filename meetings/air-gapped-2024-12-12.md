# 2024-12-12 Air-gapped deployment

## Attendees 

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Parth Patel | parth@kusari.dev | Kusari | he/him
| Michael Lieberman | mike@kusari.dev | Kusari | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Jeff Mendoza | jeff@kusari.dev | Kusari | he/him
| Brandt Keller | | Defense Unicorns | he/him
| Brandon Whitfield | brandon@kusari.dev | Kusari | he/him
| Sunny Yip | sunny@kusari.dev | Kusari | he/him

## Agenda

* Considerations for an air-gapped GUAC deployment (issue 2294)
* What’s the deployment mechanism? This is the easy part.
    * Helm chart and container images are a common pattern. GUAC’s images and helm chart seem pretty straightforward
    * Question: from customer experience is a Helm chart/Docker compose enough, or is bare metal a requirement?
        * There are different opinions on this. There are a lot of patterns of “save whatever images/helm charts/etc you need and bring them into the environment.”
            * The user experience tends to drop off. Are there other things that are needed, like operators?
        * Zarf (an OpenSSF tool) helps package things up and make it easier
            * A statically-compiled Go binary
            * Zarf init package (a tarball) brings what you need to run, e.g. k8s.
            * Zarf agent runs to mutate things (e.g. from docker.io/ngnix to internal.registry/nginx) without having to make manual changes
            * Day 1 - deploy it all, Day 2 - updates to the data only
* What would the workflow look like in an airgapped environment?
    * What considerations
        * Are sboms being created in an airgapped environment?
        * Controlled baseline on what is entering their environment
        * Not a lot of SBOMs are generated in an air gapped environment
        * There could be some control in an unclassified environment as well
* What are the considerations and constraints?
    * Do the pieces require external network access? How do you get data from public services into the environment?
    * Backups
    * External blob store (example s3 bucket)
        * Local k8s hosting
    * Data augmentation
        * Deps.dev
            * Big Query dump 
        * OSV.dev
            * Pull the vulns db locally - can be instrumented with zarf
            * Hostable service, file system interface where you mount the volume
clearly defined
* Static view of GUAC in an airgapped system
    * Connected side does a development
    * Air-grapped system visualizes the data
* Next steps:
    * Coordinate a meeting in January for follow-up discussion
