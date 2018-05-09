**Purpose:** Project settings allow users to configure the project settings and their notifications for that project.

The project "Settings" page is configured differently depending on the contributor's level of permissions.

If the contributor has admin or read+write permissions, they see eight sections on the "Settings" page: "Project," "View-only Links," "Access Requests," "Wiki," "Commenting," "Email Notifications," "Redirect Link," and "Project Affiliation / Branding."

The "Settings" page has a sidebar that the user can use to navigate through the sections of the page.
  
Additional sections are shown if the project is public.

If the contributor has read-only permissions, the sidebar is not visible and only the "Email Notifications" and "Project Affiliation/Branding" sections are visible. The read-only contributor can configure their notification preferences in the "Email Notifications" section but will only have view-access to the "Project/Affiliation/Branding" section. This section reads::
  
    Project Affiliation/Branding
    Contributors with read-only permissions to this project cannot add or remove institutional affiliations.
    Projects can be affiliated with institutions that have created OSF for institutions accounts. This allows:
    * institutional logos to be displayed on public projects
    * public projects to be discoverable on specific institutional landing pages
    * single sign-on to the OSF with institutional credentials
    * FAQ (links to help guides' landing page)
    
    Available institutions:
    [instutional logo][institution]

If the user is an admin on the parent project but is not a contributor on a component, only the "Email Notifications" and "Project Affiliation/Branding" sections will be visible on the component's "Settings" page. The admin is not, however, a contributor to the component. The component's "Contributors" tab is not visible to the admin. The admin can configure their notification preferences in the "Email Notifications" section of the component's "Settings" page. However, the admin has view-only access to the "Project Affiliation/Branding" section. This section reads as follows::
  
    Project Affiliation/Branding
    Contributors with ready-only permissions to this project cannot add or remove institutional affiliations.
    
    Affiliated Institutions:
    [instutional logo][institution]

If the contributor on the parent project has read or read+write permissions, the component's "Settings" tab will not be visible.

Project/Component
-----------------
**Purpose:** The "Project" or "Component" section allows the user to update the category, edit the title or description, or delete the project/component.

The "Project" or "Component" section is formatted in the following way::
  
    Category [drop-down menu] (for descriptive purposes)
    Title:
    [title field]
    Description:
    [textbox with the word "Optional" displayed]
    [Cancel][Save changes]
    
    A project cannot be deleted if it has any components within it. To delete a parent project, you must first delete all child components by visiting their settings pages.
    [Delete Project/Component]

In the "Category" subsection, the admin can click inside the drop-down menu to select a category to assign to the project. The available categories are: "Analysis," "Communication," "Data," "Hypothesis," "Instrumentation," "Methods and Measures," "Procedure," "Project," "Software," "Other," "Uncategorized."
The "Project" category is selected automatically for all projects, and the "Uncategorized" category is selected automatically for all components.

When the admin selects a new category and clicks **Save Changes**, the following green confirmation message appears below the "Cancel" and "Save changes" buttons::

  Successfully updated project settings.

Leaving the page without cancelling or clicking "Save Changes" produces a browser warning::

  Confirm Navigation.
  There are unsaved changes in your project settings. Are you sure you want to leave this page?
  [Stay on this page][Leave this page]

For admins and read+write contributors on a project or component, the user can edit the title and description in the "Project" or "Component" section.

When the user makes changes to the title and/or description and clicks **Save Changes**, the following green confirmation message appears below the "Cancel" and "Save changes" buttons::

  Successfully updated project settings.

Leaving the page without cancelling or clicking "Save Changes" produces a browser warning::

  Confirm Navigation. There are unsaved changes in your project settings. Are you sure you want to leave this page? [Stay on this page][Leave this page]
  
Deleting a project
^^^^^^^^^^^^^^^^^^

Only admins can delete a project or a component. When the admin clicks the **Delete project** or **Delete component** button, the following modal appears::
  
    Are you sure you want to delete this project/component?
    It will no longer be available to other contributors on the project.
    Type the following to continue: (confirmation word)
    [textbox]
    [Cancel][Delete]
    
The modal instructs the admin to type a confirmation word into the textbox—this word changes each time the user visits this modal.
This field is case sensitive.

After the admin types the confirmation word into the textbox and clicks **Delete**, the project or component will be deleted. If the admin deleted a component, then they will return to the "Project Overview" page. If the admin deleted a project, then they will return to their :ref:`dashboard <dashboard>`. The following green dismissable confirmation message will appear in the top left of either page::
  
   Project/Component has been successfully deleted.

If the admin types the wrong word into the textbox, a red, dismissable alert appears in the top right of the page::

    Verification failed
    Strings did not match
    
Deleting a project with nested components
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A user must be an admin on the top-level project and all nested components in order to bulk delete them. When a user wants to delete a project or component that has nested children, the following modal appears upon clicking the **Delete project** button::
  
    Delete Project
    It looks like your project has components within it. To delete this project, you must also delete all child components
    Select: All components
    [list of components]
    [Continue]

Below the "All components" link is a list of the nested components. Clicking this link selects all components in the list. Alternatively, each component has a check box to its left that the user can select. However, all components, including the top-level project, must be selected in order for the parent project/component to be deleted. If a component is left unchecked, the blue "Continue" button will be grayed out and unclickable. 

If a user is not an admin on all of the nested components, the checkboxes next to the components where they are *not* an admin will be disabled. If a component is private, and they are not a contributor at all, a closed lock symbol will appear to the left of the component name, and the component name will read "Private Project." When a contributor is a non-admin on any of the listed components, clicking the **All components** link will select only the top-level project (and any components where they *are* an admin). If the user hovers over a listed component where they are not an admin, the following tooltip appears::
  
    You must have admin permissions on this component to be able to delete it.

If the user is an admin on all of the nested components, and they select all checkboxes in the modal, the "Continue" button will become enabled, and the user can click **Continue**.

After clicking **Continue**, the "Delete Project and Components" modal will appear::
  
    Delete Project and Components
    The following project and components will be deleted
    [list of projects/components]
    Please ntoe that deleting your project will erase all your project data and this process is IRREVERSIBLE.
    Type the following to continue: (confirmation word)
    [Back][Cancel][Delete]
    
Clicking **Back** takes the user to the previous "Delete Project" modal. Clicking **Cancel** closes the "Delete Project and Components" modal and cancels the delete process.

If the user enters a word that does not match the confirmation word, or if the user clicks **Delete** without providing the confirmation word, the modal closes, the project/components do not get deleted, and the following red, dismissable error message appears in the top right of the page::
  
    Verification failed
    Strings did not match

When the user enters the confirmation word into the text field, and clicks **Delete**, a temporary loading message appears::
  
    Deleting project

This message gets replaced by the following dismissable modal::
  
    Project has been successfully deleted.
    [OK]

Clicking **OK** takes the user to their dashboard.

Select Add-ons
--------------
See :ref:`the information about add-ons here <add-ons>`.

View-only Links
---------------
**Purpose**: View-only Links allow users to share the contents of private projects with non-contributors.

View-only links can also be configured in the project's :ref:`"Contributors" tab <contributors>`. If a view-only link is created via the "Settings" tab, the link will be listed in the "View-only Links" section on the "Contributors" page.

Only admins on a project can see the View-only Links section on the Contributors page. The section is below the Contributors table.
To the right of the "View-only Links" title is a green "Add" button. Below the title are instructions::

    Create a link to share this project so those who have the link can view—but not edit—the project.

To add a link, the user clicks "Add." A modal opens::

    Create a new link to share your project
    Link name
    Anonymize contributor list for this link (e.g., for blind peer review).
    Ensure the wiki pages, files, registration forms and add-ons do not contain identifying information.
    Which components would you like to associate with this link? Anyone with the private link can view—but not edit—the
    components associated with the link.
    [Select all] [Deselect all]
    [Cancel][Create]

The user can enter a name into the "Link name" field. Names can be any length.

Users can anonymize the contributor list by clicking the checkbox next to the "Anonymize."

Below the text asking "Which components..." is a project tree showing all components on which the user is an admin.
A "Select all" and "De-select all" option checks and unchecks all elements at once.

To create the View-only Link the user clicks the blue "Create" button. The new link is shown in a table. While the link is being created, the "Create" button temporarily reads "Please wait."

When the link is created, a table appears below the "Add" button that displays the information for the link.

The link URL and title are displayed in the "Link" column of the table. If no title was provided, it is automatically titled "Shared
project link." The view-only link is provided below the name with a button the user can click to add the link to their clipboard. Clicking the "copy to clipboard" button brings up a tooltip that says: Copied!

The project and its sub-projects and components that were shared are listed, in their tree structure, under
"Shared Components" Only the first two elements are listed, with a down arrow that the user can click to show more. The "Created Date" column lists the day and time
the link was created. "Created By" lists the admin who created the link. If the contributor list was anonymized, the "Anonymous"
column reads yes—otherwise it says no. On the far right of the table is a red "Remove" button. Clicking the **Remove** opens a modal::

    Remove view-only link?

    Are you sure you want to remove this view-only link?

    [Cancel][Remove]

Removing the link makes the link inactive and removes it from the table.

Users can share the URL for a view only link with anyone. Anyone with the link can visit the page to see the project's contents—
even if it is private and even if they do not have an OSF account. When a visitor follows a View-only Link there is a blue, non-dismissable
alert at the top of the page::

    This project is being viewed through a private, view-only link. Anyone with the link can view this project. Keep the link safe.

If the link was anonymous, the contributors list reads "Anonymous Contributors" instead of providing the names of the contributors. Activity
logs replace usernames with "A user." "Forks" and "Registrations" tabs are not shared via anonymized view-only links because contributors' names may be listed on these projects. Manually navigating to the Forks or Registrations page using an anonymized view-only link returns "Forbidden" error. 

"Forks" and "Registrations" are shared in non-anonymized view-only links. 

The Commenting panel is not available with a view-only link.

Access Requests
---------------
**Purpose**: Configuring the Request Access feature allows admins to disable or enable this feature on the project.

Only admins can see and configure the Request Access feature in the project Settings. Below the header in this section is a checkbox (which is selected by default)::
  
    Allow users to request access to this project.

If the admin unchecks this box, a red confirmation message will appear below it::
  
    Request access disabled
    
Then the page will refresh, and the project settings will be updated to disable the Request Access feature on the project. If the project is public, the "Request access" button will be removed from the "ellipsis" drop-down menu on the "Overview" page. If the project is private, non-contributors will see a private page that reads::
  
  Forbidden
  User has restricted access to this page. If this should not have occurred and the issue persists, please report it to support@osf.io.

If the admin selects the checkbox, a green confirmation message will appear below it::
  
      Request access enabled
      
Then the page will refresh, and the project settings will be updated to enable the Request Access feature on the project. If the project is public, the "Request access" button will be added to the "ellipsis" drop-down menu on the "Overview" page. If the project is private, non-contributors will see a private page that reads::
  
  You Need permission
  Ask for access, or switch to an account with permission.
  [Request access][Switch account]
  If this should not have occurred, please contact support@osf.io.


Wiki
--------------
**Purpose:** Configuring the wiki allows admins and read+write contributors to enable or disable the wiki and change who can edit a wiki page.

If the user is an admin or read+write contributor, a checkbox appears along with the text::
    
    Enable the wiki in <project>. 

When the user selects the checkbox, the following green confirmation message appears below it::
  
    Wiki Enabled.

The page refreshes, and a "Configure" section appears below the checkbox. This section is always visible when the box is checked.

Below this section is text that reads::
  
    Control who can edit your wiki. To allow all OSF users to edit the wiki, <project> must be public.

The project tree is displayed below these instructions. The project and any component titles link to their "Overview" pages. If the read+write contributor is not a contributor on the component(s), they cannot see the component name in the list. It simply reads "Private Project" without linked text. The parent project is expanded by default, and any child components are collapsed.

To the right of each project/component level is a drop-down menu to select editing privelages. If the project is private, this menu is disabled. If the user scrolls over the menu, their cursor carries the prohibition sign.

If the project/component is private, and the user is an admin, the following line appears below the project/component in the file tree::
  
    This feature is disabled for wikis of private [projects][components].

If the user has read+write access, the following line appears below the project in the file tree, whether the project is public or private::
  
    Only admins may change permissions of this wiki.

The drop-down options are: "Contributors (with write access)" or "All OSF users." By default, "Contributors (with write access)" is
selected. Changing the option to "All OSF users" means that any logged in user can visit the wiki pages of the identified
project/component and edit the contents. Only contributors with read+write or admin permissions can add, remove, and rename wiki
pages, however.

If a user selects "All OSF users," a modal opens::

    Make publicly editable
    Are you sure you want to make the wiki of [Project/Component] publicly editable? This will allow any logged in user to edit the
    content of this wiki. Note: Users without write access will not be able to add, delete, or rename pages.
    [Cancel][Apply]

Clicking "Apply" saves the changes. The drop-down is temporarily removed and replaced with a green confirmation message that reads::

    Settings Updated

After several seconds, the drop-down returns. No confirmation modal is shown.

If a user changes to "Contributors (with write access)" from "All OSF users," the drop-down is temporarily removed and replaced with a green confirmation message that reads::

    Settings Updated

After several seconds, the drop-down returns. No confirmation modal is shown.

Commenting
------------
**Purpose:** Admins and read+write contributors can configure the commenting preferences to determine who can comment on a project.

In the "Commenting" section, the user is shown two options from which they can select—radio buttons allow them to select an option::

    [radio button] Only contributors can post comments
    [radio button] When the project is public, any OSF user can post comments
    [Save]

By default, the second option,"When the project is public, any OSF user can post comments," is selected.

When only contributors can post comments, non-contributors who visit the project page do not see the "Comments" bubble on the far right of the navigation bar on the "Project Overview" page. Anyone with permission to comment sees a blue tab with a chat icon on the far right of the navigation bar on the "Project Overview" page.

Clicking **Save** causes a temporary green confirmation message to appear below the "Save" button::
  
      Success updates settings.

Then the "Settings" page refreshes and the confirmation message disappears.

Leaving the page without clicking **Save** does not produce a warning for the user.

Email Notifications
-------------------
**Purpose:** All users can modify the frequency with which they would like to receive notifications about the project/component.

In the "Email Notifications" section, text below the title reads::

    These notification settings only apply to you. They do NOT affect any other contributor on this project.

The project tree is displayed below the instructions. All project and component titles link to their "Overview" pages. Below each title are two rows titled "Comments added" and "Files updated," respectively. Right justified in these rows are drop-downs that allows users to select their notification preferences.
Components in the tree are collapsed by default, meaning their "Comments added" and "Files updated" rows are not visible until expanded.

The notification options are: "Never," "Instantly," and "Daily." "Instantly" is selected by default. Selecting "Never" means that other contributors' actions will not prompt an email to be sent to the user. Selecting "Instantly" will prompt an email to be sent immediately to the user after another contributor logs an action on the project/component. Selecting "Daily" will send a daily update of all logged actions by other contributors to the user.

Components have an additional option: "Adopt setting from parent project." Selecting this choice will apply the option selected from the parent project to that component.

When the user makes a change, the drop-down is temporarily removed and replaced with the following green confirmation message::

    Settings Updated

After several seconds, the drop-down returns.

.. _redirect link:
Redirect Link
-------------
**Purpose:** Adding an redirect link allows users to redirect project visitors to the provided URL.  

To add a redirect link to a project or component, the user can either scroll to the bottom of the "Settings" page, or click **Redirect Link** from the left sidebar.

The "Redirect Link" section appears as::
  
    Redirect Link
    [check box] Redirect visitors from your project page to an external webpage
    
Checking the box causes the following fields to appear::
  
  URL [Send people who visit your OSF project page to this link instead]
  Label [Optional]
  [Save]

Clicking inside the "URL" field without entering text and then clicking outside of it causes the following error message to appear below the field::
  
    This field is required.
    
Entering invalid text into the field causes the following error message to appear::
  
    Please enter a valid URL.
    
Leaving the "URL" field blank and entering only a label into the "Label" field causes the following red error message to appear below the "Label" field::
  
    Please fill in the required field.
    
The user may enter the URL beneath URL and have the option to add a label. When the user enters information and selects "Save," the text reads::

    Successfully linked to URL

Entering a valid URL into the "URL" field and clicking **Save** causes the following temporary confirmation message to appear below the "Label" field::
  
    Succesfully linked to [URL]


Project Affiliation / Branding
------------------------------
**Purpose:** Users can affiliate projects with institutions that have created OSF for Institutions accounts.

At the top of the "Project Affiliation / Branding" section, there is text that reads::

    Projects can be affiliated with institutions that have created OSF for Institutions accounts. This allows:
        * institutional logos to be displayed on public projects 
        * public projects to be discoverable on specific institutional landing pages 
        * single sign-on to the OSF with institutional credentials
        * FAQ [links to the help guides]
        
Underneath the text reads::

    Available institutions:
    [institutional logo] [institution name] [Add]

Available institutions are determined by the user's sign-on. If logged in under an OSF for Institutions single sign-on feature, that institution will be available to add. Alternatively, if the user's login email is associated with an OSF4I partner, the option to add will be available. 

When the user clicks **Add**, the institution is added to their "Project Overview" page. When an institution is added from the "Settings" page, a red "Remove" button replaces the green "Add" button to the right of an institution.

If an institution is affiliated with the project/component, the above introductory text is not visible. Only the affiliated and available institutions are visible to add or remove.
