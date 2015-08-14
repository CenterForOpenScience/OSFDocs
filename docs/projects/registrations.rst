**Purpose:** Registrations can be created to preserve the state of a project at a given moment in time.

Registrations create a read only copy of a project. Admins can create a registration of a project, and all sub-projects and components
to which they also have admin rights by visiting the Registrations page via their project's grey navigation bar.

On the Registrations page, all pending, retracted, and completed registrations are listed. Each registration lists its project name,
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

Creating a Registration
-----------------
Clicking "New Registration" opens a modal. If the project is the top level project of a tree, the modal reads::

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

After selecting a template the user is provided a form through which they can provide information about their project and registration.

Embargos
------------
**Purpose:** Embargo periods allow the user to keep a registration private for a limited period of time.

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

The date selected must be more than two days in the future but cannot be greater than four years away. If the user attempts to
select a date not within the appropriate range, after attempting to confirm their registration the calendar widget is opened
and a dismissable yellow growlbox alert shows at the top right of the page::

    Invalid embargo end date
    Please choose a date more than two days, but less than four years, from today.

Selecting "Enter registration into embargo" opens another text field below the dropdown titled "Embargo end date." Clicking
into the text field opens a calendar widget for the user to select a date for the conclusion of the embargo. On the selected date,
the registration will become public.

If the user selects "Make registration public immediately" the registration is never private—regardless of the project's privacy setting.

To confirm their decision, the user follows further instruction::

    Registration cannot be undone, and the archived content and files cannot be deleted after registration. Please be sure
    the project is complete and comprehensive for what you wish to register.

    Type "register" if you are sure you want to continue

The user must type "register" into the text field below the instructions. The field is not case sensitive. If the user enters
alternative text, no action occurs. When the user types "register" a blue submit button labeled "Register Now" appears. Pressing
the return key does not submit the form.

A confirmation modal appears::

    Are you sure you want to register this project?
    The content and version history of Wiki and OSF Storage will be copied to the registration.
    [Cancel][Register]

If additional add-ons are connected to the project, the modal includes information about their registration behavior.

Clicking the "Register" button brings the user to the Registrations page for their project. The new registration is listed.
A dismissable blue alert is at the top of the page::

    Files are being copied to the newly created registration, and you will receive an email notification containing a
    link to the registration when the copying is finished.

While the files are being copied, a tag to the left of the registration's title reads "Archiving." While the registration
is archiving, it cannot be visited. Once the archival is complete, the tag is removed and the title becomes a link to the registration's overview.


If the registration was entered into an embargo period, a lock indicating that the project is private appears to the left of the title.
An additional tag reads "Pending Embargo."


Registration Overview
---------------
.. todo:: finish registrations (archive folders, log linking to original, alert at top of page)

Retractions
---------------

DOIs and ARKs
------------------

pending tags on registrations page (including privacy lock)
embargos
approving an embargo
retractions
retraction tags on registrations page
DOIS
citation widget when doi exists
registrations in search
commenting
