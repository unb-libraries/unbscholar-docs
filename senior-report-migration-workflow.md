#Migrating Content Between Collections in Islandora

> Updated by Mike Nason // July 16th, 2015

##Overview

This documentation was created specifically with the need to migrate the [Faculty of Engineering (Fredericton) Unsorted Senior Reports](https://unbscholar.lib.unb.ca/islandora/object/unbscholar%3A6). The collection is a little weird, because it was a batch import into *RiverRun* from before our time. It needs metadata, for one... specifically under the *UNB Facets* section. Additionally, since the content was pulled in as one fat collection, it needs to be divvied up into its requisite collections. The workflow for that is as follows. 

<hr>

##Step 1) Login

For the time being, the login screen is *not actually present* on the first page of UNB Scholar. We are currently working on sorting out where that login option will appear. For the time being, you will need to navigate to a specific collection or perform a search for the sidebar to appear with the login fields. 

##Step 2) Navigate to the Relevant Collection for Uploaded Material

We've largely hidden the old "folder view" from general users and we may obscure it even further before too long. For the time being, after logging in you can navigate to that folder system in one of two ways.

*Method 1*

Click on the **Islandora Repository** link on any page with a sidebar. 

![Click the "Islandora Repository" Link](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/seniorrep01.png)

*Method 2*

Click on an object from the collection you're currently working with. For example, click on the **Collections** dropdown and select **Senior Reports**. Click on any title. From here, you can see the **Breadcrumb** listing all the directories. Clicking on a specific directory will take you to that folder. 

![The Breadcrumb Method](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/seniorrep02.png)

Once you've found the folder you're working in – which should represent the department or faculty that matches the content you are uploading – you can proceed to step 3. 

##Step 3) Select an Individual Record in Islandora

![Find a Record](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/collectionmove01.png)

Click on any record you're working on. 

##Step 4) "Manage" that Record

![Manage the Record](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/collectionmove02.png)

It's possible that you will be adding metadata to your record here. The steps for that process can be found in the (very similar) [Senior Reports Workflow](https://github.com/unb-libraries/unbscholar-docs/blob/master/senior-report-workflow.md) Guide. You'll want to do whatever metadata editing you need to perform *before* you move the record, ideally. 

##Step 5) Migrate that Record

![Migration](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/collectionmove03.png)

And on the *fifth step* we get to the actual migration. You can click on the button that says "migrate this object to another collection". You'll get text box that has auto complete. It looks like this: 

![Auto Complete](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/collectionmove04.png)

You'll notice that if you start to type something like "Department of..." the system will auto-complete. **This is where you need to be very careful**. Because Islandora has a few different collections named after specific departments, **it is very important that you confirm the persistent identifier of the collection you wish to migrate to**. Notice in the image above, there is a spot in brackets after the department name that says "unbscholar:xxxx" and the xxxx is a number. Those numbers are identifiers for the specific collection you need to migrate to. You'll have to know which collection is the *senior report* one. 

###Determining the PID of the Collection You Want to Move to. 

From the [Senior Reports collection](https://unbscholar.lib.unb.ca/islandora/object/unbscholar%3A4), you can determine the PID you are looking for. It's visible in the URL for a specific folder. You have two options here. If you mouse over the relevant folder/collection, you should see a url pop up in a toolbar near the bottom of your screen:

![toolbar url](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/collectionmove05.png)

Alternatively, you can click on the folder/collection and look at your URL bar at the top of your browser. Either way, *the last little bit of the URL is the PID*. 

![url bar](https://raw.githubusercontent.com/unb-libraries/unbscholar-docs/master/images/collectionmove06.png)

###Likely PIDs for this Collection 

I thought I'd sort out some of the gruntwork here and list the PIDs for the collections likely to come up in this specific project. 

| Department | PID | 
| ---- | ---- |
| Chemical | 6153 |
| Civil | 6155 |
| Electrical | 6151 |
| Geodesy | 6157 |
| Geological | 6370 |
| Mechanical | 6119 |
| ENG 4025 Multidisciplinary | 6372 |

After you've selected the right url in your **migration dropdown**, click migrate and the content will be moved. That's all there is to it! 

