
**Purpose:** The Project Overview provides a comprehensive view of a project's structure and contents.

Project Overviews are the landing page for a project when navigating from :ref:`search results <search>`,
:ref:`public profiles <profiles>`, or the :ref:`"My Dashboard" <my-dashboard>` page. Visitors to a public project can view the overview
as can contributors on a public or private project.

Project Navigation Bar
--------------
**Purpose:** The Project Navigation Bar allows users to navigate between the settings and information of a project, as well
as navigate to the project overview.

When viewing a project, the first item in the Project Navigation Bar is the Project Title. If the project title is too long, it will be shortened with
an ellipsis. The project title has a blue background and white font. If the user is viewing a project or component that is the child of
another project or component, an arrow appears to the left of the project's title. The arrow makes a right angle, turning left then up. Hovering over
the arrow shows a tooltip with the parent project or component's title. Clicking on the arrow brings the user to the parent project or component's Overview.

The next link in the Project Navigation Bar is to the Files page. This page shows the :ref:`Files Browser <storage>`.

The next link is to the :ref:`Wiki <wiki>`. This page shows wiki content and allows for wiki editing.

The next link is to the :ref:`Analytics page <analytics>`. This page shows analytics about the project and its visitors.

The next link is to the :ref:`Registrations page <registrations>`. This page lists all registrations of the viewed project.

The next link is to the :ref:`Forks page <forks>`. This page lists all the forks of the viewed project.

The next link is to the :ref:`Contributors page <contributors>`. This page lists the project's contributors and allows the user to create
:ref:`view-only links <view-only>`. This page is not visible to non-contributors.

The final link is to the :ref:`Settings page <project-settings>`. This page allows admins to configure the project. This page
is not visible to non-contributors.

Renaming a Project
------------------
**Purpose:** Allows the user to change the name of their project or component after they have created it.

The user must be on the "Project Overview" or "Component Overview" page to rename their project or component. When the user clicks the project or component name in the top left corner of the "Overview" page, the title turns into a textbox where the the user can make changes to the title. To the right of the textbox is a green checkmark and an "x" that the user can click to either save their changes or cancel their changes, respectively. The user can also press **enter** on their keyboard to commit the new name.

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

The first widget is the Wiki widget.  In the upper right corner of the widget is a button that links the user to the Wiki page.
When the :ref:`Home wiki page <wiki>` has hot been edited to include content, contributors
with read+write or admin priviliges see "No wiki content" displayed inside the panel. If the user has created additional
wiki pages with content, but has no content on the Home wiki page, the panel still displays "No wiki content." If the project
is being viewed by a non-contributor and the Home wiki has no content, then the widget is not displayed at all.

If there is content in the home wiki page, users and non-contributors will see a "Read more" link at the bottom of the wiki widget. This link directs the user to the wiki page.

.. todo:: Ask Erin if it makes sense to hide the widget if there are other pages—especially hide from read only contributors.

Below the Wiki widget is the Files widget.  In the upper right corner of the widget is a button that links the user to the Files page.
Below the panel header is a grey toolbar. Below the toolbar is the File Browser.


Files Widget
------------
**Purpose:** The Files widget provides a comprehensive view of the project's files and allows basic actions like uploading and downloading.

The Files widget is a smaller instantiation of the :ref:`Files Browser <storage>`. It is displayed, on the Project Overview, below
the Wiki widget.


Citation Widget
--------------
**Purpose:** The Citation widget provides a pre-formatted citation referencing the viewed OSF project or component.

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
---------------
**Purpose:** The Components widget allows users to view and create new components.

The Components widget is located below the Citation widget. In the panel's heading, two buttons are visible: "Add Component" and "Add Links."

When a project has no links or components within it, non-contributors do not see the Components widget. In that same scenario, users with
read only permissions see the Components widget with no buttons. The body of the panel reads::

    No components to display

Contributors with read+write or admin permissions see the two buttons and the panel provides the same message.

If the user is visiting a component with no links or components nested within it, the message reads::

    No components have been added to this component.

