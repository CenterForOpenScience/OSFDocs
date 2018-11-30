.. _wiki:

Wikis
*****

**Purpose:** Wikis can be used as means for documentation, supplementary to files.

The wiki can be accessed via the Project Overview or the "Wiki" link in the grey navigation bar. Every project and component
has a wiki page by default, titled "Home."

Visitors to a wiki or read contributors see the Wiki's title in the top left of the page. Below this on the left is the Menu.
The Menu lists all visible wiki pages for the viewed project/component and all children. Sub-projects and components are collapsed
by default. The menu itself can be collapsed to the left so that none of its content shows. When collapsed, admins and read+write
contributors can still see the options to create a new page or delete the current one.

The middle of the page is covered by the "View" panel. At the top of the "View" panel is a drop-down to select which version of the wiki the user would like to see: Preview or Current. "Current" indicates the name of the user who saved that version of the wiki as well as a timestamp of when the edits were saved. The "Current" version is selected automatically. 

If no content has been added to the wiki, then the "Preview" option is selected automatically. Selecting "Current" does not show a contributor name or a timestamp.

Below the "View" title is the wiki's contents. When a wiki is empty its body reads in italics::

    Add important information, links, or images here to describe your project.

In the top right of the page is a toggle menu. Options are "View," "Edit," and "Compare." "View" is selected by default. 

Comparing versions of the wiki
------------------------------
Clicking "Compare" cuts the width of the View panel in half and adds a second panel titled "Compare." The Compare panel header reads::

    Compare Current version to [dropdown]

If only one version exists, the viewed version is being compared to "Current," which is selected from the drop-down. "Current" lists the name of the contributor who saved the current version and the timestamp of when the save occured. If other versions are available,
the default is to compare the current version to the previous versions. Whichever version is being viewed is the basis for comparison.

To change the version being viewed, the user can select from the drop-down in the View panel header. This will also change what
versions are being compared.

Additions made to the wiki since the version being viewed was saved are highlighted in green in the Compare panel. Deletions
are in red strikethrough text.

Editing the wiki
----------------
Contributors with read+write or admin permissions can edit the wiki. If there is no content in the wiki, it will appear in edit mode by default. If there is already content, these contributors see a third option in the upper right toggle: "Edit."
Selecting "Edit" opens an additional panel on the page. Within this panel is a text box the user can type into. Line numbers appear on the left hand side of the edit pane and the preview pane. Formatting options are available
in the toolbar, or the user can make use of Markdown syntax. The toolbar options, from left to right, are as follows: format text in bold, format text in italics, insert a hyperlink, insert a blockquote, insert a code sample, insert an image, insert a numbered list, insert a bulleted list, insert a heading, insert a horizontal line, undo, redo.

While the user types, the editor will suggest Markdown syntax. While editing, if the View panel is open, it displays a preview
of the changes. The user can change this via the dropdown, however.

Users can save their changes by clicking the "Save" button below the text-edit box. Saving refreshes the page and closes all panels
except for the View panel. The current version is automatically displayed.

To undo unsaved changes, the user can click "Revert" next to the "Save" button. This will revert to the last saved version, but keep the
"Edit" panel open.

Multiple contributors can edit the wiki page at the same time. When this happens, each user sees the other editing users' profile pictures
above the formatting buttons in the "Edit" panel. Hovering over their images shows their usernames. All changes are displayed live. Users can
edit other users' work.

If the user makes changes but attempts to navigate away from the page, no alerts or warnings appear. When the user returns to the Edit
panel, however, their in-progress edits are still available.

Adding Files
^^^^^^^^^^^^
**Purpose**: to allow users to add files stored in their OSF Storage to their wiki.

The user can embed files uploaded to OSF Storage (from Quick Files or any of their projects) in their wiki. They must enter the file's GUID directly into the editor using the following markdown syntax::
  
    @[osf](GUID)

Embedding images
^^^^^^^^^^^^^^^^
**Purpose**: To allow users to add images to their wiki content.

To embed an external image into a wiki page, the user must click the **Image** icon in the toolbar, and enter the URL of the desired image into the modal that appears.

The user can also drop and drop local images directly into the wiki editor, and have those images rendered in the wiki.
  
To resize an embedded image to an exact size, the user can add the following syntax to the end of the image markdown::
  
    ![enter image description here](http://osf.io/GUID/download =[number]x[number])
    
To resize the image to fit the page, the user must add the following syntax after the URL::

  ![enter image description here](image URL =100%x)

To resize the image to a relative size, the user must use a percentage::

    ![enter image description here](image URL =n%x)
    
    
Adding a new wiki page
----------------------

To add a wiki page, users can click the "New" button in the Menu. A modal appears::

    Add new wiki page
    [text field]
    [Cancel][Add]

If the user attempts to save a new wiki page with no name, a red text alert appears below the text field::

    The new wiki page name cannot be empty

Wiki names cannot be over 100 characters. If the user attempts to give a name that is too long a red text alert appears below the text field::

    The new wiki page name cannot be more than 100 characters.

After the user creates a new wiki page, the page refreshes and they are brought to the Edit panel for the new page. The View panel
is also open.

If the user names a wiki page but does not add or save any content and then navigates away, the wiki is still saved as a new page.

Wiki pages are listed in the menu in alphabetical order with the Home wiki at the top.

Deleting a wiki page
--------------------

To delete a wiki page, the user must visit it by clicking the name in the Menu. At the top of the menu a "Delete" button is visible. Clicking
this opens a modal::

    Delete wiki page?
    Are you sure you want to delete this page?
    [Cancel][Delete]

Deleting the page refreshes the browser and brings the user to the View panel of their Home wiki. The Home wiki has no option to delete it.

Renaming a wiki page
--------------------
To rename a wiki page, the user must visit it. The name is at the top left of the page. Clicking this opens a text entry
field where the user can revise the title. To submit changes, the user must click the green check button to the right of
the field. To cancel the change, the user can click on the grey ‘x’ button to the right of the check button. To clear the
contents of the field, the user can click on a small ‘x’ within the text field. If the user makes changes but clicks out
of the text box without saving the edits, the changes are lost.

Commenting on Wikis
-------------------
Users have the ability to comment on wiki pages. Under the "Commenting" section of "Settings," users can select::
    
    Commenting
    *Only contributors can post comments
    *When the project is public, any OSF user can post comments
    [Save]

Comments are made by selecting the "Comments" text bubble icon to the far right of the upper project band (right of "Settings"). Selecting the icon will display a panel where comments are viewable and may be added. 

Publicly Editable Wikis
^^^^^^^^^^^^^^^^^^^^^^^
**Purpose:** Publicly editable wikis allow users who are not listed as contributors on a project to edit the wiki contents.

.. _todo: Update with .48 release


