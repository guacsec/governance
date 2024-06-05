# GUAC Community Meeting: 2023-04-20

Recording not available

## Attendees

* Parth Patel (Kusari)
* Mihai Maruseac (Google)
* Brandon Lum (Google)
* Jon Zeolla (Seiso)
* Tim Miller ( Kusari )
* Dejan Bosanac (Red Hat)
* Justin Abrahms (hire me?)
* Dan Perry (Google)
* Sunny Yip (Kusari)
* Jeff Mendoza (Kusari)
* Marcela Melara (Intel)
* Ed Snible (IBM)
* Shripad (Intel)
* Yotam Perkal (Rezilion)

Apologies:
* Jacques Chester (Shopify)

## Agenda

* Introductions and welcome members!
* General Project Updates
    * GUAC Beta coming up!
* Demo demo demo
    * [GraphQL API demo](https://github.com/guacsec/guac/blob/main/demo/GraphQL.md)
    * [Compose tutorial](https://github.com/guacsec/guac/blob/main/docs/Compose.md)
    * Query CLI vuln demo
    * Deps.dev collector demo
    * [Bad Packages Demo](https://github.com/guacsec/guac/blob/main/demo/bad_packages.md)
* [Contributor ladder](https://github.com/guacsec/guac/blob/main/CONTRIBUTING.md#contributor-ladder) (mihai)
* Open chat (add items here if you want)
    * sbom-scorecard (abrahms)
        * Create collector and ingestor
    * Diff between collector vs ingestor
        * a collector takes documents from various sources and brings them to GUAC - these are just document blobs
        * The ingestor is in charge or parsing and understanding them and converting them to the guac datamodel / ontology.
* https://security.googleblog.com/2023/04/supply-chain-security-for-go-part-1.html?m=1 
    * New metadata (affected functions) on vulns with Go. Can you query Guac to understand / remove false postives
    * https://pkg.go.dev/golang.org/x/vuln/vulncheck 