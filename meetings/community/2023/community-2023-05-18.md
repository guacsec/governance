# GUAC Community Meeting: 2023-05-18

Recording: https://www.youtube.com/watch?v=JciGSBGgzfU

## Attendees
* Mihai Maruseac(Google)
* Rebecca Metzman (Google)
* Mike Lieberman (Kusari)
* Jacques Chester (Independent)
* Tim Miller (Kusari)
* Will Armiros (Protect AI)
* Sunny Yip (Kusari)
* Shafee Ahmed (Kusari)
* Dejan Bosanac (Red Hat)
* John Kjell (VMware)
* Jeff Mendoza (Kusari)
* Jon Zeolla (Seiso)
* Ed Snible (IBM)
* Kevin Conner (Independent)
* Justin Perez (Microsoft)
* Parth Patel (Kusari)
* Ashmita (Opsmx)
* Verónica López (PlanetScale / Kubernetes)
* Raj Krishnamurthy (ComplianceCow)
* Anjali Batra(OpsMx)
* Brandon Lum (Google)
* Shripad Nadgowda (Intel)
* Satya Kiran (OpsMx)

## Agenda

* Introductions and welcome members!
    * Will Armiros - Heard about us, looking to learn more
    * Justin - Microsoft
    * Rebecca - Intern at Google
    * Anjali - OpsMx
* General Project Updates
    * GUAC Beta coming up!
* [Contributor ladder](https://github.com/guacsec/guac/blob/main/CONTRIBUTING.md#contributor-ladder) (mihai)
* Microsoft component detection presentation (Justin Perez)
    * https://github.com/microsoft/component-detection 
* Guac Rust library and Seedwing integration (dejan)
    * https://github.com/dejanb/guac-rs
    * https://docs.seedwing.io/seedwing/index.html 
    * https://docs.seedwing.io/seedwing/policies/guac/index.html 
* Understanding the guac repo and the new documentation (parth) - guac.sh 
* Discussion on Persistent database (everyone)
    * https://github.com/guacsec/guac/issues/851
    * Some suggestions
         * Apache Age
         * SQLite / Filesystem
         * Cloud spanner
         * https://duckdb.org/2021/10/29/duckdb-wasm.html
         * Parquet to help run on top of database / inmem for failures/easy persistence
    * Have a stress test suite so we can benchmark against different implementations
    * Looking at feature sets as well - like bitemporal features
    * It would be good to have the public instance be able to scale, which will make it usable for a lot of users to federate against (will lower the cost of internal use by federating to the public instance)
    * AI: Create a doc for discussion (Brandon to create)

* GUAC Office hours (GUAC TiME) - 2:00-2:30 pm Fridays bi-weekly starting on 26 May
