#Faculty Profile Workflow

##Overview 

Islandora is packaged with a module called "Islandora Scholar". It gives Islandora a feature wherein faculty members can have their own "profile page" with information on that particular scholar. The left bar *ought* to contain information relevant to the faculty member such as:

- profile photo
- name
- email address
- office location
- research interests
- active/retired status
- starting/retirement date

![sample](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty01.png)

This is an example of a profile. You can see that the left sidebar is currently not displaying properly and is showing empty [dublin core](http://dublincore.org/) values instead of the intended [MADS](http://www.loc.gov/standards/mads/) record. Addittionally, a profile page contains:

- a biography
- a list of recent citations that match that user in the repository
- an [rss](https://en.wikipedia.org/wiki/RSS) subscription feed
- a featured list of other members of the faculty on the right column
- a **citations** list that shows all publications from that faculty member
- a **theses** list that shows all theses that faculty member has supervised

> **Currently**, there is much work to be done to improve the display and behaviour of the Faculty Profile feature in Islandora/UNB Scholar. It is a work in progress. Please use caution in the content you create here, as well, with an emphasis on consistent metadata entry. These forms have not been modified/improved based on cataloguing standards in the way that senior reports and electronic theses forms have. 

This document is broken into two stages for now. 

1. Creating a Faculty Profile
2. Submitting a Faculty Citation

Let's get to it. 

<hr />

##Creating a Faculty Profile

It makes sense to create the Faculty Profile before you add citations. While it's possible to add citations without a profile, the linkages between Citation and Faculty Member may go more smoothly if the profile is created first. 

###Step 1) Login

For the time being, the login screen is *not actually present* on the first page of UNB Scholar. We are currently working on sorting out where that login option will appear. For the time being, you will need to navigate to a specific collection or perform a search for the sidebar to appear with the login fields. 

###Step 2) Navigate to the "Entities" Collection

For Faculty Profiles, we need to add content to a collection referred to as "**Entities**". This collection is currently accessible from anywhere by clicking the **Islandora Repository** link on any page with a sidebar. 

![Click the "Islandora Repository" Link](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty02.png)

From here, click on the **Entities** folder. 

![Click the "Entities" Folder](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty03.png)

Unlike other collections in Islandora, **Entities** isn't really one we intend on having users browse. It contains entities for both faculties, departments, and faculty members in order to relate them using Islandora. Many of the records we view in this collection will merely have a folder logo, but represent organizations instead of collections or content. 

Because of this, there are preliminary steps to creating a single faculty member. You must *also add the faculty and department for that faculty member to the repository as well*.

###Step 4) Creating a Profile 

####Step 4.1) Faculty and Departmental Entities

In order to relate members of a specific faculty together, we need to establish relationships between a faculty member, their department, and their overarching faculty. We also distinguish by UNB campus. *If the Faculty or Department for the Faculty member does not exist, you'll need to create them.*

#####Checking to see if a Faculty or Department Exists Already

1. Click on the Campus (UNB Fredericton or UNB Saint John) you're working with. 
2. Click on **Faculties and Departments**.

![Click the "Faculties and Departments" Folder](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty04.png)

You'll notice that Faculties and Departments are not sorted hierarchically here. They do not need to be. However, relationships exist between them in Fedora – the underlying repository on which Islandora (and Drupal) sit. **If the relevant faculty *and* department exist within this collection, you may move on to step 5**. 

#####Adding Faculty and Department Entities. 

From the **Faculties and Departments** collection, click the **Manage** tab. 

![Click "Manage"](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty05.png)

Click on **add an object to this collection**.

![Click "add an object to this collection"](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty06.png)

From here, you'll have a dropdown menu that asks for the format of the content you're uploading. Select **Department MADS Form**.

![Click "MADs"](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty07.png)

You'll really only need to populate two fields here, the title of the department/faculty, and the Parent department or institution, as is shown below. 

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty08.png)

###Step 5) Entities for People

Once the entities for departments and faculties are populated, you can add an entity for a person. You'll want to navigate back to the proper directory. In this case, it would be **Entities** > **UNB Fredericton** > **Scholars** > **[Faculty](https://unbscholar.lib.unb.ca/islandora/object/unbscholar%3A6646)**. You'll see all the currently imported profiles for faculty here in this collection. To add one click the **Manage** tab.

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty09.png)

