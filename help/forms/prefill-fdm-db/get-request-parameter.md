---
title: Get request parameter
description: Access the request parameter a form data model's prefill service
feature: adaptive-forms
topics: development
audience: developer
doc-type: article
activity: implement
version: 6.4,6.5
kt: 5815
thumbnail: kt-5815.jpg
---
# Access empID request parameter

The next step is to access the empID parameter from the url. The value of empID request parameter is then passed to the get service operation of the form data model.
For the purpose of this course we have created and provided the following

* Adatpive form Template called _FDMDemo_
* Page Component called _fdmdemo_
* Included our custom jsp with the page component
* Associated the adaptive form template with the page component

 By doing this our code in the custom jsp will only be executed when adaptive form based on this custom template is rendered
 As part of this course, we have provided you with Adaptive Form template and page component.
* [Import the package](assets/template-page-component.zip) using [package manager](http://localhost:4502/crx/packmgr/index.jsp)
* [Open fdmrequest.jsp](http://localhost:4502/crx/de/index.jsp#/apps/fdmdemo/component/page/fdmdemo/fdmrequest.jsp)
* Uncomment the commented lines. These lines do the following:
        * Writes the empID to log file 
        * Create java Map object
        * Fetch the  value of empID from request parameter
        * Put the value of empID in map object
        * Set slingRequest's attribute

* Save your changes
>[!NOTE]
>The key empID has to match with the binding value of the newhire entities get service