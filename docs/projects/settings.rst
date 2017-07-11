**Purpose:** Project settings allow users to configure the project settings and their notifications for that project.

The project settings page shows different options for contributors with different permissions.

If the user is an admin on the project, there are five sections in the Settings page that they can configure: "Project/Component," "Select Add-ons," "Wiki," "Commenting," "Email Notifications." Additional sections
are shown if the project is public or if add-ons are configured.

If the user is a read+write contributor, only the "Project," "Select Add-ons," "Add-ons," "Wiki," and
"Email Notifications" panels are visible.

If the user is a read only contributor, only the "Notifications" panel is visible.

If the user is a contributor on a parent project, but not a sub-project/component, only the "Notifications" panel
is visible on the settings page.


Project/Component
------------
**Purpose:** Configuring the project or component allows the user to update the category, edit the title or description, or delete the project/component.

The first item in the Project panel is "Category." A dropdown allows admins to select a category to assign to the project.
Projects cannot change their category—the dropdown is visible but inactive and set to "Project." Muted text below a project's dropdown
reads::

    A top-level project's category cannot be changed.

Component categories can be changed. Prior to editing the category, two deactivated buttons are visible below the dropdown::

    [Cancel][Save Changes]

After the user makes a new selection, the buttons become active. Clicking "Save Changes" deactivates the buttons and green inline text
is added below the buttons::

Category updated successfully

Leaving the page without cancelling or clicking "Save Changes" produces a warning for the user::

    "Confirm Navigation. There are unsaved changes in your project settings. Are you sure you want to leave this page? [Stay on this page][Leave this page]""

The available categories are: "Analysis," "Communication," "Data," "Hypothesis," "Instrumentation," "Methods and Measures," "Procedure," "Project," "Software," "Other," "Uncategorized"

.. _todo: log above as enhancement

For admins and read+write contributors on a project or component, the next section allows users to edit the title and description. There is one field for "Title" and one field for "Description."

Below this are two buttons::

    [Cancel][Save Changes]

These buttons are active regardless of whether or not a user has made a change in the text fields. Clicking "Save Changes" produces green inline text below the buttons::

Category updated successfully

Leaving the page without cancelling or clicking "Save Changes" produces a warning for the user::

    "Confirm Navigation. There are unsaved changes in your project settings. Are you sure you want to leave this page? [Stay on this page][Leave this page]""


.. TODO:: add in information about read-only permissions (likely not visible at all)

For admins on a project or component, another section is visible in the Configure Project panel. Below the Title and Description
fields is text that explains::

    A project cannot be deleted if it has any components within it. To delete a parent project, you must first delete
    all child components by visiting their settings pages.

Below this text is a red "Delete project/component" button. Clicking this button opens a modal::

    Are you sure you want to delete this project/component?
    It will no longer be available to other contributors on the project.
    Type the following to continue: [text]
    [text field]
    [Cancel][Delete]

The user must click "Delete" to proceed—pressing the return key does not submit the change.

Users are instructed in that modal to type a confirmation word—this word changes each time the user visits this modal.
This field is case sensitive.

.. _todo: log that users should be alerted that it's case sensitive.

If users type the wrong word into the text field, a red, dismissable growlbox alert appears in the upper right corner of the page::

    Verification failed
    Strings did not match

If a user attempts to delete a project or component with children, a red, dismissable growlbox alert appears in te upper right corner of the page::

    Error
    Could not delete component: Any child components must be deleted prior to deleting this project.

The user must delete components and sub-projects prior to deleting a parent project.

When a user successfully deletes a component, they are brought to the parent project's overview. A green dismissable alert
is shown at the top of the page::

    Component deleted.

When a user successfully deletes a project, they are brought to their :ref:`user dashboard <dashboard>`. A green dismissable alert
is shown at the top of the page::

    Project deleted

Select Add-ons
------------
See :ref:`the information about add-ons here <add-ons>`.

Add-ons
------------
When an add-on has been activated, an additional section is added to the page—"Configure Add-ons." See
:ref:`the information about add-ons here <add-ons>`.

Wiki
------------
**Purpose:** Configuring the wiki allows Admins and Read+Write contributors to enable or disble the wiki, and change who can edit a wiki page.

