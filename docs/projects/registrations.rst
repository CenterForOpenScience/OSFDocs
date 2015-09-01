**Purpose:** Registrations can be created to preserve the state of a project at a given moment in time.

Registrations create a read only copy of a project. Admins can create a registration of a project, and all sub-projects and components
to which they also have admin rights by visiting the registrations page via their project's grey navigation bar.

On the registrations page, all pending, retracted, and completed registrations are listed. Each registration lists its project name,
registration date and time, contributors, and contributions, in the same format as provided for components on the
:ref:`Project Overview <component-format>`.

When no registrations have been made, non-contributors see text explaining this::

    There have been no registrations of this component. For a list of the most viewed and most recent public registrations
    on the Open Science Framework, click here.

The link provided sends the user to the :ref:`Public Activity page <public-activity>`.

Contributors who do not have permissions to register the project or component see the same message. If it is a sub-project or component,
however, they see additional text::

    To register the entire project "[project name]" instead, click here.

The link provided sends the user to the parent project's registrations page.

Admins see an additional "New Registration" button.

Only contributors can comment or view comments on a registration.

Registration Overview
---------------
**Purpose:** A registration's Overview shows the stat eof the project at the time of registration and links to the supplement.

The Registration Overview has all the components of a :ref:`Project Overview <overview>`. A watermark in the background
says "read-only" repeatedly. At the top of the page is a non-dismissable blue alert::

    This project is a registration of this project; the content of the project has been frozen and cannot be edited.

The alert links to the project that the registration is a copy of.

In addition to the Project Overview's :ref:`metadata <overview-metadata>`, there is an additional field, "Registration Supplement."
This field lists the name of the registration template the registrant used. Clicking the name links the user to a page with
a copy of the template and the registrant's responses.

The Files widget does not allow for editing of file names, reorganization of files, or deletion of files, however. Only
downloads are permitted. Files are saved within their storage add-ons and OSF Storage, grouped into folders. The folders are
titled "Archive of [storage add-on]." These folders are collapsed by default.


Creating a Registration
-----------------
Clicking "New Registration" on a project's registrations pageopens a modal. If the project is the top level project of a
tree, the modal reads::

    Register [project name]
    You are about to register the component [project name] including all components and data within it.
    Registration creates a permanent, time-stamped, uneditable version of the project. If you would prefer to register
    only one particular component, please navigate to that component and then initiate registration. After clicking Register,
    you will next select a registration form.
    [Cancel][Register]

If the user is attempting to register a sub-project or component, however, the modal reads::

    Register [project name]
    You are about to register the component [project name] including all components and data within it. This will not
    register its parent, [project name]. If you want to register the parent, please go here. After clicking Register,
    you will next select a registration form.
    [Cancel][Register]

The link provided sends the user to the parent project's Registrations page.

Clicking "Register" brings the user to a new page titled "Register." Below the title is a paragraph of information::

    Registration creates a frozen version of the project that can never be edited or deleted but can be retracted.
    You can register your project by selecting a registration form, entering information about your project, and then
    confirming. You will be able to continue editing the original project, however, and the frozen version with timestamps
    will always be linked to the original. Retracting a registration will leave behind metadata about when the registration
    was created and retracted but removes the contents of the registration.

    * A registration can be made public immediately or entered into an embargo period of up to four years. At the end of
    the embargo period, the registration will automatically become public.
    * Before initiating a registration, make sure that the project is in the state that you wish to freeze. Consider turning links into forks.
    * Start by selecting a registration form from the list below. You can hit your browser's back button if the selected
    form is not appropriate for your use.

Below the information is a dropdown with different registration templates: "Open-Ended Registration," "OSF-Standard Pre-Data Collection
Registration," "Replication Recipe (Brandt et al., 2013): Pre-Registration," "Replication Recipe (Brandt et al., 2013): Post-Completion."

