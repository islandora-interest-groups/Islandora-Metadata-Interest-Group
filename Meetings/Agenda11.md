## Islandora Metadata Interest Group Agenda
### Monday, April 11, 2016, 1-2pm EST
### 
---
* Chair: Amanda Lehman
* Notetaker:  Jennifer Eustis

---

#### How to Join the Meeting  
* Meeting URL: https://uconn-cmr.webex.com/uconn-cmr/j.php?MTID=m2c31587beca52005bdf3c0a3b4607a50
* Audio via Telephone: 1-415-655-0002, code: 649 380 345

---

#### Agenda Items:
* Welcome and introductions
* Brief summary of new format for MIG: The Metadata IG now integrates discussions as well as round tables. Each month a volunteer leads a discussion on a topic of interest. The goal is to learn new ideas and network. The round table is another opportunity for attendees to ask questions, share information, and learn about new approaches. This new format will also include reports from the subgroups. Members are encouraged to participate in the subgroups which can be found on our wiki.
* The discussion will be led by Jennifer Eustis on tools for metadata migration and review 
* We will hear any updates from subgroups.
* Next month will be led by Martha Tenney on customizing the manuscript solution pack.

---
#### Notes:

Results from last discussion: Jennifer is reading Learning Sparql. http://www.learningsparql.com/ 

### Jennifer's Discussion of tools for metadata migration/review

She is not a programmer! Started as Metadata librarian with a skill base of Marcedit, text editor, ilf.
Migration from ContentDM to Islandora required a whole new toolset:
##### Use Open Refine for processing and migration
* Data profiling and cleanup
(Been under lots of different umbrellas, different platforms.  Began with Freebase (still works on their platform) - to Google Refine, then to Open. 
Not using Linked Data yet, used for cleanup and export with templates.)
* Save spreadsheets as text to avoid dates as timestamp.
* Get rid of nulls - when loading into OR.
* Regular Expressions
##### Workflow for ContentDM to Islandora Metadata Processing
1.  Contentdm exports as spreadsheet
2.  Cleanup and export as text, bring into OR
    - Removal of Nulls:
        - Loading Dataset: Preview Screen
        - Uncheck store blank cells as nulls (at bottom)
3.  Process, cleanup with Regex and export as XML Template 
    - Make it easier by saving your template for spreadsheet and export (not re-doing cells every time).
4.  Import to Oxygen and process ampersands, etc.
    - XSL Transform (version 2) - Jennifer will share this in github.
    - Create Individual MODS files with filename for group ingest into Islandora.
(Result-document: href=file structure (includes MODS) - creates folder with filename as assigned.)
    - Oxygen allows you to run a transformation on an entire folder (if all files have same structure).
Harvest, Masterfile, Transform.
(considered Python script from spreadsheet to mods, but cleanup is important in these steps)

* Notes: 
    - Similar to other metadata workflows in MarcEdit - but different tools.
    - 20,000 records (small batch relative to some) - other worflows (python) might be better for larger batches.
    - Different stages of cleanup/manipulation: XSL is useful for iterating through/creating topics, Regex for removing semicolons to avoid empty topics.

##### Review Process.
* Dublin Core harvest produces 60+ datasets to import into OR all at once
* Transformation to correct fields with the same name, ensures that each column header has unique name (simplify data processing)
* Profile data
* Facet to export
* Note: harvest is 38k records, transformation is serialized therefor slow! 
Python would be a useful tool

##### Other Discussion
Question about Compound objects (manuscripts) in migration
* Jennifer: Batch load children but manual parent relationship, a half-half project to make parent-child associations. 

Question: how many people review their metadata?
* Not heard of it (Erinn)
    - Migration usually includes cleanup of metadata, not always a realistic view of metadata - migration sets profile.  
* Jennifer’s policy: review of whole system includes metadata
Search for trends, find correction and try to maintain standards (example of dates w/ W3 standard).
    - MODS standards 3-dimensional objects
* DPLA metadata Harvest increases exposure and improves metadata - big plus.
    - Different flavors of schemas (used differently by various individuals) which creates collisions.
    - Experienced pushback
    - DPLA is item-level discovery, versus collection...hard to separate and shift from collection to item. 
* Bulk metadata update is still a stumbling block. 
   - Cleanup is important before, hope to get it right first, but bulk metadata update is not easy.
* Erinn’s Developers iteratively run drush scripts for metadata cleanup:
    - Cleanup, review, catch more issues, run another script.
    - Ticketing system is useful for tracking

* Try to find contentDM migration kit.
* Thought about IR migration kit. To scholar!

Call from Erinn for hands-on demo at Islandora conference 2017.
    +1 from Amanda.

UWyoming takes ILS records as Marc export and creates MODS with marcEdit - 
- tasks do other edits? Automatic cataloging changes.
- LOC transform from MarcEdit is often edited.
    - Dates
    - Subjects are not good.

##### Update on authorities Subgroup (Kevin)
* Managing from w/in Islandora
* Developing Use Cases for CLAW development
* Importing authority Records
* Managing updates as maintained in id.gov, etc.
* Autofill for catalogers from authority, and propagation of updates
* See minutes in GitHub.

##### Chat Links
* https://github.com/islandora-interest-groups/Islandora-Metadata-Interest-Group
* xsl:result-document
* https://groups.google.com/forum/#!searchin/islandora/crud/islandora/q1udVKoh194/12SFxMw0KAAJ
* https://groups.google.com/forum/#!searchin/islandora/migration/islandora/BAPes792bpo/tIK-G15UCgAJ
* Here is a video for how to create tasks in MARC Edit <https://youtu.be/vOjGdkI_ft8>
