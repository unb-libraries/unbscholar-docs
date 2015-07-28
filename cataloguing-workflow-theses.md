#Current Workflow for Islandora Ingest of Electronic Theses and Dissertations

> Updated by Mike Nason // July 28, 2015

This document is intended for use within UNB Libraries, Cataloguing and Technical Services staff for the purpose of cataloguing the contents of the the [UNB Scholar Research Repository](http://unbscholar.lib.unb.ca). UNB Scholar utilizes software called Islandora, which is an open source platform combining the popular Drupal content management system with Fedora repository software. Hopefully, you'll have to see – or know about – as little of these things as possible. 

**Best Practices** (ie: the rules and standard procedures) for the ingest of material are now included *in the forms themselves*. This should largely be familiar to Cataloging and Tech Services staff since I mostly pulled the rules from cataloging best practice. If there are departmental or local rules for the ingest of content you can inquire with a supervisor or get in touch with the repository manager and/or the head of cataloging. These practices have been checked against those of our cataloguing department and, ideally, should cover most questions you may have. This is a *living document*, however, so if there are any questions or recommendations as you work with the content, please contact [Mike Nason](mailto:michael.nason@gmail.com) for clarification and/or assistance. 

Thanks so much for your help!

<hr>

##Step 1) Login to Islandora/UNB Scholar

For the time being, the login screen is *not actually present* on the first page of UNB Scholar. We are currently working on sorting out where that login option will appear. For the time being, you will need to navigate to a specific collection or perform a search for the sidebar to appear with the login fields. 

##Step 2) View the Google Docs Spreadsheet

![Google Docs](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/catalog01.png)

Every time we add a thesis to the repository we are also filling out a quick **Google Form** that records very basic metadata about the object. We collect the following:

- a timestamp
- title
- author
- year issued
- URL for object in repository

Additionally, we include two fields in the form for "catalogued" and "proofed". The Google forms automatically populate a related spreadsheet, which you should have access to. You'll need to be logged into Google Drive to see it. If you don't have credentials to see the sheet, contact [Mike Nason](mailto:michael.nason@gmail.com) for clarification and/or assistance. The spreadsheet looks like this:

![Google Spreadsheet](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/catalog02.png)

This spreadsheet is updated *in real time* as we add content to the repository. So, you'll have a live list of content as it is added and, providing the "catalogued" field is marked with an "x" every time a thesis is catalogued, we'll also know what theses have yet to be looked at. 

##Step 3) Click on the URL of a thesis to view the record

Each of the URLs in the spreadsheet will take you to the record in UNB Scholar without having to navigate to it individually. This should be a pretty big timesaver and will allow you to skip the steps necessary to find a record. If you weren't logged in before you did this, you'll have an opportunity to do so now. 

##Step 4) "Manage" the Document to Begin

To edit this record click on the "**Manage**" button that appears over the preview image of the first page of the thesis. From the management pages, we can edit content, add policies, change access... all of the management of content in Islandora happens from here.  

![Managing Datastreams](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis08.png)

Sorry about the text overlap, we're working on it. 

Click on the **datastreams** button. 

From the datastreams option, we can add and remove content associated with this particular entry. For example, if we want to upload additional PDFs that have, say, copyright agreements, we may do so here by clicking on "add a datastream and following the screens that come up. To **edit metadata**, we'll need to modify the XML created when we made the object originally. That metadata was created using the **MODS schema**. 

So, to edit our metadata, look in the list for the **MODS Record**. You'll see on the right of the table that there is an **edit** button, which takes you back to the metadata entry fields you saw when you originally put content in. Edit the entry, and then save your progress. That's all there is do it. 

##Step 5) Metadata Entry

We have learned a few things about metadata entry via large groups in our first run through Islandora population. While **Best Practices** are now part of the form, here are things you should always keep in mind: 

- more metadata is better; put in as much as you can,
- don't make up any metadata you are unsure of,
- if anything is still ambiguous ask a supervisor of the repository manager,
- try not to navigate away from this window... drupal isn't especially great at remembering what you were doing when you leave a window open, so...
- ... try to finish each entry in one sitting. 

*A note on Faculty/Departments*

Islandora treats Departments and Faculties as “entities”. This means there should be a consistent name for them. While the content we’re working on is historical, it’s worth noting that department or faculty names may have changed over time. For example, the *Department of Forestry and Environmental Management* was formerly known as the *Department of Forestry*. 

For the purpose of browsing and faceting, it’s important to **populate these fields with the current name of a department or faculty** and note an historical name in the **notes field**. 

> One thing that's important to note is that Islandora creates a second **Physical Description** section of the metadata form when we save the PDF. When you're working on files, they'll all end with a *redundant second physical description section*. Just ignore it. There's no need to correct what's in there. We're working on that bug as well. 

**Click "Save" at the bottom of the form once you're done.**

##Step 6) Do Catalog-y things.

Once the item is saved, I'm going to assume that you folks will be doing your own work adding those records to the knowledge base. What's important is that once you've added subject headings and catalogued the thesis in the repository, **make sure that you mark off the thesis as "catalogued in the spreadsheet**. This will ensure that we don't duplicate effort. 

##Step 7) Repeat

: ) 

<hr />

As usual, if you have any issues please review the [support documentation](https://github.com/unb-libraries/unbscholar-docs/blob/master/support.md) and contact us with as much detail as possible.