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

If the user connected add-ons to the original project, the add-ons will be transfered to the fork. In this case, the following modal will appear::
  
    Are you sure you want to fork this project?
    * Because you have authorized the GitHub add-on for this project, forking it will also transfer your authentication to the forked project.
        [Cancel][Fork]

If the user creates a fork from a project that contains add-ons that the user did not connect, the following modal will appear::
  
    Are you sure you want to fork this project?
    * Because the [add-on] has been authorized by a different user, forking it will not transfer authentication to the forked project
    (the above line repeats for each add-on)
    [Cancel][Fork]

Clicking "Fork" creates the fork.

Alternatively, the user can visit the project's forks page by clicking "Forks" in the project's navigation bar or by clicking
"View Forks" from the "Duplicate" modal. From there, a new fork can be created by clicking "New Fork."

After a new fork is created, the user is brought to their forked project's overview.

The files, wiki contents, components, history, and tags are all copied into the new project. The only contributor on the new project is the user who created the fork. Below the fork's title and "Contributors" row in the top left of the page, there is a URL that links to the original project's "Project Overview" page in the following format::

    Forked from [URL] on [Date] [Time]

If the original project contains add-ons that the user connected, the following blue dismissable confirmation message appears at the top of the forked project::
  
    [add-on] authorization copied to forked project.
    
If the original project is private but it has an add-on with public content, the forked project will have the following blue nondismissable alert at the top of the page::
  
  Warning: This OSF project is private, but the [add-on folder/repo/etc. name] is public. The files in this [add-on folder/repo/etc.] can be viewed on [add-on provider] here [links to the folder/repo/etc.].
  
The logs in the Recent Activity widget that were created before the fork link to the relevant pages from the original project.

Below the fork's title in the top left of the page, there is a URL that links to the original project's "Project Overview" page. 

When the user navigates to the original project's "Project Overview" page and looks at the "Duplicate" button, the number of times the project has been duplicated will appear in the button. The user can also see this number next to the "Forks" column in the "Duplicate" modal.
