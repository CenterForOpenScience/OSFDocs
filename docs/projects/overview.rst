
**Purpose:** The Project Overview provides a comprehensive view of a project's structure and contents.

Project Overviews are the landing page for a project when navigating from :ref:`search results <search>`,
:ref:`public profiles <profiles>`, or the :ref:`"My Dashboard" <my-dashboard>` page. Visitors to a public project can view the overview
as can contributors on a public or private project.

Projects and components contain metatags in order to make the metadata available for export (e.g. Zotero).

Project Title
--------------
**Purpose:** The Project title helps identify and distinguish between projects on a user's dashboard or through the general search.

When viewing a project, the first item in the Project Navigation Bar is the Project Title. If the project title is too long, it will be shortened with an ellipsis. The project title has a blue background and white font. If the user is viewing a project or component that is the child of another project or component, an arrow appears to the left of the project's title. The arrow makes a right angle, turning left then up. Hovering over the arrow shows a tooltip with the parent project or component's title. Clicking on the arrow brings the user to the parent project or component's Overview. 

To rename the title of the project, the user must be on the "Project Overview" or "Component Overview" page. When the user clicks the project or component name in the top left corner of the "Overview" page, the title turns into a textbox wherein the the user can make changes to the title. To the right of the textbox is a green checkmark and an "x" that the user can click to either save their changes or cancel their changes, respectively. The user can also press **enter** on their keyboard to commit the new name.

Project Navigation Bar
----------------------
**Purpose:** The Project Navigation Bar allows users to navigate between the settings and information of a project, as well as navigate to the project overview.

The next link in the Project Navigation Bar is to the Files page. This page shows the :ref:`Files Browser <storage>`.

The next link is to the :ref:`Wiki <wiki>`. This page shows wiki content and allows for wiki editing.

The next link is to the :ref:`Analytics page <analytics>`. This page shows analytics about the project and its visitors.

The next link is to the :ref:`Registrations page <registrations>`. This page lists all registrations of the viewed project.

The next link is to the :ref:`Contributors page <contributors>`. This page lists the project's contributors and allows the user to create :ref:`view-only links <view-only>`. This page is not visible to non-contributors.

The next link is to the :ref:`Add-ons page <add-ons>`. This pages lists the third-party services supported by the OSF that users can connect to from their project.

The next link is to the :ref:`Settings page <project-settings>`. This page allows admins to configure the project. This page is not visible to non-contributors.

If enabled on the project, the final link is the :ref:`commenting icon <commenting>`. Clicking the icon opens the commenting panel.


Privacy settings and quick actions
-----------------------------------
In the top right of the "Overview" page are the privacy buttons, the "Forks" button, and the ellipsis button.

Contributors always see the privacy settings, the "Forks" button, and the ellipsis button. 

If the project is public, non-contributors see the "Public" setting, the "Forks" button, and the ellipsis button.

If a contributor and a non-contributor, alike, click the **Forks** button, a drop-down menu will appear with the following options::
  
      [Fork this Project]
      [Duplicate template]
      [View forks]
      
See the :ref:`forks page <forks>` and the :ref:`templates page <templates>` for details.

If the project is private, an admin will see the following options when clicking the **ellipsis** button::
  
    Bookmark
    Create view-only link

If the project is private, a read or read+write contributor will see the following options when clicking the **ellipsis** button::
  
    Bookmark

If the project is public, all contributors will see the same options as when the project is private, except they will also see the **Share** button appended to the list.

Clicking the **Create view-only link** button will take admins to the "View-only links" section of the :ref:`project settings page <project-settings>` where they can generate a view-only link for the project.

If the project is public, all non-contributors will see the following options when clicking the **ellipsis** button::
  
    Bookmark
    Share
    Request access

See the :ref:`request access page <request_access>` for details.


.. _overview-metadata:

Metadata
-------
**Purpose:** Every project has associated information about that project—its title, contributors, etc. This is metadata about that project.
The metadata is displayed at the top of the Project Overview to orient users to the project's basic information.

At the top of the Project Overview is the project's title. Below the title is the list of contributors. Below this is a row listing
the "Date Created" and "Last Updated" date. Below these two dates is the "Category" field. Below this is the License. Below this is the project description.

