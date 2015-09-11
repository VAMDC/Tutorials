.. raw:: html

    <style> .red {color:red} </style>
    
.. _user-guide-portal

.. role:: red

========================
User guide for portal
========================

Introduction
============

This document is compiled to familiarise yourself with the VAMDC portal interface.  If you are not sure what the portal is and whether you should be using it, `click here <http://www.vamdc.org/activities/research/access-to-data/general-portal/>`_ for a short presentation. 

If you believe there is a mistake in this user guide or are having problems with the portal, please send an email to support@vamdc.eu

Below is a summary of the menu options displayed on the navigation bar.

Home
====

The portal entry page.

.. image:: 
   user-guide-portal/port1.png
   
The home page of the portal acts as an entry point and displays the current number of available databases.

VAMDC Databases
===============

Displays a detailed table of the available databases.

.. image::
   user-guide-portal/port2.png
   
The VAMDC databases page presents a table of the databases that are currently available through the portal; this information is provided by the VAMDC :ref:`Registry <registry>`. The columns of the table are as follows: 

Name
    The name of the database, often appended with the interface type presented to the portal e.g. :ref:`VAMDC-TAP <vamdc-tap>`. Clicking on the name of the database will take you to an external web page that contains information about the database such as a detailed description of the data it contains. 

Description 
    A brief description of the data held in the database. A more detailed description may be found by clicking the database name. 

Maintainer 
    The most recently provided email address of the person maintaining the VAMDC interface to the database. If you have any questions regarding the interface or the database, please send an email to this address. 
    
Status 
    The last recorded status of the database. Most of these VAMDC databases are not co-located with the portal so the availability of the portal does not guarantee availability of all of the databases. This column provides an indication of the status of the database; a value of OK means that the database is available and should respond to queries although be aware that the status of the database may have changed since it was last checked by the portal. 
    
Available species
    Display in a page a list of all species available in the database by clicking on « show » link.Molecules and atoms are displayed in a separated table.
    
.. image::
   user-guide-portal/port3.png
   
Disclaimer
==============

.. _disclaimer:

The first time a  new user will access one of the search formulars, he will have to accept the disclaimer below.
If he declines it, he will be redirected on the portal home page and will not be able to search data. It he accepts it, he will access the search formular.

When the disclaimer is accepted, a cookie is installed on the client computer to remember its choice. This is the only information we will keep through it.

.. image::
  user-guide-portal/port19.png
   
Advanced query
==============

.. _advanced-query:

Queries can be constructed and submitted either from this page or from the :ref:`guided query interface <guided-query>`. When a query has been submitted, you will be taken to the :ref:`Query Results <query-result>` page. 

.. image::
   user-guide-portal/port4.png
   
The query page is used to build and submit queries to the database nodes. The portal uses the information available to it (from the :ref:`VAMDC Registry <registry>`) to make sure that you cannot submit a query to a database node that does not support a particular keyword e.g. only databases that support searches on the "AtomSymbol" keyword will receive the query from the portal. Once a query has been constructed, it can be submitted to those supporting nodes using the "Find Data" button and the results will be displayed on the separate :ref:`Query Results <query-result>` page.

:red:`Query Menu`
-----------------

The query menu provides a list of grouped keywords from which to build your query; moving your mouse over the menu items will reveal the grouped keywords (e.g. atom, molecule, particle) and clicking on one will add it to the query building space. You can add as many groups of keywords as you like, including the same grouping more than once e.g. you could select the atom group of keywords more than once if you wanted to query more than one atom. Below is a list of the available keyword groups, with a brief description where necessary. 

* Species

  * Atom
  
  * Molecule
  
  * Particle
  
* Processes

  * Radiative 
  
  * Collision 
 
* Environment - includes the keywords of Temperature, Pressure and Number Density. 

* Advanced - these are not keyword groups but they do provide advanced functionality. 

  * Util (From release 12.07) - Provides a couple of extra tools for your query such as searching by "source doi" and, replicating an earlier query by not returning additions and modifications made after a provided date (only supported by some databases). 
  
  * Query editor - Allows you edit the textual form of the query which will be sent to the VAMDC databases. The query language is a modified form of :ref:`SQL <sql>`; more details can be found at http://standards.vamdc.org/queryLanguage/index.html. 
  
  * Request - Allows you to select or deselect which data (or requestables) will be returned by your query (note that most services do not support this feature). The blue disks indicate that the data has been selected and will be returned while the black disks mean that the data will not be returned; clicking the words will select or de-select the requestable. Note that selecting some requestables will result in others being selected/de-selected. 
  
  * Comments - Allows you to add comments to your query. These will not affect the query itself but can be useful if you decide to save multiple queries. 
  
