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

Contributors who do not have permissions to register the project or component see the same message. Contributors who do have permissions to register the project or component see the message:: 

    There have been no completed registrations of this project. You can start a new registration by clicking the “New Registration” button, and you have the option of saving as a draft registration before submission. For a list of the most viewed and most recent public registrations on the Open Science Framework, click here.

If it is a sub-project or component, however, they see additional text::

    To register the entire project "[project name]" instead, click here.

The link provided sends the user to the parent project's registrations page.

Admins see an additional "New Registration" button.

Only contributors can comment or view comments on a registration.

Registration Overview
---------------
**Purpose:** A registration's Overview shows the state of the project at the time of registration and links to the supplement.

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

**The following describes creating a registration from the project page. Subsequent documentation covers the Preregistration Challenge workflow**


Clicking "New Registration" on a project's registrations page opens a modal that reads::

    Registration creates a frozen version of the project that can never be edited or deleted but can be withdrawn. Your original project remains editable but will now have the registration linked to it. Things to know about registration:
    *Ensure your project is in the state you wish to freeze before registering.
    *Consider turning links into forks.
    *Registrations can have embargo periods for up to four years. If you choose an embargo period, the registration will automatically become public when the embargo expires.
    *Withdrawing a registration removes the contents of the registrations but will leave behind a log showing when the registration was created and withdrawn.
    Continue your registration by selecting a registration form:
    *Prereg Challenge 
    *Open-Ended Registration 
    *OSF-Standard Pre-Data Collection Registration 
    *Replication Recipe (Brandt et al., 2013): Pre-Registration 
    *Replication Recipe (Brandt et al., 2013): Post-Completion 
    *Pre-Registration in Social Psychology (van 't Veer & Giner-Sorolla, 2016): Pre-Registration 
    [Cancel][Create Draft]

The user selects a template and clicks create draft. The user is provided a form through which they can provide information about their project and
registration. The template may be one page or many pages. At the bottom of each page, the user is presented with the date and time the draft registration was last saved, and two buttons: [Save as Draft][Preview for Submission]. 

Clicking "Save as Draft" saves the draft registration and returns the user to the project's Draft Registrations tab. 
Clicking "Preview for Submission" presents a preview of the registration, followed by two buttons: [Continue editing] and [Register]. 

Clicking "Continue editing" returns the user to the "Edit draft registration" page. 
Clicking "Register" brings up a modal::

    Before you continue...
    *The content and version history of Wiki and OSF Storage will be copied to the registration 
    Registration choice: 
    [Dropdown selections:] Make registration public immediately
    Enter registration into embargo (selecting this option brings up a field, "Embargo End Date" where user must select date to embargo)
    [Cancel][Continue]

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

Registration failed
-----------------
Occasionally, a registration will fail. When a registration fails, the following modal will appear::

    Registration failed
    There was a problem completing your registration. Please try again later. If this should not have occured and the issue persists, please report it to support@osf.io. 
    [Back to project]

Creating a registration in Preregistration Challenge workflow
------------
User navigates from cos.io/prereg to osf.io/prereg, where the user is greeted by two options: login to the OSF or create a new account. 

Whether a user logs into the OSF or creates a new account first, the landing page for prereg provides the user the option to "Start a new preregistration." If the user already has a draft registration, there is also an option to "Continue working on an existing preregistration." If the user has project(s), an option to "Preregister a project you already have on the OSF" is also displayed. 

Clicking "Continue working on an existing preregistration" displays a box::
    
    Go to an existing preregistration:

with a text box for users to begin typing the name of the preregistration. A list of matching projects will display below the text box as the user types. Only draft preregistrations that are using the Prereg Challenge template will populare this list. Selecting one fills the text box with the name of the preregistration with an "X" above the box to cancel the selection, and provides a button to "Edit Draft." Clicking "Edit Draft" takes the user to the editable preregistration template.

Clicking "Preregister a project you already have on the OSF" displays a box::

    Preregister an existing project:

with a text box for users to begin typing the name of the project. A list of matching projects will display below the text box as the user types. Selecting one fills the text box with the name of the project with an "X" above the box to cancel the selection, and provides a button, "Preregister." Clicking the "Preregister" button takes the user to the project's Registrations page, with a dismissable notification::

    You have been redirected to the project's registrations page. From here you can initiate a new Draft Registration to complete the registration process. 

From here the user will follow the workflow for creating a registration from the project's registrations page. 

Clicking "Start a new preregistration" will open a box::
    
    Please provide a title for your project:

with a text form to type the preregistration title and a button to "Continue >". Clicking continue will open a model containing terms and conditions for the Preregistration Challenge. Accepting the terms will land the user on the "Edit draft registration page" for the Prereg Challenge registration template. 

In each of these cases, the user will have to fill out the Prereg Challenge registration template, which is several pages. At the bottom of each page, the user is provided with buttons, "Save as draft" or "Next page." On the last page, the "Next page" button is replaced by a "Submit for review" button. 

Clicking "Submit for review" pops up a modal with a Notice of Consent for the Preregistration Challenge. The user must agree to the terms and click "Continue." Clicking "Cancel" returns the user to the registration preview page. Clicking "Continue" prompts the user to choose to either make the registration public immediately or choose an embargo (as in the normal workflow). After making this selection, the user lands on the "Registrations" page for the project and is presented with a dissmissable notice::

    Your submission has been received. You will be notified within ten business days regarding the status of your submission. If you have questions, you may contact us at prereg@cos.io. 

The preregistration appears in the "Draft registrations" tab with the label "Pending Review." There are buttons to [Preview] or [Delete] the registration. Clicking [Preview] opens the preview of the registration, with a button to go [Back] to the Registrations tab. Clicking [Delete] pops up a modal:: 
    
    Are you sure you want to delete the registration? [Cancel][Delete]


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
    whichever comes first. [Cancel Registration]

The Cancel Registration button appears only for Project Administrators. If no action is taken by any administrator, the registration is approved. The Cancel Registration button appears only for Project Administrators.

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
    whichever comes first. The embargo will keep the registration private until the embargo period ends. [Cancel Registration]

The Cancel Registration button appears only for Project Administrators.

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

End embargo early
---------------
If an embargoed registration is already approved, it may be made public by the project administrators. One the registration page, a "Make Public" button appears. Clicking it generates the following modal::

    End embargo early
    By clicking confirm, an email will be sent to project administrator(s) to approve ending the embargo. If approved, this registration, including any components, will be made public immediately. This action is irreversible.
    [Cancel] [Confirm]  

Selecting "Confirm" reveals a green dismissable alert at the top of the page::

    Email sent
    The administrator(s) can approve or cancel the action within 48 hours. If 48 hours pass without any action taken, then the registration will become public.

The following email will be sent to project contributors::

    Hello [username],

    You initiated a request to end the embargo for a registration of [project name]. The embargoed registration can be viewed here: URL

    To approve this change and to make this registration public immediately, click the following link: URL

    To cancel this change, click the following link: URL

    Sincerely yours,

    The OSF Robots

Clicking the disapproval link will immediately cancel this request and the original embargo date will remain intact. This registration will be made public when all project administrators approve the change or 48 hours pass, whichever comes first.

Withdrawals
---------------
**Purpose:** Withdrawals allow admins to make the contents of a registration private.

A registration that is not embargoed is public. Users cannot "undo" a registration or make its contents private, but admins
do have the option to withdraw the registration. To withdraw a registration the admin visits the registration's settings page.
Non-admins do not see the link to the Settings page.

Only the entirety of a registration can be withdrawn—individual components cannot be withdrawn. If an admin visits a component's
settings page to attempt to withdraw the registration of the individual component, a panel reads::

    Withdraw Registration
    Withdrawing children components of a registration is not allowed. Should you wish to withdraw this component, please
    withdraw its parent registration here.

Visiting the settings page of the parent registration shows a panel where the admin can withdraw the registration:

    Withdraw Registration
    Withdrawing a registration will remove its content from the OSF, but leave basic metadata behind. The title of a
    withdrawn registration and its contributor list will remain, as will justification or explanation of the withdrawal,
    should you wish to provide it. Withdrawn registrations will be marked with a withdrawn tag.
    [Withdraw Registration]

Clicking "Withdraw Registration" brings the user to a page where they must provide a justification::

    Withdraw Registration
    Withdrawing a registration will remove its content from the OSF, but leave basic metadata behind. The title of a withdrawn
    registration and its contributor list will remain, as will justification or explanation of the withdrawal, should you
    wish to provide it. Withdrawn registrations will be marked with a "withdrawn" tag. This action is irreversible.
    Please provide your justification for withdrawing this registration.

A text field allows the user to enter their reason for withdrawing the registration. No justification is required, however.

The user must then type the first word of the name of the project into an additional text field to continue.

After withdrawing the registration, they are brought to the registration's overview where a non-dismissable alert is visible at the top
of the page::

    This project is currently pending entering into a withdrawn state.

Visiting the settings shows, instead of the "Withdraw Registration" button, text that reads::

    This registration is already pending withdrawal.

On the registrations page of the registered project, and next to the registered components titles on the registration's overview,
a tag reads "Pending withdrawal."

The user will receive a notification that the withdrawal has been initiated::

    Hello [username],

    You initiated a withdrawal of your registration t3st. The registration can be viewed here: URL

    If approved, the registration will be marked as withdrawn. Its content will be removed from the OSF, but leave basic metadata behind. The title of a withdrawn registration and its contributor list will remain, as will justification or explanation of the withdrawal, should you wish to provide it.

    To approve this withdrawal, click the following link: URL

    To cancel this withdrawal, click the following link: URL

    Note: Clicking the disapproval link will immediately cancel the pending withdrawal. If you neither approve nor disapprove the withdrawal within 0 hours of midnight tonight (EDT) the registration will become withdrawn. This operation is irreversible. Sincerely yours,

    The OSF Robots

Non-admins also receive an email::

    Hello [username],

    We just wanted to let you know that [withdraw-initiator username] has requested a withdrawal for the following registration: URL

    Sincerely yours,

    The OSF Robots

If an admin disapproves of the withdrawal, they are brought to the registration where a green dismissable alert is shown at the
top of the page::

    Your disapproval has been accepted and the withdrawal has been cancelled.

If an admin disapproves, but then an admin attempts to approve the withdrawal, they are brought to a pages that reads::

    Invalid Token
    This registration is not a pending withdrawal.

If an admin approves the withdrawal, they are brought to the withdrawal's page. At the top is a green dismissable alert::

    Your approval has been accepted.

Withdrawn pages show the registration's title, contributors, type of registration supplement (though no link to contents),
date of the project's creation, date of the registration, and description. At the top of the page is a red, non-dismissable alert
that reads::

    This project is a withdrawn registration of this project; the content of the project has been taken down for the reason(s) stated below.

Below the description is the "Justification for Withdrawal" section. The admin's justification is provided below the header. If
no justification was entered, the section reads::

    No justification provided during withdrawal.

No other options or widgets are shown on the page.

If a user visits the registered project's registrations page, the withdrawn registration is still listed, with a link to the
withdrawal page. A red tag to the left of the link reads "Withdrawn."

Withdrawn registrations are shown in search results of the OSF. To the right of their name, in the result, is "(Withdrawn Registration)."

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


Registering with Add-ons
----------------
**Purpose:** The OSF can archive the contents of add-ons to include them in registrations.

Add-on contents can often be copied and included in registrations, but certain limits affect how complete this action is.

Draft figshare files cannot be copied. If a registration is begun for a project that contains draft figshare files, an alert is
shown to the user after they click the "Register" button::

    Before you continue...
    The figshare project settings test contains private content that we cannot copy to the registration. If this content
    is made public on figshare we should then be able to copy those files. You can view those files here.
    If you choose to continue with the registration at this time we will exclude the contents of any addons that are not copyable.
    These files will not appear in the final registration.
    [Cancel][Continue]

Continuing will register the project—no archive of the figshare files will be present.

If the figshare add-on contains only public figshare files, they will be copied and included in the registration.

No other add-on produces a similar warning during registration, though they are presented to the user in a final confirmation modal
before completing the registration.

Copies of the most recent version of all other add-ons will be present. OSF Storage maintains complete version history.