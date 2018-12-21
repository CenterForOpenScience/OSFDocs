.. _forks:

Forks
*****

**Purpose:** Forking a project copies the projects contents and creates a new project.

Any public project can be forked, meaning that any OSF user can create their own copy of a project. Forking one project creates
an entirely new project under the forking user's account.

When a project is forked, a log is made on the forks page <INSERT LINK> of that project. Public forks are listed with their title, date forked,
contributors, and number of contributions.

Forking a project
-----------------
Forks can be created by visiting the project the user wishes to copy and clicking the **Fork** icon in the top right
of the "Overview" page. A drop-down menu unfolds, with three options::
    
    [Fork this Project]
    [Duplicate templage]
    [View Forks <(number)>]

Clicking **Fork this Project** from the drop-down menu, opens a confirmation modal::
  
    Are you sure you want to fork this project?
    [Cancel][Fork]
    
If the user is forking their own project on which they connected and authorized add-ons, the add-ons will be transfered to the fork. In this case, the following modal will appear::
      
    Are you sure you want to fork this project?
      * Because you have authorized the <add-on name> add-on for this project, forking it will also transfer your authentication to the forked project.
        [Cancel][Fork]

If the project contains add-ons that were authorized by someone else, the following modal will appear::
  
    Are you sure you want to fork this project?
    * Because the <add-on name> add-on has been authorized by a different user, forking it will not transfer authentication to the forked project.
      You may authorize and configure the <add-on name> add-on in the new fork on the settings page.
      
If the project contains links to other projects, the following modal will appear::
  
    Are you sure you want to fork this project?
    * This project contains links to other projects. Links will be copied into your fork, but the projects that they link to will not be forked.
    If you wish to fork the linked projects, they need to be forked from the original project.
    [Cancel][Fork]

Clicking the **Cancel** button cancels the action and closes the modal. Clicking the **Fork** button closes the modal, while a dismissable
blue alert appears in the top right of the "Overview" page::
  
    Fork Status
    Your fork is being created. You'll receive an email when it's complete.

The user will receive an email titled "Your fork has completed", and the body reads::
  
    The fork of <project title> has been successfully created here: https://osf.io/GUID

Clicking the link in the email takes the user to their forked project.

If a fork fails, the following email is sent to the user::
  
    An error has occurred, and the fork of <node title> on The Open Science Framework was not successfully created. Please log in and try this action again. If the problem persists, please email support@osf.io.

"Overview" page of forked projects
----------------------------------
A fork's "Overview" page is the same as a regular project "Overview" page, except that an additional line of metadata
a is added to the top left of the "Overview" page::
  
    Forked from osf.io/GUID pn YYYY-MM-DD hh:mm AM/PM.

Like any new project, forks are private by default, meaning that until their privacy setting is changed,
they will be listed in the forks page as "Private Fork" to any non-contributor — including contributors on the
project it was forked from.

When a project is forked, all content and metadata, including "Recent Activity" logs, linked projects, and redirect links are copied into the new project. 
The logs in the Recent Activity widget that were created before the fork link to the relevant pages from the original project.

Contributors from the original project are not copied. Only the user who forked the project is listed as a contributor. By default, forks are titled "Fork of [Project's title]." 

If the forked project is private but it has an add-on with public content, the forked project will have the following blue nondismissable alert at the top of the page::
  
  Warning: This OSF project is private, but the [add-on folder/repo/etc. name] is public. The files in this [add-on name] <repo/folder> can be viewed on [add-on provider] here [links to the folder/repo/etc.].

Viewing forks
-------------
Users can view forks in two ways: 1). via the "View Forks" icon in the "Forks" drop-down menu, 2) via the project's 
"Analytics" page.

Clicking the **Forks** icon on the project's "Overview" page causes a drop-down menu to unfold, wherein the "View Forks (#)" button is located.

Clicking the **View Forks** button takes the user to the "Forks" page <https://osf.io/GUID/forks/>.

See the :ref:`Analytics page <analytics_forks>` for information.
