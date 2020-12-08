# Ideas and Topics #

Main users/audience: co-conveners

Purpose: keeping track of topics, ideas, etc. that we want to bring to MIG

-------------------------------------------------------------------------------

## Topics to discuss ##

  * Needs around multilingual metadata ([discussion started on #islandora8 Slack, 2020-12-04](https://islandora.slack.com/archives/CM5PPAV28/p1607114723484000) and moved to new [#multilingual Slack channel](https://islandora.slack.com/archives/C01GL883725/p1607117460000400))
      * Most of the discussion here is pretty technical so far. I.e. how one might achieve multilingual metadata Islandora 8. From the metadata perspective, how would we want multilingual metadata to work?
  * Are there any other types of metadata beyond descriptive and technical that we want to discuss? Preservation, admin, ?
  * Integrations/metadata reuse and metadata implications
      * inclusion in discovery systems
      * harvesting by aggregators
      * linked data ecosystem interoperability plans/pipe dreams
  * Permissions/authentication needs for metadata admins vs. metadata entering users
      * Seth Shaw shared their [permissions for metadata managers vs. creators Google Sheet](https://docs.google.com/spreadsheets/d/1sdZRWPFHau-8cT8ntL0dvaBAXc0nUYLbMZTQQyweywE/edit?usp=sharing) in [Slack](https://islandora.slack.com/archives/CM9CVQWJ0/p1605558976092700)
      
## Docs, etc. to produce ##

  * Wireframes/etc. for desired technical metadata functionality/forms (?) - 
  
## Presentation/etc ideas ##

  * Deep dives on particular metadata-adjacent topics. Perhaps we could request "Explain it like I'm not a developer" explanations from technical folks on how things work under the hood and use this to create non-technical documentation that would help metadata folks understand the whole metadata environment of I8: display, search, browse/faceting, mapping for metadata harvest/reuse (OAI-PMH, RDF (?)), etc. Possible topics: 
      * Solr - basically what is it? How do node fields get mapped to it? What are the options for controlling how node fields get indexed? How does this impact the user experience (what facets are there, etc)
      * FITS/technical metadata - we sort of talked about this like everyone was familiar with it, but it might be of interest to look under the hood a little bit. What does it do? When and how? What does it produce?
      * Drupal data model - data types, data storage, implications, etc. What's a node? Field? Field type?  --- this could be fleshed out more, but basically it's key-value pairs all the way down as I learned from watching [this presentation](https://www.morpht.com/blog/drupal-8-architectural-paradigms-typed-data-api) (which is more dev-centric, but helped me understand some things about how field types work)
      * Drupal views, contexts, etc. What are they? What do they do? How can they be leveraged for metadata?
      * Islandora RDF - How is it generated? What are the constraints on it? (no blank nodes, etc?) Where does it go? What does it do? How can it be accessed? Can it be accessed? What can you do with it? What can users do with it? Etc.
      * How to write a good issue/ticket/use case/etc
  * Islandora Workbench

      
***(KMS editorial on the "deep dives" idea)*** In the 2020-11-16 meeting Tillay said one of the things they'd like developers to know is "I don't understand your answers." We are working together on this project, and we cannot contribute our expertise and learn to communicate better with devs if they can't explain the software and its behavior in a non-dev comprehensible way. We as metadata folks cannot make good metadata decisions without a fuller understanding of the implications of those decisions in the system. If things aren't documented, then how are we supposed to learn? If things are documented, maybe these sessions could be "Here's where the documentation on this is. What questions are not answered by that documentation? What else needs to be in this documentation for a non-dev human to understand it?" --- Basically, I think whenever in a MIG meeting a technical topic is thrown around, I think we could take a temperature check of the room to see if people need an explanation. That explanation could happen there in the moment, and/or documentation links could be given, and/or it could be flagged as a topic that needs a deep dive. But I think we currently have a dynamic where a lot of the people in the room who the group is ostensibly for (metadata professionals working in Islandora) can't fully participate and contribute because so much of how I8 works is fairly technical/murky/cryptic/complex. I say that as a cataloger/metadata person who has become more a developer than anything else, and I find myself extremely reticent to have a strong opinion about anything or jump into a lot of discussions because I still don't feel like I understand Drupal and Islandora8 very well.
