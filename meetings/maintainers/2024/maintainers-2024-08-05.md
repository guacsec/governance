# GUAC Maintainers Meeting: 2024-08-05

Recording: https://youtu.be/lYt6EuIMO-g

## Attendees

| Name | Email | Affiliation | Pronouns
| ---- | ----- | ----------- | --------
| Jeff Mendoza | jlm@jlm.name | Kusari | he/him
| Ben Cotton | ben@kusari.dev | Kusari | he/him
| Mike Lieberman | mike@kusari.dev | Kusari | he/him
| Marco Deicas | mdeicas@google.com | Google | he/him
| Mihai Maruseac | mihaimaruseac@google.com | Google | he/him
| Soham Arora | arora106@purdue.edu | Purdue | he/him
| Brandon Lum | lumb@google.com | Google | he/him
| Alastair Turner | alastair.turney@percona.com | Percona | 

## Agenda

* Alastair looked at graphQL and postgres integration
    * The structure looks like a graph but
    * The queries underneath looks a bit more like a traditional SQL JOIN queries
    * Ent is depending on an unmaintained driver of postgres
        * Still unsure how big the patch will be but looking to get it done
    * Question on keeping track of changes, soft deletes. There are some things that ent supports there, and can be made to partition them, but not sure what the requirements need.
        * Time based is easy to get ent to abstract for us
        * Revocations, will take a look
        * Soft delete could be a partition and application controls how that is done 
        * Looking back a certain time, time based partitioning (postgres partman does some of that for you)
* GUAC User journey interviews ([GUAC user journey study](https://docs.google.com/document/d/18D0B0pjNu4bbeu_emzKdwGby4ci7Hi8gjJ6aZsjmud4/edit#heading=h.pcq73hkmltrn))
    * Abhishek to set up interview with bloomberg
* Rest API versioning