The project title can be updated by a contributor with administrative or read+write :ref:`permissions <contributors>`. These
contributors can click on the title. This opens a text entry field where the user can revise the title. To submit changes, the user
must click the green check button to the right of the field. To cancel the change, the user can click on the grey 'x' button
to the right of the check button. To clear the contents of the field, the user can click on a small 'x' within the text field.
If the user makes changes but clicks out of the text box without saving the edits, the changes are lost.

The :ref:`contributors <contributors>` list is preceded by a title that reads "Contributors:" This title is a link to the "Contributors" page. Following
this title is a list of each bibliographic contributor added to that particular component. By default, contributors are listed
in the order they were added in. Each contributor is listed by their OSF :ref:`username <account-settings>`. Each name is a link
to the user's :ref:`public profile <profiles>`.

"Date Created" and "Last Updated" are listed on the same line, separated by a bar (|). Dates are formatted to appear as
YYYY-MM-DD HH:MM AM/PM. Dates appear in local time, but when the user hovers over them, a tooltip appears to display the date in
UTC. The "Last Updated" field shows the time of the last logged action on that particular project—if other, more recent logs were created
within :ref:`components <components>` that are children of the viewed project, those do not affect the "Last Updated" field.
When a contributor makes a change to a project, the page does not refresh, meaning that the "Last Updated" field does not automatically
update; the page must be reloaded to show an accurate time.

The "Create DOI" link appears below the "Date created" field for public projects. This link is not visible for private projects. Clicking this link allows a project admin to generate a DOI for their project. Clicking this link opens the following modal::
  
    Create DOI
    Are you sure you want to create a DOI for this project? A DOI is persistent and will always resolve to this page.
    [Cancel][Create]

Clicking **Cancel** cancels the action and closes the modal. Clicking **Create** generates the DOI. All DOIs generated on OSF have the same format: DOI 10.17605/OSF.IO/GUID.

The "Category" field displays the category of that particular project or component, as specified on its creation or by changes from the
:ref:`project settings page <project-settings>`. Categories can be: project, hypothesis, methods and measures, procedure, instrumentation,
data, analysis, communication, other, or‚ if it is a component, it can be uncategorized. To the right of the category listed is an icon,
intended to visually indicate the category.

The "Description" field can be left empty or can contain a description provided by any read+write or admin contributor on the project.
If left blank, the field does not appear for non-contributors viewing a public project's overview. If left blank, and the viewer
is a read-only contributor, the field does not appear. For other contributors, an empty field reads "No Description." To add content,
the contributor clicks on the "No Description" placeholder text or hovers over existing text and types into the text field.
The field can be resized.  To submit changes, the user
must click the green check button to the right of the field. To cancel the change, the user can click on the grey 'x' button
to the right of the check button. To clear the contents of the field, the user can click on a small 'x' within the text field.
If the user makes changes but clicks out of the text box without saving the edits, the changes are lost. There is no limit to
the length of a description. If the user leaves a blank link between paragraphs, the space will be shown upon submitting the changes.
Any HTML is scrubbed from the contents, disappearing on save. Markdown does not format the text. After the changes are saved, the page refreshes.

The "License" field can be left empty or can contain a license. 

An ADMIN contributor selects a license by clicking on the field, which opens a widget containing "Choose a field" and a dropdown list of licenses. The available licenses are::

    No License
    Content:
        CC0 1.0 Universal
        CC-By Attribution 4.0 International
    Code - Permissive
        MIT License
        Apache License 2.0
        BSD 2-Clause "Simplified License"
        BSD 3-Clause "New"/"Revised" License
    Code - Copyleft:
        GNU General Public License (GPL) 3.0
        GNU General Public License (GPL) 2.0
    Code - Other:
        Artistic License 2.0
        Eclipse Publice License 1.0
        GNU Lesser General Public License (LGPL) 3.0
        GNU Lesser General Public License (LGPL) 2.1
        Mozilla Public License 2.0
    License - Other

Choosing a license causes the details of the license (full text) to appear below the License selector. Depending on the particular License selected, the ADMIN may be presented with text fields to enter a year and/or Copyright Owners' names. To choose a license, the user clicks the green [Save] button. To exit without selecting making a change to the license, the user clicks the gray "X" on the top right of the license widget.

