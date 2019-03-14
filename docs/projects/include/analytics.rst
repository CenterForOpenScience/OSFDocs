.. _analytics:

Analytics
*********
**Purpose:** provides analytics on visits, forks, links, and templates on a project.

A project's "Analytics" page is accessible from the project's "Analytics" tab in the navigation bar. The "Analytics" page provides analytics for forks, links, templates, and visits.

Counts for the number forks, links, and templates occurring from/to the project appear at the top of the page. If none have occurred, the values are 0. 

The visits appear below the forks, links, and template data. A blue dismissable alert appears above the visits::
  
    The use of adblocking software may prevent site analytics from loading properly.
    
Below the alert are four graphs displaying visitor behavior: Unique visits, Time of day visits, Top referrers, and Popular pages. Above the graphs is a filter to sort the analytics by date. Helper text next to the filter reads::
  
    Show analytics for date range

Projects are filterable by past week, past two weeks, and past month. "Past week" is selected by default. Selecting a different date range from the menu reloads and displays the visits accordingly. Analytics beyond the past month are not available. 

Analytics on visits are disabled for private projects but forks, links, and templates are still enabled. Navigating to a private project's "Analytics" page shows the page as normal but the analytics widgets are grayed out. Helper text appears above these widgets and reads::
      
    Analytics are not available for private projects. To view Analytics, make your project public by selecting Make Public from the project overview page. Public projects:
    * are discoverable
    * are citable
    * can be affiliated with OSF for Institutions partners
    * promote open practices among peers
      
    Receive data on visitors to your project by enabling Analytics and begin discovering the impact of your work.

Making the project public enables the analytics.

.. _analytics_forks:

Viewing forks
-------------
**Purpose**: The "Forks" page lists all forks that have been created from the original project, and allows users to fork the project directly from the page.

Clicking the **View all forks** link on the "Analytics" page takes the user to the "Forks" page at <https://osf.io/GUID/forks/>.

If no forks have been created from the project, the following message appears at the top of the page::
  
    This project has no forks. A fork is a copy of a project that you can change without affecting the original project.
    
If >10 forks have been created from the project, the results on this page become paginated. Both public and private forks are displayed. If a fork is private, no metadata is visible, and only the following message is listed::
  
    Private Fork

If a fork is public, the metadata appears in the following format::
  
    Fork of <project name> | Forked: YYYY-MM-DD hh:mm UTC
    <contributor lastnames>
    <description (if any)>
    
If a fork is private, it is visible to the contributors of the fork on the "Forks" page.
The fork is displayed as a public fork would be, and includes a "lock" symbol to indicate its private status.

If contributors of a fork view the fork from this list, an ellipsis button will appear next to the fork. The **ellipsis** button offers the same functions as described in the :ref:`Component formatting section <component-format>`.

A "Back to Analytics" link is located at the top of the page that users can click to return to the "Analytics" page. Helper text appears below the link to help users view the page::
  
    Forks you have permission to view are shown here.

A green "Create fork" button is located in the top right of the page. Clicking this button opens a confirmation modal::
  
    Are you sure you want to fork this project?
    [Cancel][Fork]

Clicking **Cancel** from the modal cancels the action and closes the modal. Clicking **Fork** from the modal initiates the fork. While the fork is being created, the "Create Fork" button becomes disabled and, while loading, temporarily reads: "Creating new fork." When the fork is ready, a dismissable message appears in the top right of the page::
  
    Fork status
    Your fork is being created. You'll receive an email when it is complete.
    
The user receives a confirmation email that includes a link to the fork::
  
    Your fork has completed
    The fork of <title> has been successfully created here: https://osf.io/GUID

.. _analytics_links:

Viewing links
-------------
**Purpose**: The "Analytics" page shows how many and which projects link to the current project. This page does not display information regarding projects to which the current project links. 

Clicking the "View all links" link opens the following modal::
  
    Links to this project
    Title | Authors
    [Close]
    
The project titles are linked to the projects themselves so that the user can view the project linking to the current project.    


If a project linking to the current project is private, the private project is displayed as follows in the modal::
  
    Title             | Authors
    Private Component |  Private Author(s)
    
The "Private Component" name in the "Title" column is not a link.

If a project linking to the current project is public, the public project is displayed as follows in the modal::

  Title           | Authors
  <project title> | <last name>    

If there is more than contributor on the project, the first listed author's last name appears below the "Authors" column, followed by "et al."

If the user of the private project is also a contributor on the current project, the user can view the project in the list as a regular public project.

Clicking the **Close** button closes the modal.

Viewing template copies
-----------------------
**Purpose**: This box shows users how many templates have been created based on the current project.

The total number of templates that have been created based on the current project is listed in the "Template Copies" box.
No links are included in this box.
