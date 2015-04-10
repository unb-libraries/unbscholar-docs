#Current Workflow for Islandora Ingest of Electronic Theses and Dissertations

> Updated by Mike Nason // April 10, 2015

This document is intended for use within UNB Libraries and the School of Graduate Studies at the University of New Brunswick for the purpose of populating the [UNB Scholar Research Repository](http://unbscholar.lib.unb.ca). UNB Scholar utilizes software called Islandora, which is an open source platform combining the popular Drupal content management system with Fedora repository software. Hopefully, you'll have to see – or know about – as little of these things as possible. 

**Best Practices** (ie: the rules and standard procedures) for the ingest of material are now included *in the forms themselves*. If you have departmental or local rules for the ingest of content you can inquire with a supervisor or get in touch with the repository manager. These practices have been checked against those of our cataloguing department and, ideally, should cover most questions you may have. This is a *living document*, however, so if there are any questions or recommendations as you work with the content, please contact [Mike Nason](mailto:michael.nason@gmail.com) for clarification and/or assistance. 

Good luck!

<hr>

##Step 1) Login

For the time being, the login screen is *not actually present* on the first page of UNB Scholar. We are currently working on sorting out where that login option will appear. For the time being, you will need to navigate to a specific collection or perform a search for the sidebar to appear with the login fields. 

##Step 2) Navigate to the Relevant Collection for Uploaded Material

We've largely hidden the old "folder view" from general users and we may obscure it even further before too long. For the time being, after logging in you can navigate to that folder system in one of two ways.

*Method 1*

Click on the **Islandora Repository** link on any page with a sidebar. 

![Click the "Islandora Repository" Link](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis01.png)

*Method 2*

Click on an object from the collection you're currently working with. For example, click on the **Collections** dropdown and select **Electronic Theses and Dissertations**. Click on any title. From here, you can see the **Breadcrumb** listing all the directories. Clicking on a specific directory will take you to that folder. 

![The Breadcrumb Method](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis02.png)

Once you've found the folder you're working in – which should represent the department or faculty that matches the content you are uploading – you can proceed to step 3. 

##Step 3) "Manage" the Collection to Begin Uploading Process

To add content to this collection – from the directory you are currently sitting in – click on the "**Manage**" button that appears over the content within the collection. From the management pages, we can edit content, add policies, change access... all of the management of content in Islandora happens from here.  

![Click the "Manage" Tab](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis03.png)

The contents of the Manage tab looks like this: 

![The Contents of the Manage Tab](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis04.png)

For right now, we're only concerned about adding content. Click the link that says "**+ Add an object to this Collection**". 

##Step 4) Choosing the Type of Content Model

When you add content to Islandora, it will prompt the user to select which type of content they would like to add in a dropdown menu. The types of content can be changed at the collection level, but they *should* be pre-set. You should only have the option to add *Collections* and *Theses and Dissertations*. 

Select **Thesis Content Model** from the dropdown menu if you're uploading a new document.  

![Selecting Thesis Content Model from the Dropdown](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis05.png)

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

##Step 6) Copyright and "Publication"

After you fill out the metadata and clicked **Save**, you'll be asked if you'd like to attach a PDF to the entry. Clicking yes will open up a series of menu items related to the status of the document. 

![The PDF Menu after you click **Yes**](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis06.png)

Firstly, select the document for upload and click the "upload" button. Below that, you'll see options for **Document version**. For our purposes, all of these documents will be filed under "published"

The **use permission** option is to determine who one contacts for usage. Islandora is sort of set up to assume the content is being entered by the author, so you'll have to forgive the, "I own this content", type of language. We'll largely be be selecting the **contact author** option. 

Lastly, there's an option for **certifying** that we have the authority to upload the files. We do. 

It's likely to look a little like this:

![Sample PDF Credentials](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis07.png)

After we click the **ingest** button at the bottom, it will pull the content into the collection. 

#Editing Senior Reports in Islandora

It's pretty likely that we'll want to edit existing records as we go, or we'll have to make corrections to work we've already ingested. This is a slightly different process. To edit a specific item in the repository, navigate to that specific item in the repository and click the "**manage**" button. The management menu will look different.

![Managing Datastreams](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis08.png)

Sorry about the text overlap, we're working on it. 

Click on the **datastreams** button. 

From the datastreams option, we can add and remove content associated with this particular entry. For example, if we want to upload additional PDFs that have, say, copyright agreements, we may do so here by clicking on "add a datastream and following the screens that come up. To **edit metadata**, we'll need to modify the XML created when we made the object originally. That metadata was created using the **MODS schema**. 

So, to edit our metadata, look in the list for the **MODS Record**. You'll see on the right of the table that there is an **edit** button, which takes you back to the metadata entry fields you saw when you originally put content in. Edit the entry, and then save your progress. That's all there is do it. 

**On derivatives**

Islandora creates derivative files for all sorts of things. If you change the uploaded PDF, Islandora won't necessarily create a new thumbnail image or re-index the file's text record. You'll have to create new *derivatives* to do that. For any field where that might be necessary, the right-most field in the table contains a link that says **regenerate** which will update any derivatives of that object. 

#Embargos

It is possible that you will have to upload a thesis or dissertation that has some sort of **embargo**. An embargo is time period between the submission of the document itself and a later date where the material will be made available. At UNB, we have a 4 year maximum embargo available to graduate students. As of this time, it's been common practice for theses and dissertations to only have embargos placed on *print editions*. Thanks to Islandora, we can place embargos on electronic theses as well. 

From the **manage** tab of a posted thesis (currently, you have to put the thesis up before you embargo it), select **Embargo** and adjust settings from there.  

![Embargo Field](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/thesis09.png)