For a READ+WRITE or READ contributor, or non-contributor (viewer of a public project), if there is no license applied to the project, the License field does not appear in the metadata field. For these users, if a license is applied, the title of the license appears in the License field along with an information icon. Clicking on the information icon displays the full text of the license. Clicking a second time collapses the text. 

If left empty, the License field only displays for Admin contributors. 

Below the license, the page is populated by widgets—panels that contain information and allow actions for specific parts of a project.

Wiki Widget
-----------
**Purpose:** The Wiki widget provides a preview of wiki contents.

The first widget is the Wiki widget. In the upper right corner of the widget is a button that links the user to the Wiki page. When the :ref:`Home wiki page <wiki>` has not been edited to include content, contributors with read+write or admin priviliges see "Add important information, links, or images here to describe your project" displayed inside the panel. If the user has created additional wiki pages with content, but has no content on the Home wiki page, the panel still displays "Add important information, links, or images here to describe your project." If the project is being viewed by a non-contributor and the "Home" wiki page has no content, then the widget is not displayed at all.

If there are 393-400 characters on the "Home" wiki page, the "Wiki" widget will preview the full content. If there are more than 400 characters on the "Home" wiki page, the content will be truncated by an ellipsis, and a "Read More" link will appear at the bottom widget. This link directs the user to the "Home" wiki page.

Files Widget
------------
**Purpose:** The Files widget provides a comprehensive view of the project's files and allows basic actions like uploading and downloading.

Below the Wiki widget is the Files widget. In the upper right corner of the widget is a button that links the user to the Files page.
Below the panel header is a grey toolbar. Below the toolbar is the File Browser.

The Files widget is a smaller instantiation of the :ref:`Files Browser <storage>`. It is displayed, on the Project Overview, below
the Wiki widget.

The user can view their components and corresponding files in a tree structure in the Files widget. The user can move files from project to components and vice versa (within the same overall project) by dragging and dropping into the designated storage. If the user moves a file to another location within the same project that already has a file with that same name, the following modal appears::
  
  Replace "[filename]"?
  An item named  "Architecture in Chicago.docx" already exists in this location.
  "Keep Both" will retain both files (and their version histories) in this location.
  "Replace" will overwrite the existing file in this location. You will lose previous versions of the overwritten file. You will keep previous versions of the moved file.
  "Cancel" will cancel the move.
  [Cancel][Keep Both][Replace]
  
Clicking **Cancel** cancels the file move. Clicking **Keep Both** keeps the original file and adds the newly moved file to the location. Clicking **Replace** replaces the original file in the second location with the newly moved file. The file always remains in the first location.

Citation Widget
--------------
**Purpose:** The "Citation" widget provides a pre-formatted citation referencing the viewed OSF project or component.

The Citation widget is locate to the right of the Wiki widget. Every project and component on the OSF has a unique and permanent URL, allowing
each one to be cited.

The Citation widget is collapsed by default, showing only the panel header, "Citation," on the left and the project's URL on the right.
Clicking the expand button to the right of the project's URL expands the widget. Three citations of the project are provided within the
panel's body. The first is a citation in APA format, the second in MLA format, the third in Chicago format. A dropdown below the three options
allows the user to select another citation format.

Clicking on the dropdown opens a text field with directions below the entry field reading::

    Please enter 1 or more character

When the user enters a query the results return relevant citation formats. Selecting one creates a well below the dropdown, providing the citation
for the project or component in the requested format. The user can clear their selection by clicking an 'x' in the dropdown. If
the query returns no results the dropdown returns, below the text field::

    No matches found

If the user collapses the citation widget with an alternative format selected from the dropdown, on re-expansion the format is still selected
and the citation is still provided.

Any user visiting a public project can view the Citation widget and select an additional citation style from the dropdown.

.. _component-widget:

Components Widget
-----------------
**Purpose:** The "Components" widget allows users to view and create new components as well as link projects.

The "Components" widget is located below the "Citation" widget. This widget shows all child components and any linked projects.

When a project has no links or components within it, the "Components" widget is not displayed for either read-only contributors and non-contributors. 

When a project has no links or components within it, the "Components" widget *is* dislpayed for contributors with read+write or admin permissions. These contributors see the two buttons and the following message::
  
  Add components to organize your [project/component]
  