Clicking the "Add Component" button opens a modal::

    Add Component
    [text field: "Component Title]
    [dropdown: "--Category--"]
    [Checkbox: Add contributors from [Parent Project]]
    [Cancel][Add]

The first field in the modal is an empty text field with placeholder text that reads "Component Title." The user can enter a title of any length, however,
on save, only the first 200 characters will be saved to the title.

The user can add the component without selecting a category. To choose one, however, the user clicks on the dropdown menu labeled "--Category--"
and selects any of the available options. If the user selects a category but does not enter a title, a red text alert appears below the
"Component Title" field::

    This field is required.

After clicking the "Add" button, the button becomes deactivated and reads "Adding" until the page refreshes. The user remains on the Project Overview page, and there is a blue dismissable alert at the top of the page::

    Your component was created successfully. You can keep working on the project page below, or go to the new component.

If the user selected to add contributors from the parent project, they are all added at the same permissions levels as the parent. 

Clicking the "Add Links" button opens a modal::

    Add Links
    [text field: "Search projects"]
    [Search all projects][Search my projects]

Below the search buttons are two columns, one labeled "Results" and one labeled "Adding."

The user can enter their query in the "Search projects" text field. If they select the "Search Projects" button, all public OSF projects,
components, and registrations whose title matches their query will be returned. Five results will be displayed, with additional pages listed below (see
the description of pagination on the :ref:`Watchlist <pagination>` for complete documentation or page listing). Hovering over a project title will reveal the created date and time and the most recent modified date and time in the following format::

    Created: YYYY-MM-DD HH:MM AM/PM
    Modified: YYYY-MM-DD HH:MM AM/PM

Hovering over a registration title will reveal the registered date and time in the following format::

    Registered: YYYY-MM-DD HH:MM AM/PM

To the left of each project title is a green square button marked with a '+' sign. On the right is the last name of the first listed contributor to the result.
If a project or component returned as a result has multiple contributors, "et al." is appended to the first contributor's last name. 

Clicking the '+' button adds the result to the "Adding" column. Alternatively, the user can click the "Add all" link to the right of the
"Results" title to add the results shown on the page to the "Adding" column. When a result is moved to the "Adding" column,
it is removed from the "Results" column. Projects in the "Results" column have, instead of the green button to the left, a grey button with a '-'
sign. Clicking this button removes the corresponding result from the "Adding" list and returns it to the "Results" page it was found on.
To the right of the "Adding" title is a "Remove All" link. Clicking this link moves all added results back to the "Results" column.

Only a "Cancel" button is available on the modal until a result has been put in the "Adding" column. Once one result has been added,
a green "Add" button becomes visible to the right of the "Cancel" button. Clicking "Add" refreshes the page to show the newly linked projects
listed in the Components widget.


.. _component-format:

Projects, components, and links are listed in the Components widget with their title, contributors, number of contributions, category and privacy symbols,
and a collapsible recent activity section. If one of the items is private, to the left of the title and category symbol is a lock. If the element
is public, there is no symbol. Titles link to the project/component/link's overview page. Below the titles are the names of the first three contributors;
if there are more contributors, they are indicated by the addition of "& __ more." Clicking on a contributor's name brings the user to the contributor's
public profile. Clicking on "& __ more" brings the user to the overview page for the project/component/link.

To the right of the element's title is a caret indicating that there is expandable content. Clicking the caret expands the element's information
to include a "Recent Activity" section. In this section, on the left, are dates and times of logged actions. On the right is a description of each action.
Only the three most recent actions are listed in the "Recent Activity" section.

Components are listed in the order in which they were added. Components can be dragged and dropped to re-order. After re-ordering components,
the user can refresh the page and the changes will still be visible.

Tags Widget
----------------
**Purpose:** The Tags widget allows users to provide keywords relevant to their project, helping OSF visitors more easily find their work.

The Tags widget is located below the components widget. When no tags are added, users with read+write or admin permissions
see text that reads "Add a tag." If the user is not a contributor on the project, or only has read permissions, and no
tags have been added the Tags widget is not visible.

Contributors with read+write or admin permissions can add a tag by clicking in the "Add a tag" field and typing a keyword.
Pressing the return key will add the tag. Adding a comma after a tag and pressing the space bar, as if making a list, will
also add a tag. Tags appear in blue boxes with a black 'x' to the right of the text. Clicking the 'x' allows the user to remove the tag.

Hovering over a tag darkens the background color. Clicking on a tag brings the user to search results page, where the query was the
tag name.

.. _activity:

Recent Activity Widget
--------------------
**Purpose:** The Recent Activity widget shows users the logged actions for the viewed project or component, its children, and its registrations.

The Recent Activity widget appears below the Tags widget. Below the panel title, "Recent Activity," is muted text that reads::

    All times displayed at ____ UTC offset.

Times are displayed in local time, and the correct offset is indicated in the above text.

Below this is a list of all logged actions on the project or component, its children, and registrations displayed in chronological order with the most recent
action listed at the top. Actions are listed in two columns—the left shows the date and time (YYYY-MM-DD HH:MM AM/PM).
Hovering over a time shows a tooltip with the date and time in UTC.

In the right column is a description of the log, first listing the user who committed the action, then the action and the
affected component or project. For example::

    [Username] tagged [project] as [tag]
    [Username] added [Username] as contributor(s) to [project name]

User, file, project, component, registration, and wiki names are linked to the relevant pages.

Only the ten most recent logs are shown at once. Pagination behavior is described in detail :ref:`here <pagination>`.