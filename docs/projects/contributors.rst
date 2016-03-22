**Purpose:** The Contributors page allows users to configure contributors' permissions and create View-only Links.

The Contributors page is accessible via the grey navigation bar within a project or component. All contributors on a project can
see this link. Non-contributors cannot access a project or component's Contributors page.

The top half of the Contributors page is devoted to managing contributors. The bottom half allows configuration of View-only Links.

Contributors
--------------
**Purpose:** Contributors to a project or component can make changes to the project/component's content and can be included in the
citation.

The Contributors page is divided into two parts. To the left are filtering options and to the right is a table of contributors. 

The Table section of the Contributors page has an "Add" button to the right of the title. Below the title are instructions
referring to the table below them::

    Drag and Drop contributors to change listing order.

The table has four columns: "Name," "Permissions," "Bibliographic Contributor," and a remove contributor column. When the user
hovers over a '?' to the right of "Permissions" a popover appears::

    Permission Information
    Read
    View project content and comment

    Read+Write
    Read privileges plus add and configure components; add and edit content

    Administrator
    Read and write privileges; manage contributors; delete and register project; public-private settings

When the user hovers over a '?' to the right of "Bibliographic Contributor" a popover appears::

    Bibliographic Contributor Information
    Only bibliographic contributors will be displayed in the Contributors list and in project citations. Non-bibliographic
    contributors can read and modify the project as normal.

Below the "Name" column is a list of the contributors. User images are to the left of usernames, which link to public profiles.

Contributors, by default, are listed in the order they were added, with the project creator listed first. Contributors can be re-ordered
by admins, by dragging and dropping contributor rows. After re-ordering, changes must be saved; a red "Discard Changes" button
appears to the left of a green "Save Changes" button. Clicking the "Save Changes" button opens a modal::

    Save changes?
    Are you sure you want to save these changes?
    [Cancel][Save]

Saving the changes refreshes the page and shows the new settings.

Clicking the "Discard Changes" button removes the button and text alert and reverts the changes.

If the user attempts to leave the page without discarding changes, a browser alert appears asking to confirm the choice to discard changes.
If the user attempts to add a new contributor without discarding changes, a dismissable red growlbox alert appears in the upper right
corner of the page::

    Error:
    Your contributor list has unsaved changes. Please save or cancel your changes before adding contributors.

In addition to managing project settings and contributor permissions, admins on a project can see the contents of all children of
that project regardless of the privacy setting—even if they are not explicitly made a contributor on the child components or projects.

When an admin on a parent project visits a child that they are not a contributor to, they see the project as if they were a
read only contributor, meaning they have no access to the Contributors page and have limited settings options. Contributors to
the child project, when visiting the Contributors page, see an additional section under the "Contributors" section. This section is
labeled "Admins on Parent Project." Hovering over the '?' to the right of this title shows a popover that reads::

    Admins on Parent Projects
    These users are not contributors on this component but can view and register it because they are administrators on a parent
    project.

Below the heading is a list of admins on the parent project. Their profile picture and user name are listed, linking to their public
profile. To the right of their name, under the "Permissions" column is muted text that reads "Read." Below the "Bibliographic Contributor"
column is a deactivated, emtpy checkbox. This checkbox cannot be filled in.

The left side of the screen, the filtering options, contains a text box for filtering contributors by name and several boxes to filter by Permissions and by Bibliographic Contributor status. The user can type in the "Filter by name" box and the contributor list will dynamically display only contributors who match the entered text. If no contributors match the entered text, a gray bar appears in the contributors table, along with red text, "No contributors found."

Below the filter by name field is "Permissions" and a ? tooltip. If the user mouses over the tooltip icon, he sees text explaining various contributor permissions. Below this are 3 boxes: Administrator, Read+Write, and Read. The user can click to select or deselect 1, 2, or 3 of these. The contributor list will dynamically change to display only contributors who have the chosen permissions. If no contributors match the chosen filter(s), a gray bar appears in the contributors table, along with red text, "No contributors found."

Below this is a "Bibliographic Contributor" filter and a ? tooltip. If the user mouses over the tooltip icon, he sees text explaining what a bibliographic or non-bibliographic contributor means. Below this are two boxes: Bibliographic contributor or non-bibliographic contributor. The user can select one or both of these. The contributor list will dynamically change to display only contributors who have the chosen bibliographic status. If no contributors match the chosen filter(s), a gray bar appears in the contributors table, along with red text, "No contributors found."

