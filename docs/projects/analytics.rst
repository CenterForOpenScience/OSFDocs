**Purpose:** The Analytics page of a project is designed to provide contributors with additional information about visitors to their
project.


Analytics pages are accessible via the grey navigation bar in every project. When a project is private, only the contributors
have access to the Analytics page. When a project is public, any visitor can see it. Read only contributors who attempt
to visit the Analytics page of a private project are brought to a new page displaying an error::

    Forbidden
    You do not have permission to perform this action. If this should not have occurred and the issue persists, please report
    it to support@osf.io.


When an :ref:`admin or read+write <permissions>` contributor visits the Analytics page of a :ref:`public <privacy>` project,
they are shown several widgets identifying visitor behavior. If these contributors visit the Analytics page of a private project
they can see any data that was created from the project during times it was public. If there is no such data, the widgets
displayed show no information.

When viewing the Analytics page, on the top left, a date range is selected. Users can click the range to revise it and update the
widgets displayed below. To the right of the date range is a dropdown that allows the user to segment the audience (e.g. into visit
location, referrers, etc.). The next option is titled, "Widgets & Dashboard." When the user clicks a widget title from this dropdown,
a new widget is added to the page. On the far right is text that identifies which project's analytics are being viewed.

Below these options are widgets that inform the user about project visitors. These can be reordered by dragging and dropping.
Many have additional filter and sort options. If there are more widgets than can appear on the page, the user must scroll down
to view the rest of the contents.

Widgets can be refreshed. They can also be removed from the Analytics page by clicking the 'X' in that appears when hovering
in their upper right hand corner. Clicking this 'X' opens a modal::

    Are you sure you want to delete this widget from the dashboard?
    [Yes] [Cancel]

If the user clicks yes, the modal is closed and the widget is removed. Widgets can be collapsed by clicking the minimize
button in their upper right hand corner. When collapsed, only their title is shown. Widgets can be expanded by clicking the
expand button in the upper right hand corner. When expanded, the widget opens as a modal over the screen.

