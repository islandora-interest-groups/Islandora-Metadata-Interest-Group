# Tools useful for editing metadata

## Getting Data from XML into CSV

- "[Islandora Get CSV](https://github.com/mjordan/islandora_get_csv)" by Mark Jordan at SFU: For a given islandora 7.x collection, get a CSV of all the metadata values, from Solr. By Mark Jordan.
  - This is a Drupal 7 module that must be installed on an Islandora 7 site that can access your collections and Solr in question. 
  - This gets the metadata out of Solr, not the XML directly. The way that your XML got _into_ Solr is through XSLTs in fedoraGsearch. 
  - multiple values are 
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

- "[XML2CSV](https://github.com/carakey/xml2csv)" by Cara Key at LSU: Given a directory of MODS XML files (e.g. from [Islandora Datastream CRUD](https://github.com/SFULibrary/islandora_datastream_crud), create a CSV with a column showing the values for every xpath.
    - This is a suite of XSLT files and needs an XML processor. If you don't have access to Oxygen, you can use the Saxon XSLT processor as a command-line tool. It requires XSL version 2.0, but the [PHP libraries for XML](https://www.php.net/manual/en/book.xsl.php) don't support 2.0.
    - Workflow is multi-step and involves merging into one modsCollection file, extracting relevant xpaths, and then executing those xpaths to populate a CSV.
    - Multiple values are separated with a delimiter (see above regarding loss of ordering and correlation).
    - Once split up, it's not possible to re-create the original XML.
    - Work in progress, as it was initially developed to be generic, but re-worked to focus on the MODS to RDF mapping developed by the MIG. 

- "[Complex XML To OpenRefine](https://github.com/markpbaggett/complex_xml_to_openrefine)" by Mark Baggett at UT Knoxville: Given a directory of XML files (e.g. from Datastream CRUD), create a CSV with one column per value (including attribute values). 
    - This is a python script and can be run from the command line.
    - This creates columns not only for text values in the XML, but also attribute values.
    - is generic and can deal with any XML schema
    - It is not possible (yet?) to re-create the original XML from the flat structure.

## Editing data in CSV

- **Please do not use Excel**. It will mangle the data.
- OpenRefine (link to tutorial?)

## Getting data back out of OpenRefine

- OpenRefine can export CSVs, but can also take templates. Here is a [MODS Export Template for Open Refine](https://github.com/UTKcataloging/tenncities/blob/master/cleaned_data/remediation_files/open_refine_template.md) from UTK.
    

