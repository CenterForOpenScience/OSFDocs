.. _quickfiles:

Quickfiles
**********

**Purpose**: To allow users to upload public files quickly and independently from projects.

Every user has their own Quick Files page and can be found in the :ref:`OSF navigation bar <navigation>` as the "My Quick Files" tab. Clicking this tab takes the user to a list where they can upload and access their quick files.

The "Quick Files" page is in table format, with the following columns of metadata::

    Name | Size | Version | Downloads | Modified
    
The modified date is in the following format: YYYY-MM-DD 00:00 AM/PM.

All quick files can be viewed on their respective "File Detail" page. If a user has uploaded quick files, their quick files will be listed on their OSF profile page. If the user has not uploaded files to Quick Files, this section will not appear on their profile page. Quick files appear in the main OSF search under "Files" with the following source::
  
    From: <username's> Quick Files

Uploading Quick Files
---------------------

When the Quick Files page is empty, an upload zone appears in place of the file's table with the following helper text::
  
    Drop files here to upload

The user can drag and drop files into the upload zone. Only single file uploads are supported. If dragging and dropping more than one file into the upload zone, a red dismissable progress bar/error message appears in the top right of the page::
  
    Cannot upload multiple files

The user can also click the **Upload** button in the toolbar to select a file from a dialog box. Only one file can be selected for upload at a time.

Once a file is uploaded, a temporary confirmation message appears above the files list::
  
    This file has been added

A progress bar appears in the top right of the page with the following title::
    
    A file has been added

Quick Files toolbar
-------------------
**Purpose**: allows the user to perform general actions to files.

The following buttons are visible in the toolbar on the Quick Files page:

* Upload: Clicking this button opens a dialog box from which the user can select a file to add to their Quick Files.

* Download as zip: Clicking this button downloads all Quick Files as a zip file.

* Filter: Clicking this button opens a "Filter" box with the helper text "Filter". The user can fitler the files by name and date. An "x" icon appears to the right of the box that, when clicked, closes the Filter.

* i: Clicking this button opens the following information modal::
  
    How to use the file browser
    Upload: Single file uploads via drag and drop or by clicking the upload button.

    Select rows: Click on a row to show further actions in the toolbar. Use Command or Shift keys to select multiple files.

    Folders: Not supported; consider an OSF project for uploading and managing many files.

    Open files: Click a file name to go to view the file in the OSF.

    Open files in new tab: Press Command (Ctrl in Windows) and click a file name to open it in a new tab.

    Download as zip: Click the Download as Zip button in the toolbar to download all files as a .zip.
    [Close]

File toolbar
------------
**Purpose**: allows the user to perform actions to specific files.

The toolbar for individual files appears when the user selects file in its file row. The following buttons are visible when a file is selected:
  
* Upload: Clicking this button opens a dialog box from which the user can select a file to add to their Quick Files.
      
* Share: Clicking this button shows a drop-down window called "Share," and gives the URL of the quick file along with a "Copy" button that, when clicked, copies the URL to the user's clipboard.      

* Download: Clicking this button downloads the file to their browser. 
      
* View: Clicking this button takes the user to the respective file's `File Detail page`_ below.
      
* Move: Clicking this button initiates the "Move to project" workflow. See `Moving Quick Files to Projects`_ below.
      
* Delete: Clicking this button intiates the Delete file workflow. See `Deleting Quick Files`_ below.
      
* Rename: Clicking this button initiates the Rename file workflow. See `Renaming Quick Files`_ below.
      
* Filter: Clicking this button opens a "Filter" box with the helper text "Filter". The user can filter the files by name and date. An "x" icon appears to the right of the box that, when clicked, closes the Filter.

Moving Quick Files to Projects
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
**Purpose**: allows the user to move a Quick File to a project.

Clicking the **Move** button opens the "Move file to project" modal, allowing the user to move the file to a project::
  
      Move file to project
      [Create new project][Connect file to existing OSF project]
      [Cancel]

Clicking the **Create new project** button changes the modal screen to initiate the "Create new project" process. A "Title" field will appear with helper text "Enter project title" along with additional helper text and buttons::
  
    You have selected to create a new public project for your file. Users will still have access to your file unless the project becomes private.
    [Cancel][Back][Move file]

