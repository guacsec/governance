# GUAC Community Meeting: 2024-02-15

Recording: https://youtu.be/vU89EE05G6E

## Attendees

* Parth Patel (Kusari)
* Brandon Lum (Google)
* Sunny Yip (Kusari)
* Michael Lieberman (Kusari)
* Marco Deicas (Google)
* Jeff Mendoza (Kusari)
* Nathan Naveen (Kusari)
* Mike Lieberman (Kusari)
* Alex Feng (Microsoft)
* Kanchan Dhamane(Guidewire)
* Marco Rizzi (Red Hat)

## Agenda

* Introductions and welcome members!
    * Alex - Microsoft, on Azure container registry team focused on container supply chain efforts
    * Kanchan Dhamane, Guidewire - work on project related to security supply chain
    * Arvind Singharpuria - part of ortellius?, came to contribute to the community
* [Parth] Flexibility of blob store and pubsub 
    * Demo use of S3 and SQS
    * https://github.com/guacsec/guac/pull/1664
* [Nathan] What is your “most critical dependency”? 
    * [Nathan] Won’t be able to actually demo it because of a couple of technical difficulties.
    * https://github.com/guacsec/guac/pull/1705 - contains the design doc
    * Output:
        * the number of dependents: the package name 
        * --------------------------------------------- 
        * 41 deb_debian_base-files 
        * 35 deb_debian_tzdata 
        * 32 golang_k8s.io/release/images/build_go-runner 
        * 32 deb_debian_netbase 
        * 17 deb_debian_libssl1.1 
        * 17 deb_debian_grep 
        * 17 deb_debian_dash 
        * 15 deb_debian_adduser
* [Marco Deicas] Google Scorecard Dashboard via GUAC
* [Brandon] Recursive search for query known 
    * https://github.com/guacsec/guac/pull/1692 
* [Jeff] Backend Test suite
    * https://github.com/guacsec/guac/blob/main/internal/testing/backend/README.md