You'll want to click on **add an object to this collection** and, in the dropdown menu, select **Scholar MADS Form**.

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty10.png)

From here, fill out the form as best as possible, referring to departmental affiliation as consistently with the named collections as possible. One essential field here that we need to specifically sync our content between citation and profiles is the **identifier** field. 

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty11.png)

The **identifier** field *must match the faculty member's unb email prefix (ie: what comes before @unb.ca)*. 

Fill in as much of the content as you can in this metadata field. When done, you'll be prompted to also upload an image for their profile photo. Anything I don't have, I typically get from their UNB Faculty page. *If you're going to be doing this with faculty, please clear it with them in advance.*

###Step 6) Submitting a Citation for a Faculty Member

You'll need to navigate to the **Citations** collection. You can do this using the **Islandora Repositories** button while logged in. 

![Click the "Islandora Repository" Link](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty02.png)

From here, you can click on the **Citations** collection. 

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty12.png)

You can navigate to the appropriate collection for the faculty member whose content you are uploading. If the collection doesn't exist, you'll need to create it. The appropriate heirarchy for these collections should drill down pretty far. For example:

- Citations
	- Faculty of Science (Fredericton)
		- Department of Chemistry (Fredericton)
			- Faculty Publications
				- ````name of professor````
					- citations/records here

If you don't have all of these collections created, you'll need to create them. 

####Step 6.1) Creating Collections for Content

Navigate through the directories until you hit a collection you need to create. Click the **Manage** tab and select **add an object to this collection**.

From the dropdown menu, select **Islandora Collection Content Model**.

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty13.png)

You'll be prompted with a follow-up screen: 

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty14.png)

Make sure that you **do not enter anything in the PID field** and that you select to **inherit the XACML policy of the collection this new collection sits in**. XACML policies determine access for content to users and you want to make sure those policies are consistent with the existing content in that broader collection. 

Write the name of the new collection in the name field, and any other metadata you are particularly interested in filling out. To date, we have *no best practices* for collection metadata. Name is plenty. Eventually we may want to add more diligent descriptors or controlled vocabular. We are not there yet. 

###Step 7) Adding a Citation

One you are all the way into the collection as far up to the name of the relevant faculty member you are uploading content for, you can upload a citation. To recap, you *should* be this far in: 

- Citations
	- Faculty of Science (Fredericton)
		- Department of Chemistry (Fredericton)
			- Faculty Publications
				- ````name of professor````
					- citations/records **here**

Click the **Manage** tab and select **add an object to this collection**. You'll want to select Citation Content Model from the dropdown:

![](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/faculty15.png)

> **If you are unable to select this content model from the dropdown, the system adminsitrator will have to add it for you. This is because the current templates in islandora we have do not allow for metadata editor users who aren't using the current administrative interface to manage collection policies and determine what content can be uploaded.**

Once you have the form open, fill it out to the best of your ability. 

> *These forms are not even close to proofed or finalized. We are in the process of editing these per file type but have, to date, been focused on the ETD and Senior Reports collections and fine-tuning them. If you are unsure of what content should go where, you can open up the MODS record and check it against Library of Congress standards to determine what proper metadata should be.*

In order to **properly link faculty to their citation**, the **qualified name** metadata field must match their full Display name in the system as well as include their email prefix in brackets. For example:

- Marc Bragdon (mbragdon)

At the bottom of the form we have a section for UNB Faceting fields. None of these citation forms have been configured to match our controlled vocabulary for senior reports or ETDs yet, so please just leave them be or we'll have an organizational mess on our hands. We'll regularly check these citation forms to ensure that we've caught new uploads, or you can tell us what you've uploaded so we can correct it. This is largely a byproduct of the system not being ready or tested for this activity. 

After the form is filled out, you'll be asked to upload a PDF. If you have one and we have the rights to put it in the repository, please do so. 

That should be it. If you've properly filled out the content and matched the metadata in the citation properly, the work should show up attached to the specific scholar you're entering contact for. 

<hr />

As usual, if you have any issues please review the [support documentation](https://github.com/unb-libraries/unbscholar-docs/blob/master/support.md) and contact us with as much detail as possible. Additionally, you may want to look at other guides for theses and senior reports in Github to get a handle on the workflows we've established for those. They are much more well defined than citation workflows, although citations have a *lot* more potential metadata. 