The "Move file" button is disabled until the user enters text into the "Title" field. If the user enters a title, and navigates away from the "Quick Files" page, the project will not be created and the file will remain in "Quick Files. Clicking the **Cancel** button cancels the action and closes the modal. Clicking the **Back** button takes the user to the first modal screen, where they can choose to create a new project or choose an existing project.

To move the file to a new project, the user must enter a title into the field, then click the **Move file** button. Clicking **Move file** moves the file into the newly created project. The following confirmation modal appears::
  
    File was moved successfully!
    [Keep working here][Go to new project]
      
Clicking **Keep working here** closes the modal and keeps the user on their "Quick Files" page. Clicking outside the modal (without clicking a button) also closes the modal and keeps the user on the page. Clicking **Go to new project** takes the user to the new project.

Clicking the **Connect file to existing OSF project** button changes the modal screen to initiate the process of moving a file to an existing project. At the top of the modal is helper text "Choose project" below which is a drop-down menu listing the user's existing projects. Inside the menu is helper text "Click to select." Below the menu is additional helper text and buttons::
  
    The list of projects appearing are projects and components for which you have write access. Registrations are not included here.
    [Cancel][Back][Move file]

The "Move file" button is disabled until the user selects a project from the drop-down menu. If the user selects a project, and navigates away from the "Quick Files" page, the move will not occur and the file will remain in "Quick Files. Clicking the **Cancel** button cancels the action and closes the modal. Clicking the **Back** button takes the user to the first modal screen, where they can choose to create a new project or choose an existing project.

To move the file to an existing project, the user must select a project from the drop-down menu, then click the **Move file** button. If the user selects a private project, red in-line text will appear above the buttons::
  
    Files moved to private projects will no longer be public or discoverable by others.
    
If the user selects a public project, an in-line text will appear above the buttons::
  
    Clicking "Move file" will immediately make changes to your OSF project and move your file.

Clicking **Move file** moves the file into the newly created project, and the following confirmation modal appears::
      
        Files was moved successfully!
        [Keep working here][Go to new project]
          
Clicking **Keep working here** closes the modal and keeps the user on their "Quick Files" page. Clicking outside the modal (without clicking a button) also closes the modal and keeps the user on the page. Clicking **Go to new project** takes the user to the new project.

Deleting Quick Files
^^^^^^^^^^^^^^^^^^^^
**Purpose**: allows the user to delete single or multiple quick files.

Selecting a single file and clicking the **Delete** button opens the following confirmation modal::
  
    Delete "<filename>"?
    This action is irreversible.
    [Cancel][Delete]

Clicking **Cancel** cancels the action, and closes the modal. Clicking **Delete** deletes the file, and a temporary red confirmation message appears in place of the file in the file row::
  
    This file has been deleted.

If selecting multiple files to delete, the button reads "Delete multiple." Clicking the **Delete multiple** button opens the following confirmation modal::
  
    Delete multiple?
    This action is irreversible.
    <filename>
    <filename>
    [Cancel][Delete]

Clicking **Cancel** cancels the action, and closes the modal. Clicking **Delete** deletes the file, and temporary red confirmation messages appear in place of each deleted file in their file rows::
      
    This file has been deleted.
    
If the user navigates away from the "Quick Files" page while the confirmation modal is still open, the file(s) will not be deleted.

Renaming Quick Files
^^^^^^^^^^^^^^^^^^^^
**Purpose**: allows the user to rename their quick file after uploading it.

Clicking the "Rename" button opens a text field in the toolbar along with a pencil icon and an "x" icon to the right of it. The filename will appear in the text field by default. To make changes to the filename, the user must type into the text field, then click the pencil icon to the right of the field. Upon renaming the file, a temporary green confirmation message will appear in the file row::
  
      successfully renamed
    
Or, the user can click the "x" icon to cancel any changes and close the text field.

If the user enters text or other changes into the text field, then leaves the "Quick Files" page without saving the changes, the changes will not be saved to the file.

File Detail page
----------------
**Purpose**: allows the user to view the file on a dedicated page.

The "File Detail" page is the same as a regular file's (see the :ref:`File Detail page <storage>`) with the following exceptions:

 * files cannot be edited
 * files cannot renamed on this page
