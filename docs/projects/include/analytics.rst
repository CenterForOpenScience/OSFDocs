**Purpose:** The "Analytics" page of a project is designed to provide contributors and visitors with additional information about project visits and pages.

A project's "Analytics" page is accessible via the grey navigation bar in every project. When a project is private, only the contributors
have access to the "Analytics page." When a project is public, any visitor can view the analytics. 

The "Analytics" page provides analytics for forks, links, template copies, and visitor behavior.

At the top of the page are three large boxes for forks, links, and templates::
  
       Fork       | Links to Project | Template Copies
         #                #                   #
  <View all forks>| <View all links> |

The "Template Copies" box does not have a link to view all templates made of the project.

A blue dismissable message separates the boxes from the widgets::
  
    The use of adblocking software may prevent site analytics from loading properly.
    
Below the message are four graphs displaying visitor behavior: Unique visits, Time of day visits, Top referrers, and Popular pages.

If a project is private, these widgets are grayed out and disabled. However, the boxes at the top of the page
remain enabled.

Above the widgets on the right is a date range::
  
    Showing analytics from m/d/year until m/d/year [Update]

The last month's data is displayed by default. Users can click the **Update** button to select a new date range. Clicking the button replaces
the "Showing analytics from m/d/year until m/d/year [Update]" line with "From" and "Until" fields. The "Update" button is replaced by an
"Update date range" button. Clicking inside the fields opens a calendar selector from which users can select "from" and "until" dates, respectively.
After the user has selected the new date range, they can click **Update date range** to filter the data displayed in the widgets accordingly.

The "Unique Visits" widget is a graph that displays the date (MM/YY) along the x-axis, and the number of visits along the y-axis.
Hovering over a date along the x-axis shows the following tooltip::
  
    Day Month Date Year
    Visits | #
 
The "Time of day of visits" widget is a column bar chart that displays the hour (0-24) along the x-axis, and the number of visits along the y-axis.
Hovering over an hour along the x-axis shows the following tooltip::
  
    Hour
    Visits | #
    
The "Top Referrers" widget is a pie chart that displays the top referrers to the project. A legend in the top right lists the color code next to its corresponding
means of referral. Hovering over a section of the pie chart shows the following tooltip::
  
    <referrer> | #

The "Popular pages" widget is a horizontal bar chart that displays the number of visits along the x-axis, and the popular project pages along the y-axis.
Hovering over a popular page along the y-axis shows the following tooltip::
  
    <page or filename>
    Visits | #

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
