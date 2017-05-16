**Purpose:** Templates copy one project's structure so that the bare bones of a new project can be easily created.

**Using a public project as a template**

Any public project can be used as a template, meaning that any OSF user can copy the tree structure and component titles of that
project. A user can also copy their private projects using this same workflow.

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

**Using a personal project as a template**

Alternatively, if the project that the user wants to use as a template is one of their own, they can create a new templated project from their dashboard.

Templates can be created by clicking the **Create new project** button on the dashboard. In the modal that appears, the user will need to enter a title for their project and then click **More**. The following drop-down section will unfold::
  
    Description
    Enter project description [texbox]
    
    Template (optional)
    Start typing to search your projects. Selecting project as template will duplicate its structure in the new project without importing the content of that project.
    Select a project to use as a template [drop-down menu of the user's projects]
    
When the user selects one of their projects as a template from the drop-down menu, and then clicks **Create**, the following modal will apppear::
  
    New project created successfully!
    [keep working here][Go to new project]

If the user clicks **Go to new project**, they will see the project they created from the template. The new project will be titled according to what the user entered into the modal. "Templated from" will not be part of the title when the user creates a templated project from their dashboard.

If the user clicks **Keep working here**, the page will reload and the user will remain on their dashboard.
    