All of these filtering options can be used simultaneously (i.e., a user can filter for contributors named "Steve" who have Admin Permissions and are non-bibliographic contributors).

.. _permissions:

Changing Permissions
^^^^^^^^^^^^^^^^^^^^
**Purpose:** Dropdowns allow users to change permission settings for contributors, affecting what kinds of edits the contributor
can make to a project.

Below the "Permissions" column is a dropdown for each contributor. Dropdown options are: "Read," "Read+Write," "Administrator."
Users with admin or read+write permissions can change all contributors' or their own permissions, respectively. Contributors with
read permissions do not see the dropdown, just muted text stating each contributor's permission setting.

When a project or component only has one registered contributor, that contributor must be an admin. If that user attempts to change their own
permissions by selecting another option from the dropdown, a red button labeled "Discard Changes" appears below the contributor list.
Below that button is a red text alert that reads::

    Must have at least one registered admin contributor

When there are multiple contributors, if the user attempts to change permissions so that there is no admin, the same errors appear. If
there is an admin, but changes are initiated, a red "Discard Changes" button appears below the contributor list to the left of a green
"Save Changes" button. Clicking the "Save Changes" button opens a modal::

    Save changes?
    Are you sure you want to save these changes?
    [Cancel][Save]

Saving the changes refreshes the page and shows the new settings.

Clicking the "Discard Changes" button removes the button and text alert and reverts the changes.

If the user attempts to leave the page without discarding changes, a browser alert appears asking to confirm the choice to discard changes.
If the user attempts to add a new contributor without discarding changes, a dismissable red growlbox alert appears in the upper right
corner of the page::

    Error:
    Your contributor list has unsaved changes. Please save or cancel your changes before adding contributors.

If the user makes a change, but manually changes it back, the "Discard Changes" and "Save Changes" buttons disappear.

Admins can change any contributor's permission setting. Read+Write contributors can change their own setting. Read only contributors
cannot change any contributor permission settings.


Changing Biobliographic Settings
^^^^^^^^^^^^^^^^
**Purpose:** A user can be set to be non-bibliographic so that their name is hidden from the contributor list.

When a user is made non-bibliographic, their name is removed from the contributor list and the citation, regardless of their position
in the contributor list. When visiting a project overview, users will not see a non-bibliographic contributor in the contributor list.

By default, all users are bibliographic, meaning that the checkbox under the "Bibliographic Contributor" column is checked. To
make someone nonbibliographic, and therefore make their name invisible in the contributor list, an admin can uncheck the corresponding
checkbox. Changes must be saved; a red "Discard Changes" button
appears to the left of a green "Save Changes" button. Clicking the "Save Changes" button opens a modal::

    Save changes?
    Are you sure you want to save these changes?
    [Cancel][Save]

Saving the changes refreshes the page and shows the new settings.

Clicking the "Discard Changes" button removes the button and text alert and reverts the changes.

If the user attempts to leave the page without discarding changes, a browser alert appears asking to confirm the choice to discard changes.
If the user attempts to add a new contributor without discarding changes, a dismissable red growlbox alert appears in the upper right
corner of the page::

    Error:
    Your contributor list has unsaved changes. Please save or cancel your changes before adding contributors.

When a project or component only has one registered contributor, that contributor must be a bibliographic contributor.
If that user attempts to change their own settings by unchecking the "Bibliographic Contributor" box, a red button
labeled "Discard Changes" appears below the contributor list. Below that button is a red text alert that reads::

    Must have at least one registered admin contributor

Admins can change any contributor's bibliographic setting. Read+Write contributors can change their own setting. Read only contributors
cannot change any contributor bibliographic settings.



Adding Contributors
^^^^^^^^^^^^^^^^^^
**Purpose:** Adding contributors allows additional OSF users to be cited on a project or to make edits to that project.

To add a contributor, the user must be an admin on the project. The user first clicks the green "Add" button to the right of the "Contributors"
title on the Contributors page. A modal appears::

    Add Contributors
    [text field: Search by name][Search]

Below the search bar and links are two columns, one labeled "Results" and one labeled "Adding."

