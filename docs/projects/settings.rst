**Purpose:** Project settings allow users to configure the project settings and their notifications for that project.

The project settings page shows different options for contributors with different permissions.

If the user is an admin or a read+write contributor on the project, there are five sections on the "Settings" page that they can configure: "Project/Component," "Select Add-ons," "Configure Add-ons" (only shows if add-ons are connected),"Wiki," "Commenting," and "Email Notifications."
The "Settings" page has a sidebar that the user can use to navigate through the sections of the page.
  
Additional sections are shown if the project is public or if add-ons are configured.

If the user is a read-only contributor on a project/component, the sidebar is not visible and only the "Project Affiliation/Branding" and "Notifications" sections are visible. The read-only contributor can configure their notification preferences in the "Email Notifications" section but will only have view-access to the "Project/Affiliation/Branding" section. This section reads::
  
    Project Affiliation/Branding
    Contributors with read-only permissions to this project cannot add or remove institutional affiliations.
    Projects can be affiliated with institutions that have created OSF for institutions accounts. This allows:
    * institutional logos to be displayed on public projects
    * public projects to be discoverable on specific institutional landing pages
    * single sign-on to the OSF with institutional credentials
    * FAQ (links to help guides' landing page)
    
    Available institutions:
    [instutional logo][institution]

If the user is an admin on a parent project, but is not a contributor on a component, only the "Project Affiliation/Branding" and "Notifications" sections will be visible on the component's "Settings" page. The admin is not, however, a contributor to the component. The component's "Contributors" tab is not visible to the admin. The admin can configure their notification preferences in the "Email Notifications" section of the component's "Settings" page. However, the admin has view-only access to the "Project Affiliation/Branding" section. This section reads as follows::
  
    Project Affiliation/Branding
    Contributors with ready-only permissions to this project cannot add or remove institutional affiliations.
    
    Affiliated Institutions:
    [instutional logo][institution]

If the contributor on the parent project has read or read+write permissions, the component's "Settings" tab will not be visible.

Project/Component
-----------
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

If a user clicks the "Delete project/component" button when the project or component has children, a red, dismissable alert appears in the top right of the "Settings" page::

    Error
    Any child components must be deleted prior to deleting this project.

The user must delete the child components prior to deleting a parent project or component.


Select Add-ons
------------
See :ref:`the information about add-ons here <add-ons>`.

Add-ons
------------
When an add-on has been activated, an additional section is added to the page—"Configure Add-ons." See :ref:`the information about add-ons here <add-ons>`.

Wiki
------------
**Purpose:** Configuring the wiki allows admins and read+write contributors to enable or disable the wiki and change who can edit a wiki page.

If the user is an admin or read+write contributor, a checkbox appears along with the text::
    
    Enable the wiki in [project/component name]. 

If the project is private, and/or the user is a read+write contributor, text below reads::
  
   To allow all OSF users to edit the wiki, [project/component title] must be public and the wiki enabled.

If the project is public and the user is an admin, the word "Configure" appears below the checkbox in large text, followed by::

    Control who can edit the wiki of [project/component name]:

The project tree is displayed below these instructions. All project and component titles link to their "Overview" pages.
Below each public project/component in the tree is a row titled "Who can edit." Right justified in this row is a drop-down that allows
admins to indicate who can edit that project/component's wiki pages.

Components are collapsed by default, meaning their "Who can edit" rows are not visible until expanded.

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

Email Notifications
------------
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

