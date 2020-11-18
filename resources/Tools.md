# Tools useful for editing metadata

## Getting Data from XML into CSV

- "[Islandora Get CSV](https://github.com/mjordan/islandora_get_csv)" by Mark Jordan at SFU: For a given islandora 7.x collection, get a CSV of all the metadata values, from Solr. By Mark Jordan.
  - This is a Drupal 7 module that must be installed on an Islandora 7 site that can access your collections and Solr in question. 
  - This gets the metadata out of Solr, not the XML directly. The way that your XML got _into_ Solr is through XSLTs in fedoraGsearch. 
  - Many sites use slurp_all_MODS_to_solr.xslt which is part of Discovery Garden's suite of gsearch configuration. This does a pretty 
    good job of naming solr fields after the XML path and attributes, for example, mods_titleInfo_title_ms. 
    However:
      - Solr does not preserve the ordering of elements. Author order will not be preserved. A common issue if coming from MARC is that composed subject headings 
      (e.g. involving a topic, a geographical location, and a temporal identifier)
      are often broken out into their component parts. From the Solr it is impossible to know which terms went together to create which headings, 
      and in what order they were composed.       
      - if you make heavy use of XML attributes in MODS, then the Solr data may either:
        - be split in an overly granular way, as sometimes attributes cause the field name to change, so columns may need to be merged, or,
        - not be granular enough, as not all attributes will cause the field names to change. (please confirm)

- "[XML2CSV](https://github.com/carakey/xml2csv)" by Cara Key at LSU: Given a directory of MODS XML files (e.g. from [Islandora Datastream CRUD](https://github.com/SFULibrary/islandora_datastream_crud),
  create a CSV with a column for every xpath. 
    - This is a suite of XSLT files and needs an XML processor. If you don't have access to Oxygen, you can use the Saxon XSLT processor as a command-line tool.
    - Multiple values, especially of subject headings, are not entirely handled.
    - Once split up, it's not possible to re-create the original XML.
    
## Editing data in CSV

- Please do not use Excel. It will mangle the data.
- OpenRefine (link to tutorial?)