Users can enter the name of an OSF user into the "Search by name" field. Clicking the "Search" button or pressing the return key submits
their query. The "Results" column shows up to five recent collaborators by default, and these are replaced by search results when
a query has been submitted. If multiple pages of results are returned pagination appears in the same way that it does on the
:ref:`Watchlist <pagination>`.

To the left of each OSF user returned as a result is either a white box with a gray check mark, indicating that the user is already a contributor on the project, or a green square button marked with a ‘+’ sign. Hovering over the checkmark shows a tooltip that reads::

    Already a contributor

Hovering over the '+' button
shows a tooltip that reads::

    Add contributor

To the right of this button is the user's profile picture and name. The name links to the user's public profile.
If any employer or education information was provided in the user's profile, the most affiliation is listed below the user name.
The number of projects, if any, that the result user has in common with the searching user is listed below affiliations.

Clicking the ‘+’ button adds the result to the “Adding” column. Alternatively, the user can click the “Add all” link to
the right of the “Results” title to add the results shown on the page to the “Adding” column. When a result is moved to
the “Adding” column, it is removed from the “Results” column. Projects in the “Results” column have, instead of the green
button to the left, a grey button with a ‘-‘ sign. Hovering over the '-' sign shows a tooltip tha reads::

    Remove contributor

Clicking this button removes the corresponding result from the “Adding” list and returns it to the “Results” page it was found on.
To the right of the “Adding” title is a “Remove All” link. Clicking this link moves all added results back to the “Results” column.

If the results do not list the user being searched for, or it returns no results at all, the user can click the link to "add
[username] as an unregistered contributor. Clicking this link changes the modal contents to read::

    Add Unregistered Contributor
    Full name
    Email
    We will notify the user that they have been added to your project.
    [Cancel][Back][Add]

The user provides a name for the to-be-added contributor and an email in the appropriate fields. After clicking "Add" the
unregistered user is listed in the "Adding" column with "(unregistered) to the right of their name. The added contributor can
:ref:`claim their account <sign-up>` via email or by visiting the OSF.

The  names and profile pictures of users moved into the "Adding" column are listed under a "Name" column within the "Adding" column.
A second column on the right is labeled "Permissions."  When the user hovers over a '?' to the right of "Permissions" a popover appears::

    Permission Information
    Read
    View project content and comment

    Read+Write
    Read privileges plus add and configure components; add and edit content

    Administrator
    Read and write privileges; manage contributors; delete and register project; public-private settings

By default, "Read + Write" is selected. To change the selection, the user clicks on the dropdown and chooses a new option.

