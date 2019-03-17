.. _registrations:

Registrations
*************

**Purpose:** Registrations can be created to preserve the state of a project at a given moment in time.

Registrations create a frozen copy of a project. Admins can create a registration of a project and selected components to which they also have admin rights by visiting the registrations page on the project.

On the registrations page, all pending, withdrawn, and completed registrations are listed. Each registration card lists the project title, date registered, registration title (if applicable), form type, contributors, project description (if applicable), and tags (if applicable). 

When no registrations have been made, non-contributors see the following helper text::

  There have been no completed registrations of this project.
  Learn more about registrations here <help guide>.

Non project admins see the same helper text. Admins on the project see the following helper text::

  There have been no completed registrations of this project.
  Start a new registration by clicking the “New registration” button. Once created, registrations cannot be edited or deleted.
  Learn more about registrations here <help guide>.

On a component, however, the helper text reads::

  There have been no completed registrations of this project.
  Start a new registration by clicking the “New registration” button. Once created, registrations cannot be edited or deleted.
  Learn more about registrations here <help guide>.
  
  To register the entire project <project title> instead, click here <project_registration_page>.

Only contributors can comment or view comments on a registration.

A "Draft registrations" tab is also visible on the "Registrations" page, and is always visible to admins whether or not a draft exists. This page also provides the user with the option to create a new registration. Draft registration cards list the form type, initiator, start date, last updated date, and edit, delete, and register buttons. Clicking **Delete** on a draft registration opens a confirmation modal::
  
    Please confirmation
    Are you sure you want to delete this draft registration?
    [Cancel][Delete]

Clicking **Delete** deletes the draft and directs the user to the list of drafts.

Clicking **Edit** directs the user to the draft form.

The **Register** button is disabled when the form is an incomplete state. Clicking **Register** when enabled directs the user to draft form.

When no draft registrations have been made, helper text reads::
  
  There are no draft registrations of this project.
  Start a new registration by clicking the “New registration” button. Once created, registrations cannot be edited or deleted.

  Learn more about registrations here <help guide>.

Registration Overview
---------------------
**Purpose:** A registration's Overview shows the state of the project at the time of registration and links to the registration form.

The Registration Overview has all the widgets of a :ref:`Project Overview <overview>`, including a line that indicates when the registration was registered in the top left of the page where the rest of the metadata is::
    
    Date registered: year-month-day

The registration has a watermark in the background that says "read-only" repeatedly in order to distinguish it from a project. At the top of the page is a non-dismissable blue alert::

    This registration is a frozen, non-editable version of this project [links to the Project Overview page].

In the top right of the Registration Overview page is a blue button that reads "View Registration Form." Clicking this button takes the user to a page with a noneditable copy of the user's registration form and their responses.

If the registration does not have wiki content, the Wiki Widget is not included on the Registration Overview page, but it is included in the registration's navigation bar. Clicking the tab takes the user to the "Wiki Home" page with the message::
  
    No wiki content.

The Files widget does not allow for editing of file names, reorganization of files, or deletion of files. Only
downloads are permitted. Files are saved within their storage add-ons and OSF Storage, grouped into folders. The folders are
titled "Archive of [storage add-on]." These folders are collapsed by default.

A registration's Recent Activity widget only shows the original OSF project's activity prior to the creation of the registration. Activity related to the registration itself, such as the user's creation of the registration, is only logged into the live project's Recent Activity widget and not the registration's. Logs on the project are as follows:

* Initiated: the administrator who creates the registration is listed in the Recent Activity widget as the oen who initiated the registration.
* Approved: the last administrator to approve the registration is the only admin listed in the Recent Activity widget who approved the registration.
* Canceled: the first administrator to cancel the registration is the only admin listed in the Recent Acvitity widget who canceled the registration.
* Registered: the last administrator to approve the registration is the only admin listed in the Recent Activity widget who registered the registration.

The project's comments are not carried over to the registration.

Admins and read+write contributors can add tags to the registration after it has been registered. The behavior is the same as described in the :ref:`Tags section <tags>`. for the project "Overview" page.

Creating a Registration
-----------------------