After selecting a template the user is provided a form through which they can provide information about their project and
registration. There, the user also chooses whether or not to embargo the project. After finishing the form, the user must
confirm the registration::

    Registration cannot be undone, and the archived content and files cannot be deleted after registration. Please be sure
    the project is complete and comprehensive for what you wish to register.

    Type "register" if you are sure you want to continue

The user must type "register" into the text field below the instructions. If the user enters
alternative text, no action occurs. When the user types "register" a blue submit button labeled "Register Now" appears. Pressing
the return key does not submit the form.

A confirmation modal appears::

    Are you sure you want to register this project?
    The content and version history of Wiki and OSF Storage will be copied to the registration.
    [Cancel][Register]

If additional add-ons are connected to the project, the modal includes information about their registration behavior.

Clicking the "Register" button brings the user to the registrations page for their project. The new registration is listed.
A dismissable blue alert is at the top of the page::

    Files are being copied to the newly created registration, and you will receive an email notification containing a
    link to the registration when the copying is finished.

While the files are being copied, a tag to the left of the registration's title reads "Archiving." While the registration
is archiving, it cannot be visited. Once the archival is complete, the tag is removed and the title becomes a link to the
registration's overview.

When visiting the :ref:`Project Organizer <organizer>`, a project or component that is still being archived will have "[Archiving]"
written to the right of its title.

Embargos
------------
**Purpose:** Users can opt to make their registration public immediately or after a period of time.

Prior to completing their registration, the user decides on an embargo period. Text explains the embargo period to the user::

    You can choose whether to make your registration public immediately or embargo it for up to four years. At the end
    of the embargo period the registration is automatically made public. After becoming public, the only way to remove a
    registration is to retract it. Retractions show only the registration title, contributors, and description to indicate
    that a registration was made and later retracted.

    If you choose to embargo your registration, a notification will be sent to all other project contributors. Other
    administrators will have 48 hours to approve or cancel creating the registration. If any other administrator rejects
    the registration, it will be canceled. If all other administrators approve or do nothing, the registration will be
    confirmed and enter its embargo period.

Below the "Registration Choice" header is a dropdown for the user to make their selection. Options are: "Make registration
public immediately," "Enter registration into embargo."

Registrations with No Embargo
^^^^^^^^^^^^^^^^
**Purpose:** Registrations that have no embargo are public immediately after confirmation.

If the user selects "Make registration public immediately" the registration is never private—regardless of the project's
privacy setting. After confirming the registration, the user is brought to their registrations Page. A blue dismissable alert
is at the top of the page::

    Files are being copied to the newly created registration, and you will receive an email notification when the copying is finished.

The user and all other admins on the project receive an email::

    Hello [username],

    [You or username] initiated a registration of your project [project name].
    To approve this registration, click the following link: URL
    To immediately cancel this registration, click the following link: URL
    Note: If you take no action within 48 hours, the registration will be automatically approved. This operation is irreversible.

    Sincerely yours,

    The OSF Robots

Clicking to approve the registration brings the user to the registration's overview. There, a green dismissable alert is
at the top of the page::

    Your registration approval has been accepted.

Clicking to disapprove the registration brings the user to the project's overview. There, a green dismissable alert is
at the top of the page::

    Your disapproval has been accepted and the registration has been cancelled.

Non-admins also receive an email notifying them of the registration::

    Hello [username],

    We just wanted to let you know that [registrant username] has initiated the following pending registration: URL

    Sincerely yours,

    The OSF Robots

Clicking the link brings the user to the registration with the following alert at the top of the page::

    This project is currently pending registration, awaiting approval from project administrators. This registration will
    be final and enter the embargo period when all project administrators approve the registration or 48 hours pass,
    whichever comes first.

If no action is taken by any administrator, the registration is approved.

If a user attempts to visit a link to or approve a cancelled registration, they are brought to a page that reads::

    Resource Deleted
    This resource has been deleted

.. todo:: after fixed, log what happens if you try to cancel an approved registration

Before a registration has been approved or cancelled, the registrations page shows a tag to the left of the registration
that reads "Registration Pending." Visiting that registration also shows the tag to the left of the components titles on the
overview page.

