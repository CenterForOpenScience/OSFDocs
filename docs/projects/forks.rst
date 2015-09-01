**Purpose:** Forking a project copies the projects contents and creates a new project.

Any public project can be forked, meaning that any OSF user can create their own copy of a project. Forking one project creates
an entirely new project under the forking user's account.

By default, forks are titled "Fork of [Project's title]."

When a project is forked, a log is made on the forks page of that project. Public forks are listed with their title, date forked,
contributors, and number of contributions. Like any new project, forks are private by default, meaning that until their privacy
setting is changed, they will be listed in the forks page as "Private Fork" to any non-contributor—including contributors on the
project it was forked from.

Forks can be created by visiting the project the user wishes to copy and clicking the "Duplicate" button in the upper right
hand corner. A modal opens, the third column reads::

    Forks
    Fork this project if you plan to build upon it in your own work. The new project will be an exact duplicate of this
    project's current state, with you as the only contributor.
    [Fork this Project]
    [View Forks]

To the right of the column title is a count of the number of forks created.

Clicking "Fork this Project" opens a modal::

    Are you sure you want to fork this project?
    [Cancel][Fork]

If the project had any add-ons connected, notices about what will and will not be included in the fork are provided in the modal.

Clicking "Fork" creates the fork.

Alternatively, the user can visit the project's forks page by clicking "Forks" in the project's navigation bar or by clicking
"View Forks" from the "Duplicate" modal. From there, a new fork can be created by clicking "New Fork."

After a new fork is created, the user is brought to their new project's overview.

The files, wiki contents, components, history, and tags are all copied into the new project. The only contributor on the new project
is the user who created the fork. Below the "Contributors" field is a statement::

    Forked from [URL] on [Date]

The logs in the Recent Activity widget that were created before the fork link to the relevant pages from the original project.

The URL links to the project overview of the project that was forked. The "Duplicate" button on that project's overview, as
well as the count next to "Forks" in the "Duplicate" modal is incremented by one after the fork is created.

.. todo:: forking your own project with add-ons?
