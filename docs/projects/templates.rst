**Purpose:** Templates copy one project's structure so that the bare bones of a new project can be easily created.


Any public project can be used as a template, meaning that any OSF user can copy the tree structure and component titles of that
project.

Templates can be created by visiting the project the user wishes to copy and clicking the "Duplicate" button in the upper right
hand corner. A modal opens, the second column reads::

    Templated From
    This option will create a new project, using this project as a template. The new project will be structured in the
    same way, but contain no data.
    [Copy Project Structure]

To the right of the column title is a count of the number of times the project was used as a template.

Clicking "Copy Project Structure" opens a modal::

    Are you sure you want to create a new project using this project as a template?
    Any add-ons configured for this project will not be authenticated in the new project.
    [Cancel][Create]

Clicking "Create" creates the new project.

The user is then brought to their new project. The project title is "Templated from ____," referencing the project from
which it copied its structure. The user who created the templated project is the only contributor.

Alternatively, a project can be created from a template via the :ref:`quick-tasks <Quick Tasks>` panel on the My Dashboard page.
There, after providing a title an description, the user can select a template::

    Template (Optional)
    Start typing to search. Selecting project as template will duplicate its structure in the new project without importing
    the content of that project.

A dropdown below these instructions allows the user to search their own projects and public projects on the OSF. As the user
types a query into the dropdown's text field, results matching the query are displayed. Selecting a result and clicking
"Create" brings the user to their new project based on their selected project's structure.

Projects created from templates copy the tree structure, including all components, subprojects, and subcomponents. The titles of
components and projects are preserved in the new project. Public links are also copied, though private links are not. No files
or wiki contents are copied.

