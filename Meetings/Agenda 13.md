## Islandora Metadata Interest Group Agenda
### Monday, June 13, 2016, 1-2pm EST
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
* Announcements  
* The discussion will be led by John Yobb the creator of the Metadata Analyzer module for Islandora 
* Subgroups updates
* Volunteers for next month
* Round table

#### Notes:
* Welcome everyone
* Announcements: There is a solution that was created by Mark Jordan that allows you to select parent metadata to be displayed. The module can be found on [Jira](https://jira.duraspace.org/browse/ISLANDORA-1718). Mark Jordan also released a solution to display a point on a Google maps for those objects that have a coordinates in the MODS file called [Simple Map](https://github.com/mjordan/islandora_simple_map).
* Discussion led by John: They have a 9TB machine that is growing for years to come. Currently they have 11 different multisites hosted on the machine of which 3 are in development. They have music collections, collections of photography, archives collections such as their newspaper one, air photo collections, repository collections, etc. Some content is added one at a time and some is batch loaded. The mandate is to also provide repository for other institutions as well. This is available on [one site](http://saskhistoryonline.ca/). As there are multiple people contributing, there is metadata all over the map. They wanted to see what was there and how to fix it. They asked John to create this tool called Metadata Analyzer. This module still needs work. Currently it just displays metadata. The results of the queries are stored in a database and can be looked at in the results to be used in the future for instance. You start out by adding a title, select a datastream, provide a PID. This will not drill down into subcollections right now. You add a list of comma seprated fields and click submit. Then you go to the results page. The results show the records processed such as /mods/abstract@. In the test showed by John, there was an example where there was a field with no information. This could be used to see if those records need to be enhanced. Question: do you need to include the XPath? If you use subject, it will recognize the children. It will generate the XPath statement which will make it easier to edit these files later; this would be a later component for development. Right now it just grabs fields and tells you whether they exist or not and if ther eare values these are shown. This can be used in the future to work out case sensitivity, controlled vocabularies, and facets. There are some bugs to resolve and some code cleanup and then it will be ready. Question: Is it hard to install? It is a standard Drupal module and doesn't have any dependencies. It does have a drush interface for super large collections. Question? How long was the development on this? This could be about 5 days. It would be great to be able to do this type of development. Question? Have you thought of linkng this functionality with Drupal user accounts and have a report sent to that user. Question? Can you show from the beginning again. Provide a name, datastream, PID and element. Those who implement the namespace will have problems which is a current bug. The estimated time line is by the end of summer. Question: Is there any export function? You can save the file which is just a comma separate list of the PIDs. John might ties this into Mark Jordan's PID search and replace tool to enhance and add functionality for editing. 
* Authorities subgroup: They are currently collecting use case scenarios and have 1 which is posted to the wiki. We're working on getting more posted along with the notes. They are looking for more use cases. They are also looking to the MIG to asign a priority for these use cases.
* Volunteers for next month: Jennifer will put out a call for volunteers through Islandora and touch base with those working on Fedora 4.
