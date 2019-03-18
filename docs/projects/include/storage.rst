.. _storage:

File Storage
************

**Purpose:** The OSF allows users to store, view, and share files. Users can take advantage of the built in OSF Storage or connect to an add-on.

Files can be accessed via the Files Browser available on the :ref:`Project Overview <overview>` or the Files page. A project
or component's files page can be accessed by clicking on "Files" in the grey navigation bar.

OSF Storage is the default file storage tool on the OSF. Users are given unlimited storage for free when they create an account. Files can be up to 5gb.

Files Browser
-------------
The Files Browser displays the project tree and, above that, a toolbar with available actions.
The project or component that the user is currently visiting is at the top of the project tree, followed by the files uploaded
to that project/component, then components that are housed within that project/component. The tree continues to extend until
all children have been listed. Every project and component displays its OSF Storage folder
and any contained folders. If any :ref:`add-ons <add-ons>` are connected, they are displayed within the project
or component. To the left of each add-on, project, component, and file is an icon representing the item. Every item in the
tree is labeled with its title. 

New versions of files that the user has previously viewed will be formatted in bold in the file tree, indicating that a new version of the file is available. Selecting the file to view will unbold the file in the file tree.


Nested projects, components, add-ons, and files are indented to indicate their hierarchy.
On page load, top level storage add-ons and OSF Storage are expanded, meaning their contents are visible.
Projects and components nested immediately within the top level project/component are expanded as well, as are their storage
add-ons and OSF Storage. Third level components (i.e. children of the currently viewed project/component's children) are not expanded.
Expanded elements are indicated by a minus sign to their left. Collapsed elements are indicated by a plus sign.
Clicking on these symbols expands and collapses the contents. All icons stay the same when their corresponding elements
are open or collapsed. Folders are an exception to this rule: When a folder is expanded, its icon is an open folder.
When a folder is collapsed, its icon is a closed folder.

Double clicking on a project or component returned as a result brings the user to the
corresponding project overview page. Double clicking on a file brings the user to the file's :ref:`details page <files_view>`.
Double clicking on a storage item like an add-on or OSF Storage returns the file tree with the item selected.

There are three columns in the Files Browser: "Name," "Size," and "Downloads." The "Names" column is sortable in alphabetical order. Sorting
by name re-orders files within each project or folder to be in alphabetical or reverse alphabetical order. The "Size" column
lists the file size for each file. The "Downloads" column lists the number of downloads for each file; if there have been no downloads,
the number is O.

By default, the toolbar displays a "Search" button and an information button, indicated by an "i."
Clicking on the information button pulls up a modal that is displayed inside the panel and reads::

    How to Use the Files Browser
    Select Rows: Click on a row (outside the name) to show further actions in the toolbar.
    Select Multiple Files: Use Command or Shift keys to select multiple files.
    Open Files: Click a file name to go to the file.
    Open Files in New Tab: Press Command (or Ctrl in Windows) and click a file name to open it in a new tab.
    Copy Files: Press Option (or Alt in Windows) while dragging a file to a new folder or component.
    [Close]

Searching in the Files Browser
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
**Purpose:** The search bar in the Files Browser allows the user to quickly find a file they are seeking.

Clicking the "Search" button opens a text field for the user to enter their query into. The "Search" button disappears when
the text field opens and a cancel button indicated by an 'x' appears to the right. The user can type their query into the text field
and any element in the file tree (projects, components, OSF Storage, add-ons, files) matching the search are displayed in the
Files Browser. Only titles are searched—not file contents. Elements that do not match the query are hidden.
Selecting a result returns the file tree and closes the search field. The selected result is then highlighted within
the file tree.

.. _OSF-storage:

Uploading to OSF Storage
^^^^^^^^^^^^^^^^^^^^^^^^
**Purpose:** Users can upload files to be stored by the OSF.

If the user is a contributor with read+write or admin :ref:`privileges <contributors>`, then selecting an OSF Storage element
adds two additional buttons to the toolbar: "Upload" and "Create Folder."

Clicking the "Upload" button will open a file selector that allows the user to search their
computer to select files for upload. Any file type can be uploaded. Folders cannot be uploaded. While a file is uploading,
the title is displayed in the storage folder it is being uploaded to. A progress bar indicates the file's upload progress.
An 'x' button to the right of the upload bar allows the user to cancel the upload.

Users can also drag and drop a file to be uploaded into any storage add-on or OSF Storage folder that they have read+write or
admin privileges on.

.. _folders:

Folders
^^^^^^^
**Purpose:** Folders allow users to organize items within a project or component's OSF Storage.

Clicking the "Create Folder" opens a text field and two buttons that replace the existing buttons in the toolbar: a "Create" and a
cancel button labeled with an 'x.'  The user can type a folder name into the text field and press the return key or click "Create"
to save the change. Folder titles can be any length; if they are too long to fit in the panel, an ellipsis cuts off the excluded content.
The folder appears, collapsed, within the OSF Storage folder selected. Any number of folders can be created. Folders can be nested
within one another.

Clicking on a folder shows the "Upload," "Create Folder," "Search," and "i" buttons in the toolbar as well as two additional options:
"Delete Folder" and "Rename."

Clicking "Rename" opens a text field with the current folder title editable within it. A pencil icon
allows the user to confirm the changes and an 'x' button cancels the changes. If the user attempts to rename the folder but leaves
the text field empty, no changes are saved. After renaming a folder, before showing the newly renamed folder, a temporary message appears in the folder's row that reads: "Renaming [folder name]." Once the changes have been saved, a temporary confirmation message in the the folder's row reads::

    Successfully renamed.

Clicking the "Delete Folder" option opens a modal within the Files Browser::

    Delete "[folder name]"?
    This folder and ALL its contents will be deleted. This action is irreversible.
    [Cancel][Delete]

Confirming the deletion removes the folder and all contained files from the Files Browser.

Clicking on any folder or OSF Storage folder that has files contained within it adds one additional button to the toolbar—"Download as zip."
Clicking this button immediately issues the download of a zip file containing all files and folders that were housed within the selected
element. On refresh, the download count for each file in the folder is incremented by one.

Single File Actions
^^^^^^^^^^^^^^^^^^^
Selecting a single file from any add-on or folder adds four additional buttons to the toolbar, beyond the default "Search" and "i:"
"Download," "View," "Delete," and "Rename." Selecting a file from OSF Storage also adds a "Check-out file" button. 

Clicking the "Rename" button when a file is selected opens a text field with the current folder title editable within it. A pencil icon allows the user to confirm the changes and an 'x' button cancels the changes. If the user attempts to rename the file but leaves the text field empty, no changes are saved. 

After renaming a file, before showing the newly renamed file, a temporary message appears in the file's row that reads: "Renaming [filename]." After the save is complete, the file's row reads::

    Successfully renamed.

When the user renames a file, they must add the file extension to the end of the new name; otherwise, the file will be corrupted and its contents will not show. When the user leaves off the file extension, the icon to the left of the file changes from the file format logo, to an icon with a white page. When the user clicks on the corrupted file to view it on the "File Details" page, a nondismissable yellow alert appears that reads::
  
    Unable to detect encoding of source file.
    
The user needs to rename the file again and append the file extension to the end of the name. The icon with the file format logo will return to the left of the file, and the file's contents will show on the "File Details" page.

Clicking the "Check out file" button when a file stored in OSF Storage is selected opens a modal::

    Confirm file check out?
    This would mean other contributors cannot edit, delete or upload new versions of this file as long as it is checked out. You can check it back in at any time.
    [Cancel][Check out file]

Upon checking out the file, for all users, a checked-out icon appears to the left of the file name. For the user who has checked out the file, the "Check out" button changes to a "Check in" on the toolbar. 

On the File Detail page, for any contributor who has not checked the file out, a growl box appears::
    
    File is checked out. This file has been checked out by a [collaborator] (link to profile page of user who has checked out file). It needs to be checked back in before any changes can be made. 

For an ADMIN contributor who has not checked the file out, the "Check-out" button becomes "Force Check in"

Clicking the "Force Check in" button brings up a modal::
    
    Force check in file? This will check in the file for all users, allowing it to be edited. Are you sure?
    [cancel][Force check in]

For the user who has checked out the file, clicking the "Check in" button refreshese the page and returns the "Check out" button. 

Clicking the "Delete" button when a file is selected opens a modal within the Files Browser::

    Delete "[file name]"?
    This action is irreversible.
    [Cancel][Delete]

Confirming the deletion removes the file from the Files Browser. Provenance information is left behind for deleted files - including files deleted on third-party add-ons. Information includes: file name, provider, name of user who deleted the file, timestamp of deletion, hashes, file size, date the file was last seen, and provider path.

Clicking the "View" button brings the user to the file's :ref:`Details page <details>`.

Clicking the "Download" button downloads the file. On refresh, the download count for the file increments by one.

Multiselection of items
^^^^^^^^^^^^^^^^^^^^^^^
**Purpose:** Selecting multiple items at once allows users to perform batch actions.

Users can select multiple items by holding down the Command or Shift keys.

When multiple items are selected, a "Delete Multiple" button shows in the toolbar. Clicking this button opens a modal
within the Files Browser that reads::

    Delete multiple files?
    This action is irreversible.
    [list of items being deleted]

    [Cancel][Delete All]

If one of the selected items is a folder, the modal contains an extra warning::

    Some of the selected items are folders. This will delete the folder(s) and ALL of their content.

Only files and folders from within the same project or component can be multi-selected.

Multiple files cannot be downloaded at once unless they are in a :ref:`folder <folders>`.

File Detail Page
----------------

**Purpose:** Most files can be rendered in the browser on the File Detail Page. The File Detail page also provides access to previous versions of a file. 

Along the left side of the page is a sidebar enabling access to the other files associated with the project. 

In the bottom left is a Tags widget, for files stored on OSF Storage. When no tags are added, users with read+write or admin permissions see text that reads “Add a tag.” If the user is not a contributor on the project, or only has read permissions, and no tags have been added, the Tags widget is not visible.
Contributors with read+write or admin permissions can add a tag by clicking inside the widget and typing a keyword. Pressing the return key will add the tag. Adding a comma after a tag and pressing the space bar, as if making a list, will also add a tag. Admins and read+write contributors will see an ‘x’ to the right of the tag that they can click to remove the tag. Clicking on a tag brings the user to the OSF search results page with the tag name query.

If the file can be rendered, it displays in the MFR on the page. For a list of which file types render in the browser, go to `<https://gist.github.com/felliott/8fd378c25c1b7122b6e7992cdb2693a7>`_. 

If the file is an image with a height greater than 200, the user can click anywhere on the image to zoom in on details. Once zoomed in, the user can scroll around the image to navigate to different details. Above the image is a question mark icon. The user can hover over the question mark to view on-screen instructions in a tooltip::
  
    HiRes: Click on the image to view in higher resolution when available
    
    Zoom: Click on the image and use the mouse wheel to zoom in and out
    
    Navigate: Move the mouse cursor to navigate through the magnified image
    
For images that have a height less than 200, zoom is disabled and no instructions are available.

Above the rendered file are three buttons: "Download", "View", "Revisions." If the project is public, a "Share" button is also visible.

For ADMIN contributors and files stored on OSF Storage, the "Check Out" button appears. 

For ADMIN and READ+WRITE contributors, a "Delete" button is also present. For these users and plain text files, an "Edit" button appears. If the "Edit" button is present, the "View" and "Edit" buttons can be toggled on and off, so that the user can edit and view the changes simultaneously. Clicking the "Edit" button opens the "Edit" pane, where the user can make changes to their file. At the top of pane is a green "Live editing mode" button that, when clicked, opens the following modal::
  
  Connected to collaborative file editing
  This page is currently connected to collaborative file editing. All edits made will be visible to contributors with write permission in real time. Changes will be stored but not published until you click the "Save" button.
  [Close]

At the bottom of the pane are "Revert" and "Save" buttons. Clicking **Revert** reverts to the last saved version of the file. Clicking **Save** saves the newest changes and updates the file to a new version. 

If the file is stored on a 3rd-party add-on, a link to view the file on the 3rd-party service appears above the rendered file.

Clicking the **Revisions** button shows all versions of the file in a table format::
  
    Version ID | Date | User | Download | MD5 | SHA2

The latest version (indicated by the version ID) is displayed in the MFR by default. All IDs of the previous verisons are linked and render in the MFR when clicked. The "Download" column presents a button to download the version of the file. The MD5 column shows the hash value with a button to copy the hash to the user's clipboard. To the right of MD5 is a question mark icon that, when clicked, gives a definition of the hash in a tooltip::

    MD5 is an algorithm used to verify data integrity.

The SHA2 column shows the hash value with a button to copy the hash to the user's clipboard. To the right of SHA2  is a question mark that, when clicked, gives a definiton of the hash in a tooltop::
  
    SHA-2 is a cryptographic hash function designed by the NSA used to verify data integrity.

Admin and read+write contributors can rename the file directly from the "File Detail" page. The workflow and behavior is the same
as :ref:`Renaming a project <renaming_project>`. Clicking the filename in the top left of the page turns the title into a textbox wherein the user can
make changes to the title. To the right of the textbox are a green checkmark and an "x" that the user can click to either save their
changes or cancel their changes, respectively.

After clicking the green check mark, the following dismissable confirmation message appears in the top right of the page::
  
    Success
    Your file was successfully renamed. To view the new filename in the file tree below, refresh the page.

Storage Add-Ons
---------------
**Purpose:** Storage add-ons can be used to connect a user's OSF account to another file storage system, increasing their
capacity to share files via the OSF and bringing more functionality to their projects.

Information on connecting add-ons to user accounts :ref:`can be found here. <user-addon>` Information on individual add-on's
behavior :ref:`can be found here. <add-ons>`
