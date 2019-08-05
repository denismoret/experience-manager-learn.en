---
title: Chapter 3 - Authoring Event Content Fragments
seo-title: Getting Started with AEM Content Services - Chapter 3 - Authoring Event Content Fragments
description: Chapter 3 of the AEM Headless tutorial covers creating and authoring Event Content Fragments from the Content Fragment Model created in Chapter 2.
seo-description: Chapter 3 of the AEM Headless tutorial covers creating and authoring Event Content Fragments from the Content Fragment Model created in Chapter 2.
---

# Chapter 3 - Authoring Event Content Fragments

Chapter 3 of the AEM Headless tutorial covers creating and authoring Events Content Fragments from the Content Fragment Model created in [Chapter 2](./chapter-2.md).

## Authoring an Event Content Fragment

With a Event Content Fragment Model created and the AEM Configuration for WKND applied to the `/content/dam/wknd-mobile` Asset folder (via the `cq:conf` property), a Event Content Fragment can be created.

Content Fragments, which are a type of Asset, should be organized and managed in AEM Assets just like other assets.

* Use locale folders in the Assets folder structure if translation is (or may be) required
* Logically organize Content Fragments so they are easy to locate and manage

In this step, well create a new Event for `Punkrock Fest` in the `/content/dam/wknd-mobile/en/events` assets folder.

![Create a new Event Content Fragment](assets/chapter-3/create-a-new-event-content-fragment.gif)

1. Navigate to **AEM > Assets > Files > WKND Mobile > English** and create Asset folders **Events**.
1. Within **Assets > Files > WKND Mobile > English > Events** create a new Content Fragment of type **Event** with a title of **Punkrock Fest**.
1. Author the newly created Event Content Fragment.

    * Event Title: **Punkrock Fest**
    * Event Description: **&lt;Enter a few lines of description...&gt;**
    * Event Date: **&lt;Select a date in the future&gt;**
    * Event Type: **Music**
    * Ticket Price: **10**
    * Event Image: **/content/dam/wknd-mobile/images/tom-rogerson-574325-unsplash.jpg**
    * Venue Name: **The Reptile House**
    * Venue City: **New York**
  
   Tap **Save** in the top action bar to save changes.

1. Using [AEM's Package Manager](http://localhost:4502/crx/packmgr/index.jsp), install the package below on AEM Author. This package contains a number of Event Content Fragments.

   [Get File: GitHub > Assets > com.adobe.aem.guides.wknd-mobile.content.chapter-3.zip](https://github.com/adobe/aem-guides-wknd-mobile/releases/latest)

## Reviewing the Content Fragment's JCR structure

*This section is informational only and meant to socialize the underlying JCR structure of Content Fragments made from Content Fragment Models.*

![Content Fragment JCR Node Structure](assets/chapter-3/content-fragment-node-structure.gif)

1. Open **[CRXDE Lite](http://localhost:4502/crx/de/index.jsp)** on AEM Author.  
1. In CRXDE Lite, on the left-hand hierarchy menu, navigate to [/content/dam/wknd-mobile/en/events/punkrock-fest/jcr:content](http://localhost:4502/crx/de/index.jsp#/content/dam/wknd-mobile/en/events/punkrock-fest/jcr:content) which is the node representing the Punkrock Fest Event Content Fragment in the JCR.
1. Expand the [data](http://localhost:4502/crx/de/index.jsp#/content/dam/wknd-mobile/en/events/punkrock-fest/jcr:content/data/master) node.
Review in the **Properties pane** that it has a property `cq:model` that points to the Event Content Fragment Model definition.
    * **`cq:model` **=** `/conf/settings/wknd-mobile/dam/cfm/models/event`**
1. Beneath the `data` node select the [master](http://localhost:4502/crx/de/index.jsp#/content/dam/wknd-mobile/en/events/punkrock-fest/jcr:content/data/master) node and review the properties. This node contains the content collected during the authoring of an Event Content Fragment Model. The JCR property names correspond to the Content Fragment Model property name's, and the values correspond to the authored values of the "Punkrock Fest" Event Content Fragment.

## Next step

It is recommended, you install the [com.adobe.aem.guides.wknd-mobile.content.chapter-3.zip](https://github.com/adobe/aem-guides-wknd-mobile/releases/latest) content package on AEM Author via [AEM's Package Manager](http://localhost:4502/crx/packmgr/index.jsp). This package contains the configurations and content outlined in this and preceding chapters of the tutorial.

* [Chapter 4 - Defining AEM Content Services Templates](./chapter-4.md)