If the user is an Admin or Read+Write contributor, a checkbox appears along with the text::
    
    Enable the wiki in [project/component name]. 

If the project is private, and/or the user is a Read+Write or Read contributor, text below reads, "To allow all OSF users to edit the wiki, [project/component title] must be public and the wiki enabled."

If the project is public and the user is an Admin contributor, the word "Configure" appears next in large text, followed by::

    Control who can edit the wiki of [project/component name]:

The project tree is displayed below the instructions. All project and component titles link to their overview pages.
Below each public project/component in the tree is a row titled "Who can edit." Right justified in this row is a dropdown that allows
admins to indicate who can edit that project/component's wiki pages.

Sub-projects/components are collapsed by default, meaning their "Who can edit" rows are not visible until expanded.

Dropdown options are: "Contributors (with write access)" or "All OSF users." By default, "Contributors (with write access)" is
selected. Changing the option to "All OSF users" means that any logged in user can visit the wiki pages of the identified
project/component and edit the contents. Only contributors with write or admin privileges can add, remove, and rename wiki
pages, however.

If a user selects "All OSF users," a modal opens::

    Make publicly editable
    Are you sure you want to make the wiki of [Project/Component] publicly editable? This will allow any logged in user to edit the
    content of this wiki. Note: Users without write access will not be able to add, delete, or rename pages.
    [Cancel][Apply]

Clicking "Apply" saves the changes and refreshes the page.

If a user changes to "Contributors (with write access)" from "All OSF users," the dropdown is temporarily removed and replaced with green text that reads::

    Settings Updated

After several seconds, the dropdown returns. No confirmation modal is shown.

Commenting
------------
**Purpose:** Admins can configure the commenting preferences to determine who can comment on a project.


In the Commenting panel, the user is shown two options to choose between—radio buttons allow them to select an option::

    [radio button] Only contributors can post comments
    [radio button] When the project is public, any OSF user can post comments
    [Save]


By default, "When the project is public, any OSF user can post comments.

When only contributors can post comments, non-contributors who visit the project page do not see the comment tab in the upper
right hand corner of the Project Overview. Anyone with permission to comment sees a blue tab with a chat icon in the upper right
corner of their Project Overview—clicking opens the :ref:`Comments panel <comments>`.

Leaving the page without clicking "Save" does not produce a warning for the user.

Project Affiliation / Branding
------------
**Purpose:** Users can affiliate projects with institutions that have created OSF for Institutions accounts.

In the Project Affiliation / Branding panel, text below read::

    Projects can be affiliated with institutions that have created OSF for Institutions accounts. This allows:
    institutional logos to be displayed on public projects 
    public projects to be discoverable on specific institutional landing pages 
    single sign-on to the OSF with institutional credentials
    FAQ

Underneath the text reads:: 

    Available institutions:
    [institution name] [Add]

Available institutions are determined by the user's sign-on. If logged in under an OSF for Institutions single sign-on feature, that institution will be available to add. Alternatively, if the user's login email is associated with an OSF4I partner, the option to add will be available. 

Email Notifications
------------
**Purpose:** All users can modify the frequency with which they would like to receive notifications about the project.


In the Notifications panel, text below the title reads::

    These notification settings only apply to you. They do NOT affect any other contributor on this project.

The project tree is displayed below the instructions. All project and component titles link to their overview pages. Below
each title is a row titled "Comments Added." Right justified in this row is a dropdown that allows users to select their
email choice. "None" is selected by default.

Sub-projects/components are collapsed by default, meaning their "Comments Added" rows are not visible until expanded.

Dropdown options are: "None," "Emails," and "Email Digest." Selecting "None" means that other contributors' actions will not
prompt an email to be sent to the user. Selecting "Emails" will prompt an immediate email to the user after another contributor
logs an action on the project/component. Selecting "Email Digest" will send a daily update of all logged actions by
other contributors to the user.

Components have an additional option—"Adopt setting from parent project." Selecting this choice will apply the option applied to the parent project
to that component.

When the user makes a change, the dropdown is temporarily removed and replaced with green text that reads::

    Settings Updated

After several seconds, the dropdown returns.