Components within this widget show basic metadata about the component: 
  
In the widget's heading, two buttons are visible: "Add Component" and "Link Projects."

Add a Component
^^^^^^^^^^^^^^^
Clicking the "Add Component" button opens a modal::

    Create new component
    [text field: "Title"]
    ["Affiliation"]
    [Checkbox: Add contributors from [Parent Project]]
    [Checkbox: Add tags from [Parent Project]]
    ["License"]
    [ drop-down menu: "More"]
      > [text field: "Description"]
        [drop-down menu: "Category (for descriptive purposes)"]
    [Cancel][Create]

The first field in the modal is an empty text field with placeholder text that reads "Enter component Title." The user can enter a title of any length, however,
on save, only the first 200 characters will be saved to the title.

If the user is affiliated with an institution, the institutional logo will appear in the "Affilation" section. Affiliation are selected automatically and added to a component upon creation. If the user does not want to affiliate their component, they can click the logo to deselect it from the component.

If the user wants the component to inherit the parent project's contributors, they can check the box next to "Add contributors from [parent project]." Contributors will not be added from the parent project if this box is left unchecked. If the user selected to add contributors from the parent project, they are all added with the same permissions as the parent. 

If the user wants the component to inherit the parent project's tags, they can check the box next to "Add tags from [parent project]."

The "License" section simply has a line of text that reads: "This component will inherit the same license as [parent project]. Learn more (links to:http://help.osf.io/s/support/m/projects/l/524050-license-your-project)].

Clicking the **More** drop-down menu causes a sub-section to unfold to show the "Description" and "Category" fields. The user can enter a description into the field or leave it blank. The user can also select a category from the drop-down menu or keep the default option of "Uncategorized." The other categories are: "Analysis," "Communication," "Data," "Hypothesis," "Instrumentation," "Methods and Measures," "Procedure," "Project," "Software," and "Other."

After clicking **Create**, a confirmation modal appears::

  New component created successfully!
  [Keep working here][Go to new component]

Clicking **Keep working here** keeps the user on the "Project Overview" page. Clicking **Go to new component** takes the user to the new "Component Overview" page.

Adding Links
^^^^^^^^^
**Purpose**: This feature enables users to link between personal or public projects, components, and registrations.

Clicking the **Link Projects** button opens a modal::

    Link other OSF projects
    <text field> "Search projects"
    [Search all projects][Search my projects]
    
The "Search my projects" button is selected by default. 

Below the search buttons are two tabs, one labeled "Projects" and one labeled "Registrations." "Projects" is selected by default. Below "Projects" are the results::
  
    Results: My Projects

The results are paginated, displaying 4 at a time. Selecting the "Registrations" tab shows the user's registrations::
  
    Results: My Registrations

Like projects, the results are paginated, displaying 4 at a time.

The user can type a project or registration title into the "Search projects" field, and click the either the **Search all projects** button or the **Search my projects** button to find the project/registration.
If the user clicks the **Search all Projects** button, all public OSF projects, components, and registrations whose title matches the query will be returned. If the user clicks the **Search my projects** button,
all of the user's OSF projects, components, and registrations whose title matches their query will be returned. 

Project results are displayed in a table format, as follows::
  
  <project title> | Created: YYYY-MM-DD HH:MM AM/PM | <lastname of first listed contributor>
                    Modified: YYYY-MM-DD HH:MM AM/PM

In the author column, if more than one author is listed on project, the last names appear as "<lastname et al.>".

Registration results are also displayed in a table format, as follows::
  
    <registration title> | Registered: YYYY-MM-DD HH:MM AM/PM | <lastname of first listed contributor>
    
In the author column, if more than one author is listed on project, the last names appear as "<lastname et al.>".

To the left of each project and registration title is a green square button marked with a '+' sign. 

Clicking **+** selects the project or registration from the results. The "+" sign is replaced by a gray button with a "-" sign.
Clicking **-** loads the button until it returns back to the green "+" button. 

The user can select up to any number of projects or registrations from the results. The user can switch between the "Projects" and
"Registrations" tabs, selecting from each, and selected results will be saved and applied upon adding. After the user has selected
the project(s)/registration(s), they can click the **Done** button in the bottom right of the modal to add the linked projects/registrations to their project. Upon
clicking **Done**, the page refreshes and the linked project(s)/registration(s) will appear in the list in the "Components" widget.

