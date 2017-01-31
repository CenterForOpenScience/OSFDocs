.. _my-dashboard:

Dashboard
============

**Purpose:** The Dashboard provides users quick access to their projects and allows them to create new projects. 

At the top of the page, on the right side, is a green "Create new project" button. Clicking it allows a user to create a new project. A modal appears,::

	Title: (text field)
	(caret)More:
	Description: (text field)
	Template (optional)
	[Cancel][Create]

Users must type someting in the Title field but may leave the others blank. Clicking Cancel returns the user to the dashboard with no changes. Clicking Create creates the new project and displays a modal::

	New project created successfully!
	[Keep working here][Go to new project]

Clicking the "Keep working here" button returns the user to the dashboard. Clicking the "Go to new project" button sends the user to the Project Overview page of his/her new project.

Below this green button is a search box that reads "Quick search your projects." Below the search box is a table displaying the 10 most recently updated Projects and Components for which the user is a contributor. Typing in the search box filters the list below according to what is typed (pressing "enter" is not necessary). The user may type project/component names or Contributor names to filter the quick search. Below this search box is a sentence that reads "Go to My Projects to organize your work or search the OSF." In this sentence, "My Projects" and "search" are links. The user can go to "My Projects" (links to the Project Organizer) or "search" (links to osf.io/search) the OSF.  

The table of recently updated projects and components contains 3 columns: Title, Contributors, Modified. The user can sort by date last modified (ascending or descending) and Project or Component title (ascending or descending) by clicking the up or down arrows in the table heading. By default, the most recent 10 projects or components are shown. The user can click the down arrow below these 10 to produce more listings in groups of 10. 

Below the list of the user's projects is a section called "Discover Public Projects." In this section, there are two columns: "New and Noteworthy" and "Most popular." Each contains links to 5 public projects on the OSF. Below this is a button, "Search for more projects," which takes the user to osf.io/search

Below this section is a marketing section. Currently this displays information about OSF for Meetings, but it can be used to highlight other products or initiatives. 

The dashboard is accessed through the “My Dashboard” link in the :ref:`navigation bar <navigation-bar>` at the
top of the page; the url is https://osf.io/dashboard.

When logging into the OSF, the "My Dashboard" is the default landing page.

.. _organizer:

Project Organizer
******************

.. include:: organizer.rst

.. _quick-tasks:

Quick Tasks
**************

.. include:: quick_tasks.rst

.. _watchlist:

Watchlist
************

.. include:: watchlist.rst
