#UNB Scholar Ongoing Development FunStorm

It does dawn on me that I/we should be more diligent at documenting what we need fixed. It's not a trivial list of things, either. Welp, let's get right to it. Here's some things we ought to consider working on as we move forward here with UNB Scholar.

<!-- TOC depth:6 withLinks:1 -->
- [New Things](#new-things)
	- [UNB Scholar "Access Widget"](#unb-scholar-access-widget)
	- ["Check for Fulltext" Option](#check-for-fulltext-option)
	- [Moderation Queues for Ingest](#moderation-queues-for-ingest)
	- [User's "My Bookmarks" Features](#users-my-bookmarks-features)
	- [Filters for Date Behave Weird](#filters-for-date-behave-weird)
	- [Metadata](#metadata)
		- [Attribution](#attribution)
		- [Islandora Lies About Not Displaying Empty Metadata Fields](#islandora-lies-about-not-displaying-empty-metadata-fields)
		- ["Sort By" on shortlist displays for collections](#sort-by-on-shortlist-displays-for-collections)
		- ["Citations" Content Model and Metadata Edits](#citations-content-model-and-metadata-edits)
			- [Collapsable Metadata Sections Based on Type of Item](#collapsable-metadata-sections-based-on-type-of-item)
			- [New "Variant Title" field for Islandora across all content types.](#new-variant-title-field-for-islandora-across-all-content-types)
			- [Labels and Documentation for "Citation" level forms](#labels-and-documentation-for-citation-level-forms)
- [Still Kicking](#still-kicking)
	- [Second "Physical Description" link appears when editing a file.](#second-physical-description-link-appears-when-editing-a-file)
<!-- /TOC -->

#New Things

##UNB Scholar "Access Widget"

Should have a widget above an object record that uses PDF, embargo, or access to use to determine one of four statuses.

1. Open
2. Requires Login (with link to login [checks against access])
3. Embargo and release date (checks embargo)
4. Metadata Only.

We can talk about this possible feature at the next implementation committee meeting as part of a reskin/ui/framework update.

> Solves the issue of left sidebar login, prompts users for login where necessary, and doesn't make OA content appear as though login is required.

- **Action Item** // Develop.
- [ ] Requested in FogBugz, [2010](http://support.lib.unb.ca/default.asp?2010#16882)
- [ ] Resolved in FogBugz

##"Check for Fulltext" Option

UNB Scholar should allow user to check for fulltext against UNB collection.

- **Action Item** // Duh.
- [ ] Requested in FogBugz
- [ ] Resolved in FogBugz

##Moderation Queues for Ingest

We need some level of moderation for not-yet-accessible but still *in islandora* content. One potential option is that, assuming we're ingesting content into a new "collection" – say, a faculty member's folder in the *Citations* "collection" – we can edit the XACML policies to restrict access to that content for anyone who isn't an admin or metadata editor. If that content hasn't yet been tied to that scholar profile, that's not an issue. It *becomes an issue* if that scholar profile is active *and if the citations are linked to that profile* because the articles will still be listed there.

**Or**, there's an option (at least as Admin) to edit the "**State**" of an object. Head to a record, click **Manage** > **Properties** and there's an option for the "State" of an object here. The options are Active, Inactive, and Deleted. Perhaps labelling things as inactive will remove them from the list and we can have a separate metadata moderation **view** that only lists "inactive" content for the purpose of Metadata and/or copyright proofing. That would be awesome.

- **Action Item** // Figure out mideration queues for ingest to allow for metadata proofing on batch uploads.
-  [ ] Requested in FogBugz
-  [ ] Developed // Fixed
- **Action Item** // Integrate solution with batch RefWorks uploads.
-  [ ] Requested in FogBugz
-  [ ] Developed // Fixed
-  Related Requests: [597](http://support.lib.unb.ca/default.asp?597#11398)

##User's "My Bookmarks" Features

These appear to be super broken. I should be able to export a list of citations from a few different places in the UI. Here's a place to try:

https://unbscholar.lib.unb.ca/islandora/object/islandora%3A110/theses

I chose this because it also suggests that our *Theses* module we spent $10,000 on **sort of works**. You'll note that the drop down has a CSV option but selecting it does nothing. You'll also note a sub-dropdown heading thing that says "Bookmarks" because that makes a lot of sense. It's not selectable because of course it isn't.  

**Action Item** // Either fix bookmarks (we should probably contribute to fixing these), or disable them, or at least remove them from the UI for now so that people aren't trying to use them but watching the process fail.
-  [ ] Requested in FogBugz
-  [ ] Resolved in FogBugz

##Filters for Date Behave Weird

Currently, search filters operate on a **+/-** system where clicking **+** applies that filter to a search. But you can't apply, say, two date filters easily. Also, clicking on the **-** doesn't actually do anything. It's like it's one big button. You can only remove a filter by clicking the name of the filter in the search breadcrumb. That's weird.

- Can users just enter a date range if they want?
- **Action Item** // sort out solution.
-  [ ] Requested in FogBugz
-  [ ] Developed // Fixed

##Metadata

A lot of things fall under Metadata, so I'll spread these out.

###Attribution

In a number of places throughout Islandora, our default dublin core display is problematic. It's super obvious, for example, with theses. Under the record, you'll notice that the dublin core **creator** field is empty, but the **contributor** field is chalk full of both authors and everyone on their defense committee. This is *additionally problematic* when you visit a list of theses attributed to a faculty member, where the **author** field displays *only the defense committee* and not the name of the student.

- Creator field empty.
- Contributor field way overpopulated.
- **Action Item** // Fix
- [ ] Reported in FogBugz
- [ ] Resolved in FogBugz

###Islandora Lies About Not Displaying Empty Metadata Fields

Islandora has an option to suppress empty metadata fields but it doesn't work with the dublin core display enabled, because of course it doesn't.

- **Action Item** // Fix.
- [ ] Reported in FogBugz
- [ ] Resolved in FogBugz
- Related requests: [1188](http://support.lib.unb.ca/default.asp?1188#11689)

###"Sort By" on shortlist displays for collections

It would be nice to "sort by" a date in Islandora on those collection views. Maybe by date or author alphabetical?

- **Action Item** // Fix.
-  [ ] Requested in FogBugz
-  [ ] Developed // Fixed

###"Citations" Content Model and Metadata Edits

Again, there are many items here to list. Let's list some.

####Collapsable Metadata Sections Based on Type of Item

Islandora has canned metadata for a lot of different types of content but spills them all into one giant and confusing form. For example, it asks you for information *first* that would be relevant if you were recording metadata for a book. Below that, it asks for seemingly redundant metadata that is actually supposed to only be filled out if the item is a *journal*. **This is basically madness**.

- I suspect this one could be a handful.
- **Action Item** // we should have some sort of more clear use for this thing. There's a "books" content model but it's just for things going into that section using the Internet Archive Reader. I'm starting to think the best sort of plan is that content models metadata should be arranged by the **level** of the person submitting. Like:
	- faculty
		- book
		- book chapter
		- journal article
		- presentation
		- technical report
		- etc...
	- graduate student
		- theses and disserations
		- presentation
		- publication
	- undergraduate
		- senior report as type (we limit types as they come in)
		- honors thesis as type
		- whatever else sort of content... paper? project? publication?
- **This definitely needs a conversation or two around it**.
- [ ] Requested in FogBugz
- [ ] Resolved in FogBugz
- Related requests: [1821](http://support.lib.unb.ca/default.asp?1821#15645)

####New "Variant Title" field for Islandora across all content types.

I was talking to Merle about Typos on user content. I don't actually suspect we'll see much of this for books, but we might see them on regular citations and will definitely see them in Senior Reports and Theses.

So, just a title below the subtitle that would map to:

````
<titleInfo type="alternative" displayLabel="variant title">
<title>One great senior report or whatever</title>
</titleInfo>
````

That ought to do it. I can update the wording around the form once it's added.

Ideally, in the long run, if there were a variant title it would be displayed instead of the original. Or, we could choose which to display. I'm not super concerned about this in the meantime, however.

- **Action Items** // create new field.
- [ ] Requested in FogBugz, [2004](http://support.lib.unb.ca/default.asp?2004)
- [ ] Resolved in FogBugz

####Labels and Documentation for "Citation" level forms

I'll have to do the same thing to the forms that better explains what is what.

- **Action Item** // may require some jiggering systems.
- [ ] Requested in FogBugz
- [ ] Resolved in FogBugz

#Still Kicking

##Second "Physical Description" link appears when editing a file.

I know that Jake submitted a pull request that would have fixed this issue, but apparently Islandora folks have mostly been not responding to it.
