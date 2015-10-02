
**Purpose:** Wikis can be used as means for documentation, supplementary to files.

The wiki can be accessed via the Project Overview or the "Wiki" link in the grey navigation bar. Every project and component
has a wiki page by default, titled "Home."

Visitors to a wiki or read contributors see the Wiki's title in the top left of the page. Below this on the left is the Menu.
The Menu lists all visible wiki pages for the viewed project/component and all children. Sub-projects and components are collapsed
by default. The menu itself can be collapsed to the left so that none of its content shows. When collapsed, admins and read+write
contributors can still see the options to create a new page or delete the current one.

The majority of the page is covered by the View panel. Below the "View" title is the wiki's contents. When a wiki is empty its body reads::

    No wiki content

In the top right hand of the page is a toggle. Options are "View" and "Compare." View will be selected by default. Clicking
"Compare" cuts the width of the View panel in half and adds a second panel titled "Compare." The Compare panel header reads::

    Compare ____ version to [dropdown]

If only one version exists, the viewed version is being compared to "Current," which is selected from the dropdown. If other versions are available,
the default is to compare the current version to the previous version. Whichever version is being viewed is the basis for comparison.

To change the version being viewed, the user can select from the dropdown in the View panel header. This will also change what
versions are being compared.

Additions made to the wiki since the version being viewed was saved are highlighted in green in the Compare panel. Deletions
are in red strikethrough text.

Contributors with read+write or admin permissions can edit the wiki. These contributors see a third option in the upper right toggle: "Edit."
Selecting "Edit" opens an additional panel on the page. Within this panel is a text box the user can type into. Line numbers appear on the left hand side of the edit pane and the preview pane. Formatting options are available
at the top of the page, or the user can make use of Markdown syntax. While the user types, the editor will suggest Markdown syntax. While editing, if the View panel is open, it displays a preview
of the changes. The user can change this via the dropdown, however.

Users can save their changes by clicking the "Save" button below the text-edit box. Saving refreshes the page and closes all panels
except for the View panel. The current version is automatically displayed.

To undo unsaved changes, the user can click "Revert" next to the "Save" button. This will revert to the last saved version, but keep the
Edit panel open.

Multiple contributors can edit the wiki page at the same time. When this happens, each user sees the other editing users' profile pictures
above the formatting buttons in the Edit panel. Hovering over their images shows their username. All changes are displayed live. Users can
edit other users' work.

If the user makes changes but attempts to navigate away from the page, no alerts or warnings appear. When the user returns to the Edit
panel, however, their in progress edits are still available.

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

To delete a wiki page, the user must visit it by clicking the name in the Menu. At the top of the menu a "Delete" button is visible. Clicking
this opens a modal::

    Delete wiki page?
    Are you sure you want to delete this page?
    [Cancel][Delete]

Deleting the page refreshes the browser and brings the user to the View panel of their Home wiki. The Home wiki has no option to delete it.

To rename a wiki page, the user must visit it. The name is at the top left of the page. Clicking this opens a text entry
field where the user can revise the title. To submit changes, the user must click the green check button to the right of
the field. To cancel the change, the user can click on the grey ‘x’ button to the right of the check button. To clear the
contents of the field, the user can click on a small ‘x’ within the text field. If the user makes changes but clicks out
of the text box without saving the edits, the changes are lost.


Publicly Editable Wikis
^^^^^^^^^^^^^^
**Purpose:** Publicly editable wikis allow users who are not listed as contributors on a project to edit the wiki contents.

.. _todo: Update with .48 release