Linked projects/registrations are formatted as described in the :ref:`Component widget format section <component-format>` below. Links are marked by a lock symbol to the left of the project/registration title. To the right of the title are an "x" icon and "fork" icon.
Hovering over the **x** opens the following tooltip::
  
  Remove link

Clicking the **x** opens the following confirmation modal::
  
    Remove this link?
    Are you sure you want to remove this link? This will not remove the project this link refers to.
    [Cancel][Remove]
    
Clicking the **Cancel** button cancels the action and closes the modal. Clicking the **Remove** button closes the modal and removes the linked project/registration from the "Components" widget.

Hovering over the **fork** icon opens the following tooltip::
  
    Create a fork of <project title>
    
Clicking the **fork** icon opens the following confirmation modal::
  
    Fork this project?
    Are you sure you want to fork this project?
    [Cancel][Fork]

Clicking the **Cancel** button cancels the action and closes the modal. Clicking the **Fork** button closes the modal, but the page is grayed out and a message appears::
  
    Please wait

After the fork is created, the following confirmation modal appears::
  
    Fork created successfully@
    [Keep working here][Go to new fork]

Clicking the **Keep working here** button closes the modal, and the user stays on their project "Overview" page. Clicking the **Go to new fork** button takes the user to the
forked project's "Overview" page.

Clicking the **fork** icon on a linked registration creates a regular forked project out of the registration. To make a registration out of the fork, the user would need to register themselves.

Viewing links
^^^^^^^^^^^^^
See the :ref:`Analytics page <analytics_links>` for information.

.. _component-format:
Component widget format
^^^^^^^^^^^^^^^^^^^^^^^
Components and links are listed in the Components widget with their title, contributors, description, category, and privacy symbols. Components are listed
in the order in which they were added. Components can be dragged and dropped to re-order. After re-ordering components, the user can refresh the page and the changes will be visible.

If one of the components is private, to the left of the title and category symbol is a lock. If the component
is public, there is no symbol. Titles link to the project/component/link's overview page. Below the titles are the names of the first three contributors;
if there are more contributors, they are indicated by the addition of "& <#> more."" Clicking on a contributor's name brings the user to the contributor's
public profile. Clicking on "& <#> more" brings the user to the Overview page for the project/component/link.

The component shows a snippet of the description of up to 3 lines. If the description is longer, the snippet will be tailored off by an ellipsis. If the component does not have a description, no description is displayed for the component in the "Components" section of the parent project.

To the right of the element's title is an ellipsis that, when clicked, gives contributors options to manage the component directly from the parent's "Overview" page.

The ellipsis is visible only to contributors, and is only on components. 

When an admin clicks the ellipsis, a drop-down menu appears with the following options::
  
    Manage Contributors
    Settings
    Delete
    
Read and read+write contributors only see::
  
    Manage Contributors
    Settings
    
Clicking **Manage Contributors** takes the user to the component's "Contributors" page - the view depeonds to the user's level of permissions.

Clicking **Settings** takes the user to the component's "Settings" page - the view depeonds to the user's level of permissions.

Clicking **Delete** enables the user to delete the component and its children. If the component has children, a modal will appear from which the user must select all child components before deleting the parent component::
  
    Delete component
    This component contains subcomponents. To delete this component, you must also delete all subcomponents. This action is irreversible.
    Select: All components                  * project or component contains a preprint
    <component hierarchy>      
    [Cancel][Continue]
    
Clicking the **All components** link selects all child components to be deleted. If a child component is left unselected, the "Continue" button at the bottom of the modal will be disabled. If the user deleting the component does not have admin permissions on all child components, they will be unable to delete these child components and, therefore, the parent component. The checkboxes next to these child components will be disabled, along with the "Continue" button at the bottom of the modal. The user can hover over the checkboxes to see a tooltip explaining why these components cannot be deleted::
  
    You must have admin permissions on this component to be able to delete it.
    
If a child component contains a preprint, an asterisk will appear next to its title in the modal. Deleting a child component with a preprint will also delete the preprint.

