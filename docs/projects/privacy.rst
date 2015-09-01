**Purpose:** Privacy settings allow the user to make their work visible or invisible to non-contributors.

Privacy settings are adjustable on the project/component level. Individual files or wiki pages cannot be made private or public.

To change the privacy setting of a project or component and all of its contained information, an admin must visit the project/component's
overview page. In the upper right corner, there is a toggle. The selected option will be greyed-out and unselectable. The other
option is an active button.

When a project or component is created, it is private by default. The selected toggle option reads "Private" and the unselected option
reads "Make Public." If an admin clicks "Make Public" a modal opens::

    Warning
    Once a component is made public, there is no way to guarantee that access to the data it contains can be completely
    prevented. Users should assume that once a component is made public, it will always be public. The rest of the project,
    including other components, will not be made public. Review your component for sensitive or restricted information
    before making it public. Are you absolutely sure you would like to continue?
    [Cancel][Make Public]

Confirming the choice to make the project public refreshes the page; the toggle then indicates that it is a public project.

If an admin clicks "Make Private" on a public project a modal opens::

    Warning
    Making a component private will prevent users from viewing it on this site, but will have no impact on external sites,
    including Google's cache. Would you like to continue?
    [Cancel][Make Private]

Confirming refreshes the page. The toggle will indicate that the project is private.

Adjusting the privacy of a project or component only affects that particular element—not any of its children (sub-projects/components).

Users who have permission to view a private component can see its logged history in the :ref:`Recent Activity <activity>` of
the component's parent. Users who do not have permission to see the component do not see these logs in the Recent Activity.

Private projects/components listed on a project overview or in a user's profile display a lock to the left of their title to users
that have permission to see the project/component. This lock is only shown the components list. The project/component title is
listed in the files browser without a lock.

When a user visits a public project that has private components that they do not have permissions to see, the files browser
and components list shows "Private Component" or "Private Project."

When a user is on a search results page or public profile that displays a component that is a child of a private project,
that component is titled "--private project-- / [Component title]."