Only a “Cancel” button is available on the modal until a result has been put in the “Adding” column. If applicable, the user can then
select which components or projects they wish to add the new contributors to. To do so, the user clicks the blue "Next" button that appears.
The modal page then reads::

    Select Components
    Adding contributor(s) [username(s) to component [component name].
    Select any other components to which you would like to apply these settings.

A project tree is visible below the instructions, listing all projects/components that the user has permission to add the new contributors to.
"Select all" and "De-select all" links on the right allow the user to check an uncheck each box at once. The user can submit their changes using the
green "Add" button, or they can cancel or go "Back."

If there are no additional components to add the contributors to, instead of pressing "Next" the user has the option to submit the
changes via the "Add" button.

After adding new contributors, the page refreshes and the new contributors are listed.

Newly added contributors receive an email notifying them of the change::

    Hello [username],

    You have been added as a contributor to the project "[project name]" on the Open Science Framework: URL
    If you are erroneously being associated with "[project name]" then you may visit the project contributors page and remove yourself as a contributor.

    Sincerely,

    Open Science Framework Robot

    Want more information? Visit http://osf.io/ to learn about the Open Science Framework, or http://cos.io/ for information
    about its supporting organization, the Center for Open Science.
    Questions? Email contact@osf.io

Removing Contributors
^^^^^^^^^^^^^^^^^^^
**Purpose:** Contributors can be removed to prevent them from being listed in the contributor list or from editing the project.

Admins can remove any contributor to a project. Contributors with read+write or read only permissions can remove themselves from
a project, but not others.

To remove a contributor, the user must click the red 'Remove' button in the far right column of the "Contributors" table. 

Clicking the button pops up a modal. 

If the project or component does not have components nested within it, the modal reads:: 
    
    Remove Contributor
    Remove [username] from [Project]?
    [Cancel][Remove]

Clicking [Cancel] returns the user to the Contributors page with no changes made. Clicking [Remove] removes the contributor from the project or component. The user is returned to the Contributors page.

If the project has components nested within it, the modal reads:: 

    Remove Contributor
    Do you want to remove [username] from [Project], or from [Project] and ever component in it?
    Remove [username] from [Project]
    Remove [username] from [Project] and every component in it.
    [Cancel][Remove]

The user can select the radio button corresponding to his/her choice. If the user selects "Remove [username] from [Project] and every component in it," the red Remove button becomes a gray Continue button. Clicking [Cancel] sends the user back to the Contributors page with no changes made. Clicking [Continue] sends the user to a second modal::

    Remove Contributor
    [Username] will be removed from the following projects and/or components. 
    (list of project/components to be altered)
    [Back][Cancel][Remove]

Clicking [Back] sends the user back to the previous modal. Clicking [Cancel] sends the user back to the Contributors page with no changes made. Clicking [Remove] removes the contributor from the selected project and components. 

If the user is removing him or herself in the above scenarios, user is sent to contributors page but sees a forbidden error, with a green dismissable alert at the top of the page::
    
    You have removed yourself as a contributor from this project

.. todo:: update when this bug is fixed. "confirming will send the user to the :ref:`My Dashboard <my-dashboard>` page" 

If the user tries to remove him or herself as a contributor when s/he is the only contributor on a project, a modal appears:: 

    Remove Contributor
    You cannot be removed as a contributor. You need at least one administrator, bibliographic contributor, and registered user. 
    [Cancel]


View-only Links
--------------
**Purpose:** View-only Links allow users to share the contents of private projects.

Only admins on a project can see the View-only Links section on the Contributors page. The section is below the Contributors table.
To the right of the "View-only Links" title is a green "Add" button. Below the title are instructions::

    Create a link to share this project so those who have the link can view—but not edit—the project.

A table, empty by default, is visible below the instructions. Headers are: "Link," "What This Link Shares," "Created Date,"
"Created By," and "Anonymous."

To add a link, the user clicks "Add." A modal opens::

    Create a new link to share your project
    Link name
    Anonymize contributor list for this link (e.g., for blind peer review).
    Ensure the wiki pages, files, registration supplements and add-ons do not contain identifying information.
    Which components would you like to associate with this link? Anyone with the private link can view—but not edit—the
    components associated with the link.
    [Cancel][Create]

The user can enter a name into the "Link name" field. Names can be any length.

Users can anonymize the contributor list by clicking the checkbox next to the "Anonymize..." text.

Below the text asking "Which components..." is a project tree showing all sub-projects and components the user has admin permission on.
A "Select all" and "De-select all" option checks and unchecks all element at once.

To create the View-only Link the user clicks the blue "Create" button. The new link is shown in the table.

The link URL and title are displayed in the "Link" column of the table. If no title was provided, it is automatically titled "Shared
project link."

The project and its sub-projects and components that were shared are listed, in their tree structure, under
"What This Link Shares." Only the first two elements are listed, with the option to "Show __ more..." available as a button below the
two elements. Clicking the button shows the rest of the tree structure. The "Created Date" column lists the day and time
the link was created. "Created By" lists the admin who created the link. If the contributor list was anonymized, the "Anonymous"
column reads yes—otherwise it says no. On the far right of the table is a red 'x.' Clicking the 'x' opens a modal::

    Remove view-only link?

    Are you sure you want to remove this view-only link?

    [Cancel][Remove]

Removing the link makes the link inactive and removes it from the table.

Users can share the URL for a view only link with anyone. Anyone with the link can visit the page to see the project's contents—
even if it is private and even if they do not have an OSF account.  When a visitor follows a View-only Link there is a blue, non-dismissable
alert at the top of the page::

    This project is being viewed through a private, view-only link. Anyone with the link can view this project. Keep the link safe.

If the link was anonymous, the contributors list reads "Anonymous Contributors" instead of providing the names of the contributors. Activity
logs replace usernames with "A user." "Forks" and "Registrations" tabs are not shared via anonymized view-only links because contributors' names may be listed on these projects. Manually navigating to the Forks or Registrations page using an anonymized view-only link returns "Forbidden" error. 

"Forks" and "Registrations" are shared in non-anonymized view-only links. 