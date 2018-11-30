.. _privacy:

Privacy Settings
****************

**Purpose:** Privacy settings allow the user to make their work visible or invisible to non-contributors.

Privacy settings are adjustable on the project/component level. Individual files or wiki pages cannot be made private or public.

To change the privacy setting of a project or component and all of its contained information, an admin must visit the project/component's
overview page. In the upper right corner, there is a toggle. The selected option will be greyed-out and unselectable. The other
option is an active button.

When a project or component is created, it is private by default. The selected toggle option reads "Private" and the unselected option
reads "Make Public." If an admin clicks "Make Public" a modal opens::

    Warning
    Please review your projects, components, and add-ons for sensitive or restricted information before making them public.

    Once they are made public, you should assume they will always be public. You can return them to private later, but search engines (including Google’s cache) or others may access files before you do.
    [Cancel][Confirm or Continue]

If the project or component has no components nested within it, the options in the modal are "Cancel" or "Confirm". Confirming the choice to make the project public refreshes the page; the toggle then indicates that it is a public project.

If the project or component has components nested under it, the options in the modal are "Cancel" or "Continue". Selecting "Continue" opens a new modal containing::

    Adjust your privacy settings by checking the boxes below. 

    Checked projects and components will be public. 
    Unchecked components will be private.

This is followed by links to select all components or none of the components, and a list of components one level below the project/component the user is in. A checkbox appears in the left column of the list. To its right, if there are more components nested below, a "+" appears, followed by the component's name. Clicking the "+" sign reveals the next level of nested component(s), and so on. The checkboxes reflect the current privacy setting of the component, with the exception of the project or component the "make public" or "make private" button was clicked in. A checked box indicates a component is public; an unchecked box indicates the component is private. Clicking the "Make all public" or "Make all private" links sets privacy of all components, including those nested (even if not visible in an unexpanded list). 

Clicking "Cancel" at this point abandons all changes. 
Clicking "Continue" refreshes the modal to display the names of all projects and components affected by the change in two lists: made public and made private. There are three buttons: "Back," "Cancel," and "Confirm." Clicking "Back" takes the user back to the previous modal to further edit which components are selected. Clicking "Cancel" abandons all changes. Clicking "Confirm" refreshes the page and alters privacy settings of the selected projects and components. 

If an admin clicks "Make Private" on a public project a modal opens::

    Warning
    Please review your projects, components, and add-ons for sensitive or restricted information before making them public.

    Once they are made public, you should assume they will always be public. You can return them to private later, but search engines (including Google’s cache) or others may access files before you do.
    [Cancel][Confirm or Continue]

If the project or component has no components nested within it, the options in the modal are "Cancel" or "Confirm". Confirming the choice to make the project private refreshes the page; the toggle then indicates that it is a private project.

If the proejct or component has components nested under it, the options in the modal are "Cancel" or "Continue." Selecting "Continue" opens the same modal described in this step above in the 'make public' scenario. 

Users who have permission to view a private component can see its logged history in the :ref:`Recent Activity <activity>` of
the component's parent. Users who do not have permission to see the component do not see these logs in the Recent Activity.

Private projects/components listed on a project overview or in a user's profile display a lock to the left of their title to users
that have permission to see the project/component. This lock is only shown the components list. The project/component title is
listed in the files browser without a lock.

When a user visits a public project that has private components that they do not have permissions to see, the files browser
and components list shows "Private Component" or "Private Project."

When a user is on a search results page or public profile that displays a component that is a child of a private project,
that component is titled "--private project-- / [Component title]."