Clicking **New registration** on a project's registrations page opens an initiation modal::

  Registration creates a frozen version of the project. Your original project remains editable and will have the registration linked. Things to know about registration:

  * Registrations cannot be edited or deleted.
  * Withdrawing a registration removes its contents, but leaves behind basic metadata: title, contributors, date registered, date withdrawn, and justification (if provided).
  * Registrations can be public or embargoed for up to four years. Embargoed registrations will be made public automatically when the embargo expires.
  
  Continue your registration by selecting a registration form:

  OSF Preregistration
  Open-Ended Registration
  Registered Report Protocol Preregistration 
  Preregistration Template from AsPredicted.org
  OSF-Standard Pre-Data Collection Registration
  Replication Recipe (Brandt et al., 2013): Post-Completion  
  Replication Recipe (Brandt et al., 2013): Pre-Registration 
  Pre-Registration in Social Psychology (van 't Veer & Giner-Sorolla, 2016): Pre-Registration 
  [Cancel][Create draft]

The user must select a form and click **Create draft** to initiate a registration of their project. Each form follows a different template that is either one-page or multiple-pages long. At the bottom of each page, the user is presented with the date and time that the draft registration was last saved, and two buttons: **Save draft** and **Preview for submission**. 

Clicking **Save draft** saves the draft registration and returns the user to the project's Draft Registrations tab. Clicking **Preview for submission** generates a preview of the registration, followed by two buttons: **Continue editing** and **Register**. 

Clicking **Continue editing** returns the user to the "Edit draft registration" page. Clicking **Register** initiates the submission process. If the project has components, a modal will appear from which the user can select components to include and exclude from the registration. All components are selected by default::
  
    Register Project
    Select components to be included in the registration.
    Select: <Select All> | <Clear All>
    <components>
    [Cancel][Continue]

The user can click **Select All** or **Clear All** to mass select or deselect components from the list. If a component has a child-component under it, the child component cannot be registered without the top-level component. Deselect the top-level while the child component is selected throws an error::
  
    To register a subcomponent, you must also register the component above it.

The "Continue" button will be disabled in this state.

Once the user has (de)selected the components to be included in the registration, they can click the **Continue** button to proceed. Clicking **Continue** shows a confirmation modal for the list of components::
  
    Confirm
    The following projects and components will be registered:
    <components>
    [Cancel][Continue]

Clicking **Back** takes the user back to the component list view to select or deselect components. Clicking **Continue** opens the "Embargo" modal::

    Embargo
    * Registrations cannot be modified or deleted once completed.
    * The content and version history of Wiki and OSF Storage will be copied to the registration.
    Registration choice
    [Register]
  
If additional add-ons are connected to the project, the modal includes information about their registration behavior.

If keeping the registration public, the user can click the **Register** button to finalize the registration.

Selecting **Enter registration into embargo** opens another text field below the drop-down titled "Embargo End Date." Clicking
into the text field opens a calendar widget from which the user can choose the embargo's end date. On the selected end date, the registration will become public.

The embargo end date must be more than three days but cannot be greater than four years in the future. 

If the user chooses a date that is greater than four years, an inline red alert will appear below the "Embargo End Date" field::
  
    Embargo end date must be less than four years in the future.

The user cannot click "Continue" until they have chosen an appropriate date.
    
If the user chooses a date that is less than three days in the future, the calendar will close and the chosen date will appear in the field (even though this date is invalid). A red inline error will also appear below the "Embargo End Date" field::
  
    Embargo end date must be at least three days in the future.
    
The "Continue" button remains disabled until the user chooses an appropriate date.
    
When the user chooses a date within the correct date range, they can click **Register**, after which they are brought to the registration "Overview" page with a pending status::
  
    This project is currently pending registration, awaiting approval from project administrators. This registration will be final and enter the embargo period when all project administrators approve the registration or 48 hours pass, whichever comes first. The embargo will keep the registration private until the embargo period ends. [Cancel registration]
    
If the registration is public, the pending status reads::
  
    This is a pending registration of this project, awaiting approval from project administrators. This registration will be final when all project administrators approve the registration or 48 hours pass, whichever comes first.
    
The **Cancel registration** button appears only for admins. Clicking **Cancel registration** cancels the registration and directs the user to the project "Overview" page where a dismissable confirmation message appears at the top of the page::
  
  Your disapproval has been accepted and the registration has been cancelled.
  
If the canceled registration was under embargo, this helper text reads::
  
    Your disapproval has been accepted and the embargo has been cancelled.

Canceled registrations return to a draft state and appear in the "Draft registrations" tab of the "Registrations" page.

Registration confirmation emails
--------------------------------
**Purpose**: Admins can either approve or cancel the registration for up to 48 hours.

If the user opts to make their registration public, the user and all other admins on the project receive an email::

    Hello [username],

    [You or username] initiated a registration of your project [project name].
    To approve this registration, click the following link: URL
    To immediately cancel this registration, click the following link: URL
    Note: If you take no action within 48 hours, the registration will be automatically approved. This operation is irreversible.

    Sincerely yours,

    The OSF Robots

Clicking to approve the registration brings the user to the registration's "Overview" page, where a green dismissable alert appears
at the top of the page::

    Your registration approval has been accepted.

Clicking to disapprove the registration brings the user to the project's "Overview" page, where a green dismissable alert appears
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

The "Cancel Registration" button appears only for Project Administrators. If no action is taken by any administrator, the registration is approved. If one administrator cancels the registration by either clicking the cancel link in the email or by clicking the "Cancel Registration" button on the registration Overview page, the registration is cancelled and logged in the original project's Recent Activity widget. Until all administrators on a registration have clicked the approval link in the email, any registration administrator can click "Cancel Registration" on the registration's Overview (even if the administrator had formerly approved).

If a user clicks the link to *approve* an already cancelled registration, they are brought to a page that reads::

    Resource Deleted
    This resource has been deleted
    
If a user clicks the link to *cancel* an already approved registration, they are taken to the OSF project for that registration. 

Before a registration has been approved or cancelled, the registrations page shows a tag to the left of the registration
that reads "Registration Pending." Visiting that registration also shows the tag to the left of the components titles on the
overview page.

Prior to a registration's approval, the privacy settings from the registered project and its components apply. After approval,
the entirety of the registration is public.

If a registration is embargoed, all admins on the project, including the registrant, receive an email::

    Hello [username],

    [username or "You"] initiated an embargoed registration of [project name]. The proposed registration can be viewed here: [URL of registration].
    If approved, a registration will be created for the project and it will remain private until it is withdrawn, manually
    made public, or the embargo end date has passed on [date].
    To approve this embargo, click the following link: [URL]
    To cancel this embargo, click the following link: [URL]
    Note: Clicking the disapproval link will immediately cancel the pending embargo and the registration will
    remain in draft state. If you neither approve nor disapprove the embargo within 48 hours from
    midnight tonight (EDT) the registration will remain private and enter into an embargoed state.

    Sincerely yours,

    The OSF Robots

Non-admins also receive an email::

    Hello [username],

    We just wanted to let you know that [registrant username] has initiated an embargoed registration for the following pending registraiton: [URL].
    If approved, a registration will be created for the project, viewable here: [URL], and it will remain
    private until it is withdrawn, manually made public, or the embargo end date has passed on [date].

    Sincerely yours,

    The OSF Robots

After an embargo is enacted, a red non-dismissable alert is shown at the top of the page::

    This registration is currently embargoed. It will remain private until its embargo end date, [Day, Month date, year].

After an embargo ends, the registration and its components are made public. 

The cron job runs to end an embargo at midnight.

Registration failed
-------------------
Occasionally, a registration will fail. When a registration fails, the following modal will appear::

    Registration failed
    There was a problem completing your registration. Please try again later. If this should not have occurred and the issue persists, please report it to support@osf.io. 
    [Back to project]

OSF Preregistration
-------------------
The "Prereg" page is accessible by URL: https://osf.io/prereg/. The user must be logged in to preregister. The logged-out "prereg" page appears as follows::

  Improve your research with preregistration <https://cos.io/prereg/>. By writing out specific details such as data collection methods, analysis plans, and rules for data exclusion, you can make important decisions early on and have a clear record of these choices. This can help reduce biases that occur once the data are in front of you.

  Use OSF Registries <https://osf.io/registries> to discover previously registered work.
  
  [Preregister]

Clicking **Preregister** directs the user to the "Sign up" page: https://osf.io/register/.

The logged-in "prereg" page appears as follows::
  
  Improve your research with preregistration <https://cos.io/prereg/>. By writing out specific details such as data collection methods, analysis plans, and rules for data exclusion, you can make important decisions early on and have a clear record of these choices. This can help reduce biases that occur once the data are in front of you.

  Use OSF Registries <https://osf.io/registries> to discover previously registered work. 
  
  [Start a new preregistration]

If the user has a draft preregistration or existing projects, the options to "Continue working on an existing draft preregistration" and "Preregister a project you already have on OSF" are also displayed.

Clicking **Start a new preregistration** will opens a required title field::
    
    Please provide a title for your project:

Below the field is "Continue" button which remains disabled until a title is entered into the field. Clicking **Continue** creates an OSF project and directs the user to the project's "Registrations" page where they will need to click the **New registration** button and select the preregistration form they want to use from the "Register" modal.

Clicking **Continue working on an existing draft preregistration** opens a required title field where the user needs to enter an existing draft preregistration. Helper text above the field reads::
    
    Go to an existing preregistration:

Matching drafts will be auto-suggested in a drop-down menu from which the user can select the desired draft. Only titles of OSF Preregistration drafts will appear. If the user types in the title of an existing draft registration that does not use the OSF Preregistration form, the draft will not appear. Below the field is a "Preregister" button that remains disabled until a preregistration draft is selected. Clicking **Preregister** directs the user to the draft preregistration form.

Clicking **Preregister a project you already have on OSF** opens a required title field where the user needs to enter an existing project. Helper text above the field reads::
  
    Preregister an existing project:

Matching projects will be auto-suggested in a drop-down menu from which the user can select the desired project. Below the field is a "Preregister" button that remains disabled until a project is selected. If the user enters a title of a project that does not exist under their account, the button will remain disabled. Clicking **Preregister** directs the user to the project's "Registrations" page where they will need to click the **New registration** button and select the preregistration form they want to use from the "Register" modal.

Creating a registered report
----------------------------
**Purpose**: the registered report landing page and workflow provides users an easy way to create and share registered reports.

The "Registered Report" landing page is accessible at https://osf.io/rr. This page provides an onboarder to create registered reports following stage 1 peer review. Users must receive an in principle acceptance by a journal following stage 1 peer review in order to be eligible for the form. 

The page header is titled "Simple Registered Report Protocol Preregistration". Introductory text below the header reads::
  
  Registered Reports benefit science by improving rigor and reducing publication bias.

  When to use this form:

  Use this form after you have received “in principle acceptance” (IPA) by a journal following Stage 1 Peer Review, and before you have begun the study.

At the bottom of the page are options to start a registered report::
  
    [Create a Registered Report]

If the user is logged out when clicking this button, they will be prompted to sign in or create an account.

If the user has pre-existing OSF projects, a second button will be visible (the user must be logged in to see this option)::
  
    [Preregister an analysis plan for an OSF Project]
    
If the user previously started a registered report and left it in a draft state, a third button will be visible (the user must be logged in to see this option)::
  
    [Continue working on an existing draft of Registered Report]

Clicking **Create a Registered Report** opens a "Title" field below the button where the user must enter the title of their registered report before proceeding. Clicking **Create** takes the user to the form.

Clicking **Continue working on an existing draft of Registered Report** opens a search field below the button with helper text::
  
    Go to an existing registration:

Typing the name of the project that has a draft registered report into the field pulls up matching results. Typing existing project names that do not have draft registered reports associated with them will not show search results. After selecting the project and clicking **Continue**, the user is taken to their draft registered report.

Clicking **Preregister an analysis plan for an OSF project** opens a search field with helper text::
  
    Register existing project:

Typing the name of an existing project into the field pulls up matching results. After selecting the project and clicking **Register**, the user is taken to the form. The rest of the workflow follows regular registrations.

End embargo early
-----------------
If an embargoed registration is already approved, it may be made public by the project administrators. This action is irreversible.

On the registration page, a "Make Public" button appears. Clicking it generates the following modal::

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
-----------
**Purpose:** Withdrawals allow admins to make the contents of a registration private.

A registration that is not embargoed is public. Users cannot "undo" a registration or make its contents private, but admins
do have the option to withdraw the registration. Both public and embargoed registrations can be withdrawn. 

To withdraw a registration the admin visits the registration's Settings page.
Non-admins do not see the link to the Settings page.

Only the entirety of a registration (a registered project and its registered components) can be withdrawn—individual components cannot be withdrawn. If an admin visits a component's
Settings page to attempt to withdraw the registration of the individual component, a panel reads::

    Withdraw Registration
    Withdrawing children components of a registration is not allowed. Should you wish to withdraw this component, please
    withdraw its parent registration here.

Visiting the settings page of the parent registration shows a panel where the admin can withdraw the registration::

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

The user must then type a generated word into an additional text field to continue.

After withdrawing the registration, they are brought to the registration's Overview where a non-dismissable alert is visible at the top
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
date of the project's creation, date of the registration, date of the registration's withdrawal, DOI (if any), description (if any), and justification for withdrawal (if any). If no justification is given, a message appears in place of an explanation::
  
    No justification provided during withdrawal.

At the top of the page is a red, non-dismissable banner::

    This project is a withdrawn registration of this project; the content of the project has been taken down for the reason(s) stated below.

No other options or widgets are shown on the page.

If a user visits the registered project's registrations page, the withdrawn registration is still listed, with a link to the
withdrawal page. A red tag to the left of the link reads "Withdrawn."

Withdrawn registrations are shown in search results of the OSF. To the right of their name, in the result, is "(Withdrawn Registration)."

DOIs
-----
**Purpose:** DOIs can be issued to provide means of citation alternate to the OSF URL.

Public, meaning non-embargoed, registrations can be given DOIs. To do so, admins visit the registration's page and
click the "Create DOI" link below the "Date Created" field. Clicking opens a modal::

    Create identifiers
    Are you sure you want to create a DOI for this project? DOI identifiers are persistent and will always resolve to this page.
    [Cancel][Create]

Clicking "Create" turns the link to text that reads::

    Creating DOI. Please wait...

After several seconds, the text changes again to read::

    Identifiers: DOI [DOI identifier]

DOIs for projects and registations are minted through DataCite, and have the prefix: DOI 10.17605/OSF.IO/GUID.

Registering with Add-ons
------------------------
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

External Links
^^^^^^^^^^^^^^
The user can create external links to both registrations (public and embargoed) and projects/components alike. If an external link points to a project that is registered, the link will point to the project and not the registration. In other words, if the user has Project A and creates an external link to Project B, and registers project B, the external link will still point to Project B and not its registration.

To point a project or component to a registration, the user will need to enter the registration's URL into the "External Link" field when :ref:`configuring the external link <external link>`. If a user has access to an embargoed registration, the user can still create an external link that directs to it.


Adding institutional affiliations to registrations
--------------------------------------------------
**Purpose**: To allow registrations to have affiliations and/or to have different affiliations from the corresponding project. 

Only read+write and admins can add and remove registration affiliations. Read+write can only add/remove affiliations with which they are affiliated.
 
By default, registrations inherit the corresponding project's affiliations. If the project is not affiliated, the registration is also not affiliated by default.

To add an affiliation to a registration, the user clicks the **Settings** tab in the registration's navigation bar. 

On the "Settings" page there is a "Project Affiliation / Branding" button in the left side bar menu below the "Withdraw" option. 

Below the "Withdraw Registration" section of the "Settings" page is the "Project Affiliation / Branding" section with the following language::
  
  Projects can be affiliated with institutions that have created OSF for Institutions accounts. This allows:
  institutional logos to be displayed on public projects
  public projects to be discoverable on specific institutional landing pages
  single sign-on to the OSF with institutional credentials
  FAQ [links to help.osf.io]

Below this text block are a list of institutions with which the admin or read+write user are affiliated. To the right of the institution is a greed "Add" button. Clicking **Add** adds the institution as an affiliation to the registration. The green "Add" button turns into a red "Remove" button upon click. Clicking the red "Remove" button removes the affiliation, and the button turns back into the green "Add" button.
  
The institutional logo will appear in the top left of the registration "Overview" page.