Prior to a registration's approval, the privacy settings from the registered project and its components apply. After approval,
the entirety of the registration is public.

Registrations with an Embargo
^^^^^^^^^^^^^^
**Purpose:** Embargo periods allow the user to keep a registration private for a limited period of time.

Selecting "Enter registration into embargo" opens another text field below the dropdown titled "Embargo end date." Clicking
into the text field opens a calendar widget for the user to select a date for the conclusion of the embargo. On the selected date,
the registration will become public.

The date selected must be more than two days in the future but cannot be greater than four years away. If the user attempts to
select a date not within the appropriate range, after attempting to confirm their registration the calendar widget is opened
and a dismissable yellow growlbox alert shows at the top right of the page::

    Invalid embargo end date
    Please choose a date more than two days, but less than four years, from today.

After confirming the registration, the user is brought back to the registrations page for the registered project. A blue alert
is at the top of the page::

    Files are being copied to the newly created registration, and you will receive an email notification when the copying is finished.

If the registration was entered into an embargo period, a lock indicating that the project is private appears to the left
of the title on the registration page. Before an admin approves the embargo, an additional tag reads "Pending Embargo."
These also appear to the left of component titles on the registration's overview. After the embargo is approved, the tag
reads "Embargoed" until the embargo period is concluded.

If a registration is embargoed, all admins on the project, including the registrant, receive an email::

    Hello [username],

    We just wanted to let you know that [username] has requested an embargoed registration for a project you administer.
    The proposed registration can be reviewed here: URL.
    If approved, a registration will be created for the project and it will remain private until it is retracted, manually
    made public, or the embargo end date has passed on [date].
    To approve this action click the following link: URL
    To disapprove this action, click the following link: URL
    Note: Clicking the disapproval link will immediately cancel the pending embargo and the registration will
    be deleted. If you neither approve nor disapprove the embargo within 48 hours from
    midnight tonight (EDT) the registration will remain private and enter into an embargoed state.

    Sincerely yours,

    The OSF Robots

Non-admins also receive an email::

    Hello [username],

    We just wanted to let you know that [registrant username] has requested an embargoed registration for a project you
    contribute to.
    If approved, a registration will be created for the project, viewable here: URL, and it will remain
    private until it is retracted, manually made public, or the embargo end date has passed on [date].

    Sincerely yours,

    The OSF Robots

Visiting the embargoed registration before it is approved shows a non-dismissable alert at the top of the page::

    This project is currently pending registration, awaiting approval from project administrators. This registration will
    be final and enter the embargo period when all project administrators approve the registration or 48 hours pass,
    whichever comes first. The embargo will keep the registration private until the embargo period ends.

After an embargo is enacted, a red non-dismissable alert is shown at the top of the page::

    This component is currently embargoed. It will remain private until its embargo date, [date], passes or an admin
    manually makes it public.

An admin can change the privacy setting on an embargoed project or components they are an admin on. If an admin clicks the
"Make Private" button, a modal appears::

    Warning
    Once a registration is made public, you will not be able to make the registration private again. After making the
    registration public, if you discover material in it that should have remained private, your only option will be to
    retract the registration. This will eliminate the registration, leaving only basic information of the project title,
    description, and contributors with a notice of retraction.
    [Cancel] [Make Public]

Public components or projects in an embargo cannot be made private.

After an embargo ends, the registration and its components are made public.

Retractions
---------------
**Purpose:** Retractions allow admins to make the contents of a registration private.

A registration that is not embargoed is public. Users cannot "undo" a registration or make its contents private, but admins
do have the option to retract the registration. To retract a registration the admin visits the registration's settings page.
Non-admins do not see the link to the Settings page.

Only the entirety of a registration can be retracted—individual components cannot be retracted. If an admin visits a component's
settings page to attempt to retract the registration of the individual component, a panel reads::

    Retract Registration
    Retracting children components of a registration is not allowed. Should you wish to retract this component, please
    retract its parent registration here.