Once the user selects all child components from the modal, they will be able to click the **Continue** button. Upon clicking **Continue**, the user will be directed to a final confirmation modal::
  
    Delete component and subcomponents
    The following component and subcomponents will be deleted
    <component hierachy>
    Please note that deleting your component will erase all your component data and this process is IRREVERSIBLE. Deleted component and subcomponents will no longer be available to other contributors on the component.
    Type the following to continue: <confirmation word>
    [Back][Cancel][Delete]

The "Delete" button will be disabled until the user enters the confirmation word into the field. Upon entering the confirmation word, the user can click **Delete**.

If the component does not contain child components, the user will go through only one modal to confirm the deletion of the component::
  
    Are you sure you want to delete this component?
    It will no longer be available to other contributors on the project.
    Type the following to continue: <confirmation word>
    [Cancel][Delete]

After deleting the component, the user will see a dismissable confirmation banner on the top-level project "Overview" page::
  
    Component has been successfully deleted.

If the component contained children, the user will see a confirmation modal::
    
    Your component has been successfully deleted.
    [OK]

Clicking the **OK** button dismisses the modal, and returns the user to the parent project "Overview" page.


.. _tags:

Tags Widget
----------------
**Purpose:** The Tags widget allows users to provide keywords relevant to their project to enhance discoverability of their work.

The "Tags" widget is located below the components widget. When no tags are added, contributors with read+write or admin permissions
see text that reads: "add a tag to enhance discoverability." If the user is not a contributor on the project, or only has read permissions, and no
tags have been added, the "Tags" widget is not visible.

Contributors with read+write or admin permissions can add a tag by clicking inside the "Tags" widget and typing in a word. 
Pressing the return key will add the tag. Inserting a comma after a tag will also add the tag. Entering the same tag more
than once is not supported. If the user attempts to enter the same tag twice, the tag will not be added. Read contributors
and non-contributors see the tags but cannot edit or remove them. Admins and read+write contributors will see a
black 'x' to the right of the tag that they can click to remove the tag.

After the user has added tag(s), the text "Add a tag" appears to the right of the last tag. If the user deletes all tags, the text in the widget reads "add a tag." 
Refreshing the page returns the original text "add a tag to enhance discoverability" to the widget. 

Clicking on a tag takes the user to the OSF "Search" page where other projects, registrations, or preprints with the same tag are returned. If no results are returned,
the message "No results found" appears at the top of the page.

The query in the search bar is as follows::
  
    (tags:"[keyword]")

.. _activity:

Recent Activity Widget
--------------------
**Purpose:** The Recent Activity widget shows users the logged actions for the viewed project or component, its children, and its registrations.

The Recent Activity widget appears below the Tags widget. Below the panel title, "Recent Activity," is muted text that reads::

    All times displayed at ____ UTC offset.

Times are displayed in local time, and the correct offset is indicated in the above text.

Below this is a list of all logged actions on the project/component, its children, and registrations displayed in chronological order with the most recent action listed at the top. Actions are listed in two columns—the left shows the date and time (YYYY-MM-DD HH:MM AM/PM).
Hovering over a time shows a tooltip with the date and time in UTC.

In the right column is a description of the log, first listing the user who committed the action, then the action and the
affected component or project. For example::

    [Username] tagged [project] as [tag]
    [Username] added [Username] as contributor(s) to [project name]

When an admin adds more than three contributors to a project at a time, only the first three contributors are shown in the log, and the rest are represented by the remaining number::
  
    [Username] added [username], [username], [username] and [#] others as contributor(s) to [project name]

Users, files, projects, components, preprints, registrations, and wikis are linked to their corresponding pages.

Only the ten most recent logs are shown at once. The full list of logs are paginiated. Pagination behavior is described in detail :ref:`here <pagination>`.

Viewing a redirect Link
***********************
**Purpose:** Users who configure a redirect link give visitors the option to follow an external link from the "Overview" page. Visitors are prompted to redirect to this link upon entering the OSF project. 

If configured (see :ref:`Configuring a redirect link <redirect link>`) visitors to the project will immediately see a modal that reads::

    This project contains a forward to 
    [URL]
    [Cancel] [Redirect]

Clicking **Cancel** will allow the user to stay on the OSF project. Clicking the link itself or **Redirect** will take the user to the external link. 