:red:`Query Building Space`
---------------------------

The query building space is where your keyword groups will appear when you select them from the query menu; when you first view the query page it will be blank. Each keyword group will appear as a small form, the screenshot below shows an example with the important features annotated. 

.. image::
   user-guide-portal/port5.png
   
Entering a value/text into a keyword field will enable it in your query; some keyword fields (such as "Chemical Name" in the Molecule keyword group) have auto-complete drop down lists.
    
:red:`Database node tree`
-------------------------

The database node tree provides a detailed tree-based view of the query keywords supported by each database and provides an indication of which databases will support your current query. Moving your mouse cursor over any database name in the tree will show a small text box with the description of that database. You can expand the "node tree" for any database by clicking the triangle at the beginning of the corresponding line. This will show you a list of the keywords supported by that database and moving your mouse cursor over any of the keywords will show you a brief description of that keyword. 

Initially all of the databases entries will appear black. When you enter a value into a keyword field you will see that some databases will turn green meaning that those databases support a search on that particular keyword. If you enter values into subsequent keyword fields and see a database turn red, it means that the database does not support all of the keywords of your search and will not be included in the query. 

Below is an annotated screenshot of the node tree. 

.. image::
   user-guide-portal/port6.png
   
:red:`Submitting and saving your queries`
-----------------------------------------

The "Find Data" button is used to submit your query and take you to the query results page. If your query is not valid then the button will appear ghosted and will be non-functioning (as is the case on first visiting the page). Once you have constructed a valid query, the button will become usable. 

Guided query 
============

.. _guided-query:

Queries can be constructed and submitted either from this page or from the :ref:`advanced query interface <advanced-query>`. When a query has been submitted, you will be taken to the :ref:`Query Results <query-result>` page. 
This query method is less flexible than the advanced query interface but its use is more straightforward for users that are not familiar with the VAMDC data model.

.. image::
   user-guide-portal/port10.png
   
There are 3 search modes :
  - :ref:`Collisional processes <guided-query-collisional>`
  - :ref:`Radiative processes <guided-query-radiative>`
  - :ref:`Species <guided-query-species>`
   
   
:red:`Collisional Process`
-------------------------
.. _guided-query-collisional:

Collisional processes can be searched either with or without reaction. The search process is slightly different according to the user's choice as can be seen below.

.. image::
  user-guide-portal/port16.png
  
.. image::
  user-guide-portal/port17.png
  
.. image::
  user-guide-portal/port18.png  


:red:`Radiative Process`
-------------------------
.. _guided-query-radiative:

The user will be able to configure radiative transition parameters ( wavelength, frequency ... ), initial and final states parameters ( energies, transition probability ) and to select a list of species.

.. image::
  user-guide-portal/port13.png
   
When the first option "Transition from an energy range to another one" is selected, the corresponding form is displayed.
It is possible to define an energy interval for both the upper and lower states of the transition.
   
.. image::
   user-guide-portal/port14.png
   
If the second option "Any transition" has been selected, the previous step is skipped and the species selection form is displayed.


.. image::
   user-guide-portal/port15.png


:red:`Species`
-------------------------
.. _guided-query-species:

The query will be limited to a search by species (any number of atoms, molecules and particles). For each selected species, the user has to fill at least one field of the form.
The generated query will use a "OR" clause ( search data related to species 1 OR species 2 ... OR species n ).

.. image::
   user-guide-portal/port11.png
   
When the choices are validated, a dedicated form is displayed for each species.

.. _guided-query-species-form:

.. image::
   user-guide-portal/port12.png
   
The "Edit" button allows the user to add some new species to those that have been initially selected. 
Species can be deleted by a click on the "Remove form" link.

Some fields provide an auto completion feature, most notably for molecule names and formula.

Query Results
=============

.. _query-result:

.. image::
   user-guide-portal/port7.png
   
The query results page appears after the "Find Data" button is pressed on the query page. A description of the components follows.

:red:`Query status`
-------------------

The query status is a progress bar showing the current status of the query. When the query is in the process of running, it will indicate the number of database nodes which have responded so far.

:red:`Query control buttons`
----------------------------

The query control buttons enable you to: 

* Modify query - stops the currently running query and takes you back to the query building page. 

* Stop waiting - stops the current query from running rather than waiting for the remaining nodes to send a response. 

* Save query - saves the query that you have constructed - see :ref:`Saved Queries <saved-queries>` for further information. Unless you are logged in (see :ref:`Login and Register <login-register>`), your saved queries will only persist for your current browser session.  This is unavailable while the query is running. 