Visiting the settings page of the parent registration shows a panel where the admin can retract the registration:

    Retract Registration
    Retracting a registration will remove its content from the OSF, but leave basic metadata behind. The title of a
    retracted registration and its contributor list will remain, as will justification or explanation of the retraction,
    should you wish to provide it. Retracted registrations will be marked with a retracted tag.
    [Retract Registration]

Clicking "Retract Registration" brings the user to a page where they must provide a justification::
    Retract Registration
    Retracting a registration will remove its content from the OSF, but leave basic metadata behind. The title of a retracted
    registration and its contributor list will remain, as will justification or explanation of the retraction, should you
    wish to provide it. Retracted registrations will be marked with a "retracted" tag. This action is irreversible.
    Please provide your justification for retracting this registration.

A text field allows the user to enter their reason for retracting the registration. No justification is required, however.

The user must then type the first word of the name of the project into an additional text field to continue.

After retracting the registration, they are brought to the registration's overview where a non-dismissable alert is visible at the top
of the page::

    This project is currently pending entering into a retracted state.

Visiting the settings shows, instead of the "Retract Registration" button, text that reads::

    This registration is already pending a retraction.

On the registrations page of the registered project, and next to the registered components titles on the registration's overview,
a tag reads "Pending Retraction."

Admins on the project receive a notification that the retraction has been initiated::

    Hello [username],

    We just wanted to let you know that [username] has initiated a retraction for the following registration: URL

    To approve this action click the following link: URL

    To disapprove this action, click the following link: URL

    Note: Clicking the disapproval link will immediately cancel the pending retraction. If you neither approve nor disapprove
    the retraction within 48 hours of midnight tonight (EDT) the registration will become retracted. This operation is irreversible.

    Sincerely yours,

    The OSF Robots

Non-admins also receive an email::

    Hello [username],

    We just wanted to let you know that [retractor username] has requested a retraction for the following registration: URL

    Sincerely yours,

    The OSF Robots

If an admin disapproves of the retraction, they are brought to the registration where a green dismissable alert is shown at the
top of the page::

    Your disapproval has been accepted and the retraction has been cancelled.

If an admin disapproves, but then an admin attempts to approve the retraction, they are brought to a pages that reads::

    Invalid Token
    This registration is not a pending retraction.

If an admin approves the retraction, they are brought to the retraction's page. At the top is a green dismissable alert::

    Your approval has been accepted.

Retraction pages show the registration's title, contributors, type of registration supplement (though no link to contents),
date of the project's creation, date of the registration, and description. At the top of the page is a red, non-dismissable alert
that reads::

    This project is a retracted registration of this project; the content of the project has been taken down for the reason(s) stated below.

Below the description is the "Justification for Retraction" section. The admin's justification is provided below the header. If
no justification was entered, the section reads::

    No justification provided during retraction.

No other options or widgets are shown on the page.

If a user visits the registered project's registrations page, the retracted registration is still listed, with a link to the
retraction page. A red tag to the left of the link reads "Retracted."

Retracted registrations are shown in search results of the OSF. To the right of their name, in the result, is "(Retracted Registration)."

DOIs and ARKs
------------------
**Purpose:** DOIs and ARKs can be issued to provide means of citation alternate to the OSF URL.

Public, meaning non-embargoed, registrations can be given DOIs and ARKs. To do so, admins visit the registration's page and
click the "Create DOI/ARK" link below the "Date Created" field. Clicking opens a modal::

    Create identifiers
    Are you sure you want to create a DOI and ARK for this project?
    [Cancel][Create]

Clicking "Create" turns the link to text that reads::

    Creating identifiers

After several seconds, the text changes again to read::

    Identifiers: DOI [DOI identifier] | ARK [ARK identifier]

Both identifiers link to an EZID page for the registration.

When a DOI has been created for a project, the citation widget updates to reflect the doi.org URL instead of the registration's osf.io
URL.
