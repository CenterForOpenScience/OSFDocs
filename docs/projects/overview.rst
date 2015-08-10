
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

The next link is to the :ref:`Statistics page <statistics>`. This page shows analytics about the project and its visitors.

The next link is to the :ref:`Registrations page <registrations>`. This page lists all registrations of the viewed project.

The next link is to the :ref:`Forks page <forks>`. This page lists all the forks of the viewed project.

The next link is to the :ref:`Sharing page <contributors>`. This page lists the project's contributors and allows the user to create
:ref:`view-only links <view-only>`. This page is not visible to non-contributors.

The final link is to the :ref:`Settings page <project-settings>`. This page allows admins to configure the project. This page
is not visible to non-contributors.

Metadata
-------
**Purpose:** Every project has associated information about that project—its title, contributors, etc. This is metadata about that project.
The metadata is displayed at the top of the Project Overview to orient users to the project's basic information.

At the top of the Project Overview is the project's title. Below the title is the list of contributors. Below this is a row listing
the "Date Created" and "Last Updated" date. Below these two dates is the "Category" field. Below this is the project description.

The project title can be updated by a contributor with administrative or read+write :ref:`permissions <contributors>`. These
contributors can click on the title. This opens a text entry field where the user can revise the title. To submit changes, the user
must click the green check button to the right of the field. To cancel the change, the user can click on the grey 'x' button
to the right of the check button. To clear the contents of the field, the user can click on a small 'x' within the text field.
If the user makes changes but clicks out of the text box without saving the edits, the changes are lost.

The :ref:`contributors <contributors>` list is preceded by a title that reads "Contributors:" This title is a link to the "Sharing" page. Following
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

Below the description, the page is populated by widgets—panels that contain information and allow actions for specific parts of a project.

Wiki Widget
-----------
**Purpose:** The Wiki widget provides a preview of wiki contents.

The first widget is the Wiki widget.  In the upper right corner of the widget is a button that links the user to the Wiki page.
When the :ref:`Home wiki page <wiki>` has hot been edited to include content, contributors
with read+write or admin priviliges see "No wiki content" displayed inside the panel. If the user has created additional
wiki pages with content, but has no content on the Home wiki page, the panel still displays "No wiki content." If the project
is being viewed by a non-contributor and the Home wiki has no content, then the widget is not displayed at all.

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
    [Cancel][Add]

The first field in the modal is an empty text field with placeholder text that reads "Component Title." The user can enter a title of any length, however,
on save, only the first 200 characters will be saved to the title.

The user can add the component without selecting a category. To choose one, however, the user clicks on the dropdown menu labeled "--Category--"
and selects any of the available options. If the user selects a category but does not enter a title, a red text alert appears below the
"Component Title" field::

    This field is required.

After clicking the "Add" button, the button becomes deactivated and reads "Adding" until the page refreshes and the user is brought into the
new component.

Clicking the "Add Links" button opens a modal::

    Add Links
    [text field: "Search projects"]
    [Search all projects][Search my projects]

Below the search buttons are two columns, one labeled "Results" and one labeled "Adding."

The user can enter their query in the "Search projects" text field. If they select the "Search Projects" button, all public OSF projects,
components, and registrations whose title matches their query will be returned. Five results will be displayed, with additional pages listed below (see
the description of pagination on the :ref:`Watchlist <pagination>` for complete documentation or page listing). To the left of each
project title is a green square button marked with a '+' sign. On the right is the last name of the first listed contributor to the result.
If a project or component returned as a result has multiple contributors, "et al." is appended to the first contributor's last name.

Clicking the '+' button adds the result to the "Adding" column. Alternatively, the user can click the "Add all" link to the right of the
"Results" title to add the results shown on the page to the "Adding" column. When a result is moved to the "Adding" column,
it is removed from the "Results" column. Projects in the "Results" column have, instead of the green button to the left, a grey button with a '-'
sign. Clicking this button removes the corresponding result from the "Adding" list and returns it to the "Results" page it was found on.
To the right of the "Adding" title is a "Remove All" link. Clicking this link moves all added results back to the "Results" column.

Only a "Cancel" button is available on the modal until a result has been put in the "Adding" column. Once one result has been added,
a green "Add" button becomes visible to the right of the "Cancel" button. Clicking "Add" refreshes the page to show the newly linked projects
listed in the Components widget.

Projects, components, and links in the Components widget

Components are listed in the order in which they were added. Components can be dragged and dropped to re-order. After re-ordering components,
the user can refresh the page and the changes will still be visible.

Tags Widget
----------------
**Purpose:** The Tags widget allows users to provide keywords relevant to their project, helping OSF visitors more easily find their work.

The Tags widget is located below the components widget.