:red:`Textual view of query`
----------------------------

This is the textual form of the query that you built on the query building page. It is in the VAMDC query language which is based on :ref:`SQL <sql>`. 

:red:`Query comments form`
--------------------------

Enables you to add comments to your query which can be useful if you decide to save it. If you have added a comment to the query on the query building page, it will appear here. 

:red:`Query results table`
--------------------------

The query results table displays a summary of the data returned by each VAMDC database node after receiving the query that you built; each row in the table represents a response from a specific node. The portal does not directly receive the data from each node that matches your query, instead it receives a summary of the matching data and a web link (URL) to that data which is subsequently displayed on this table. A description of the table columns follows: 

Name 
    The name of the database node that sent the response.  
Convert
    The convert is a check-box used to select data to be sent to the conversion.
Response 
    The response indicate the status of the database node. Normally one will see 'OK' regardless of whether the database has any data applicable to your query. If your query matches a lot of data at a particular node, you may see the status as "Truncated" and a percentage of data available in parenthesis. 
Last database update
    This column provides the date of last update of the database if it is available. The column title is related to a link which gives more details on it.
Download 
    If your query matches data at a node then there will be a link in this column (hosted by the node itself) to an :ref:`XSAMS <xsams>` formatted file containing your data (please see the glossary link for more information on the XSAMS format). If you do not have any experience with the XSAMS format, you may find the :ref:`Conversion services <conversion-services>` useful. 
Species, States, Processes, Radiative, Collisions, Non Radiative 
    These columns summarise the results of your query on each individual database node.

.. _conversion-services:

:red:`Conversion services`
--------------------------

XSAMS is an advanced XML based format that manages to provide a description of atomic and molecular data between very different data sources. For these reasons, it is not well suited to be displayed directly in a web browser. The Conversion services can take the XSAMS data from database node (the result of a query) and present it to you in a more immediately convenient format e.g. a series of tables.

To send one of more query responses to an Conversion service, click the related check-box (so that a tick appears). A list of conversion services will appear (entries starting with ** are recommended for the selected data), select the conversion service that you want to use from the available list (e.g. "Table Views of XSAMS" will present the data to you as a series of web page based tables) and click "Process". After a short period of time (depending on the size of the data set and how busy the service is) you should see a link that says "Result" - click this link to see the results of the processing. 

See the screenshot below for an annotated screenshot of the Conversion services. 

.. image::
   user-guide-portal/port8.png  

Saved queries
=============

.. _saved-queries:

.. image::
   user-guide-portal/port9.png 
   
Any query you save will appear as a row in the table on this page. 
Your queries will only be saved for the length of your browser session, if you wish to save your queries between browser sessions then you must be registered on the portal and logged in (see :ref:`Login and Register <login-register>` for further information). 
From this page you can delete, clone and edit the queries as well as view the results (either directly or through an Conversion service) of any saved results. The columns in the table are described below: 

:red:`Query`
------------
    This column will show the query that you saved in VAMDC query language, which is based on SQL. In addition, there are three buttons that affect your saved query: Edit which will take you back to the query builder page, Clone which will do the same but will save as a separate query, and Delete which will delete the saved query. 
    
:red:`Comments`
---------------
    If you have added comments to your query, either on the query building or results page, they will appear in this column. 
    
:red:`Date`
-----------
    The date that you saved the query
    
The following columns are related to results from queries, only those results that contained data will be saved. If the query has been saved before it has been submitted, the database and download columns will appear blank and the results column will say "No nodes responded". 

:red:`Database`
---------------
    This column will contain a list of the database nodes that responded to your query. The check-box next to the database name is used to select data sources for the Conversion services. 
    
:red:`Results`
--------------
    This column summarises the results of the match from the corresponding node in the database column using shortened versions of the column names on the query results table. 

:red:`Download`
---------------
    This column will contain a link to :ref:`XSAMS <xsams>` data for the corresponding node in the database column.
    
Info
====

This page provides details on how to get help/support. Clicking this button will display a page with a link to these user guide and tutorial pages.

Feedback
========

Clicking this button will take you to the `VAMDC forum <http://forum.vamdc.org/>`_ website which lists all topics related to the portal

.. _login-register:

Login and Register
==================

Registration is not required but doing so enables persistent query history between sessions and email updates. 
You only need to register and login if you wish for your saved queries to be persistent between browser sessions.
To register for an account, click on the "Register" link on the navigation bar, fill in the details and click the "register" button.
To login, click on the "Login" link on the navigation bar and enter your details; selecting the "Remember Me" check-box will ensure that your login details are store in your browser so you do not have to re-enter them. 
