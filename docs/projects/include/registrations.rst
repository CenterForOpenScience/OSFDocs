.. _registrations:

Registrations
*************

**Purpose:** Registrations can be created to preserve the state of a project at a given moment in time.

Registrations create a read-only copy of a project. Admins can create a registration of a project, and all sub-projects and components
to which they also have admin rights by visiting the registrations page via their project's grey navigation bar.

On the registrations page, all pending, retracted, and completed registrations are listed. Each registration lists its project name,
registration date and time, contributors, and contributions, in the same format as provided for components on the
:ref:`Project Overview <component-format>`.

When no registrations have been made, non-contributors see text explaining this::

    There have been no completed registrations of this project. Only project administrators can initiate registrations. For a list of the most viewed and most recent public registrations on the Open Science Framework, click here.

The link provided sends the user to the :ref:`Public Activity page <public-activity>`.

Contributors who do not have permissions to register the project or component see the same message. Contributors who do have permissions to register the project or component see the message::

    There have been no completed registrations of this project. You can start a new registration by clicking the “New Registration” button, and you have the option of saving as a draft registration before submission. For a list of the most viewed and most recent public registrations on the Open Science Framework, click here.

If it is a sub-project or component, however, they see additional text::

    To register the entire project "[project name]" instead, click here.

The link provided sends the user to the parent project's registrations page.

Admins see an additional "New Registration" button.

Only contributors can comment or view comments on a registration.

Registration Overview
---------------------
**Purpose:** A registration's Overview shows the state of the project at the time of registration and links to the registration form.

The Registration Overview has all the widgets of a :ref:`Project Overview <overview>`, including a line that indicates when the registration was registered in the top left of the page where the rest of the metadata is::
    
    Date registered: year-month-day

The registration has a watermark in the background that says "read-only" repeatedly in order to distinguish it from a project. At the top of the page is a non-dismissable blue alert::

    This registration is a frozen, non-editable version of this project [links to the Project Overview page].

In the top right of the Registration Overview page is a blue button that reads "View Registration Form." Clicking this button takes the user to a page with a noneditable copy of the user's registration form and their responses.

If the registration does not have wiki content, the Wiki Widget is not included on the Registration Overview page, but it is included in the registration's navigation bar. Clicking the tab takes the user to the "Wiki Home" page with the message::
  
    Add important information, links, or images here to describe your project.

The Files widget does not allow for editing of file names, reorganization of files, or deletion of files, however. Only
downloads are permitted. Files are saved within their storage add-ons and OSF Storage, grouped into folders. The folders are
titled "Archive of [storage add-on]." These folders are collapsed by default.

Moreover, a registration's Recent Actity widget only shows the original OSF project's activity prior to the creation of the registration. In other words, the registration's Recent Activity widget is a frozen snapshot of the original OSF project's recent activity. Activity related to the registration itself, such as the user's creation of the registration, is only logged into the project's Recent Activity widget and not the registration's. 

Activity pertaining to the creation of the registration is logged into the original OSF project's Recent Activity widget:

* Intiated: the administrator who creates the registration is listed in the Recenty Activity widget as the oen who initiated the registration.
* Approved: the last administrator to approve the registration is the only admin listed in the Recent Activity widget who approved the registration.
* Canceled: the first adminstrator to cancel the registration is the only admin listed in the Recent Acvitity widget who canceled the registration.
* Registered: the last administrator to approve the registration is the only admin listed in the Recent Activity widget who registered the registration.

The blue Comments icon appears in the top right of the registration Overview page. The project's comments are not carried over to the registration. However, any comments made on the project prior to the registration's creation are logged into both the project and registrations's Recent Activity widget.

Admins and read+write contributors can add tags to the registration after it has been registered. The behavior is the same as described in the :ref:`Tags section <tags>`.
for the project "Overview" page.

Creating a Registration
-----------------------

**The following describes creating a registration from the project page. Subsequent documentation covers the Preregistration Challenge workflow**


Clicking "New Registration" on a project's registrations page opens an initiation modal::

  Registration creates a frozen version of the project. Your original project remains editable and will have the registration linked. Things to know about registration:

  * Registrations cannot be edited or deleted.
  * Withdrawing a registration removes its contents, but leaves behind basic metadata: title, contributors, date registered, date withdrawn, and justification (if provided).
  * Registrations can be public or embargoed for up to four years. Embargoed registrations will be made public automatically when the embargo expires.
  * Continue your registration by selecting a registration form:

  Prereg Challenge 
  Open-Ended Registration 
  Preregistration Template from AsPredicted.org
  Registered Report Protocol Preregistration 
  OSF-Standard Pre-Data Collection Registration 
  Replication Recipe (Brandt et al., 2013): Pre-Registration 
  Replication Recipe (Brandt et al., 2013): Post-Completion 
  Pre-Registration in Social Psychology (van 't Veer & Giner-Sorolla, 2016): Pre-Registration 
  [Cancel][Create draft]

The user must select a form and click **Create draft** to initiate a registration of their project. Each form follows a different template that is either one-page or multiple-pages long.At the bottom of each page, the user is presented with the date and time the draft registration was last saved, and two buttons: [Save as Draft][Preview for Submission]. 

Clicking "Save as Draft" saves the draft registration and returns the user to the project's Draft Registrations tab. 
Clicking "Preview for Submission" presents a preview of the registration, followed by two buttons: [Continue editing] and [Register]. 

Clicking "Continue editing" returns the user to the "Edit draft registration" page. 
Clicking "Register" brings up a modal::

    Before you continue...
    * Registrations cannot be modified or deleted once completed.
    * The content and version history of Wiki and OSF Storage will be copied to the registration.
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
-------------------
Occasionally, a registration will fail. When a registration fails, the following modal will appear::

    Registration failed
    There was a problem completing your registration. Please try again later. If this should not have occured and the issue persists, please report it to support@osf.io. 
    [Back to project]

Creating a registration in Preregistration Challenge workflow
-------------------------------------------------------------
The full "Prereg Challenge" landing page on the OSF is only accessible when logged in. If the user is logged out of the OSF or does not have an account, and they go to https://osf.io/prereg/, they will have access to a landing page that contains basic information about the Prereg Challenge and invites non-users to create accounts::

    Articles must be published by an approved journal <https://cos.io/our-services/prereg-more-information/> by December 31, 2018, to be eligible for a prize.
    Improve your research with preregistration. The process of creating a preregistration <https://cos.io/prereg/> is beneficial to both the scientific field and to you, the scientist. By writing out detailed data collection methods, analysis plans, and rules for excluding or missing data, you can make important decisions that affect your workflow earlier, without the biases that occur once the data are in front of you.
    [Preregister]

Clicking **Preregister** takes the non-user and logged-out user to the account registration page which shows the Prereg Challenge logo and the following message::
  
    Preregistration Challenge
    Please login to the Open Science Framework or create a free account to continue.


The full "Prereg Challenge" landing page appears as follows::
  
    Articles must be published by an approved journal <https://cos.io/our-services/prereg-more-information/> by December 31, 2018, to be eligible for a prize.
    Improve your research with preregistration.The process of creating a preregistration <https://cos.io/prereg/> is beneficial to both the scientific field and to you, the scientist. By writing out detailed data collection methods, analysis plans, and rules for excluding or missing data, you can make important decisions that affect your workflow earlier, without the biases that occur once the data are in front of you.

    Ready for the challenge? Please follow these steps:
      1. Specify all your study and analysis decisions prior to investigating your data
      2. Publish your study in an eligible journal [links to: https://cos.io/our-services/prereg-more-information/]
      3. Receive $1,000

The "Prereg Challenge" landing page provides the user the option to "Start a new preregistration." If the user already has a draft registration, there is also an option to "Continue working on an existing preregistration." If the user has project(s), an option to "Make a preregistration for a project you already have on the OSF" is also displayed. 

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

with a text form to type the preregistration title and a button to "Continue". Clicking continue will open a model containing terms and conditions for the Preregistration Challenge. Accepting the terms will land the user on the "Edit draft registration page" for the Prereg Challenge registration template. 

In each workflow, the user will be prompted to agree to the prereg challenge terms before continuing::
  
    Pregistration challenge
    Notice
    Below are some important items for those who choose to enter the Preregistration Challenge. If you do not agree to the terms you may still continue, use the form, and register your research study without entering the Challenge. Only Preregistrations that enter the challenge and undergo review are eligible for a $1,000 prize. We welcome questions and comments (learn more here or email us at prereg@cos.io).

    After submitting your research plan for review, it is not yet registered. Your research plan will become a static, time stamped preregistration after it passes review. Please do not begin your study until it is registered. You will hear back from the review team within 2 business days.
    The published article must also be reviewed before receiving the prize.
    Prizes will be awarded at predetermined dates to eligible entrants. If more eligible entrants exist than available prizes, entrants will be ranked based on the date of registration.
    Articles must be published in an eligible journal.
    Residents of countries on the U.S. State Department's list of embargoed countries may not participate in the Preregistration Challenge.
    Entering the Preregistration Challenge requires that you agree to all of its terms.
     [check box] I have read these terms. I understand that articles must be published by December 31, 2018, in order to be eligible for a prize.

Clicking **Continue** will take the user to a draft version of the preregistration form within their OSF project. At the bottom of each page, the user is provided with buttons, "Save as draft" or "Next page." On the last page, the "Next page" button is replaced by a "Submit for review" button. 

If a user saves their preregistration as a draft and has not opened the draft preregistration after 2 weeks time, the OSF sends trigger emails for users who have started, but not yet submitted a preregistration::
  
    Reminder: Your draft preregistration on the OSF is not yet finished
    
    Dear <user name>, 

    You have an unsubmitted preregistration on the Open Science Framework that could be eligible for a $1,000 prize as part of the Prereg Challenge. If you would like this to be considered for a prize, please complete your preregistration <links to prereg draft> from your project <project name> and submit it for review, available on the last page of the preregistration form. This review process is required for a prize and simply checks to make sure the preregistration includes a complete analysis plan. If you have questions about a particular field in the preregistration, you may review the FAQ on the website <links to https://cos.io/prereg/>, email us with a question <links to prereg@cos.io>, or use our free statistical consulting services <links to https://cos.io/our-services/training-services/>. Thank you for using the OSF! 

    Sincerely, 
    The team at the Center for Open Science

Users are only emailed once per draft. If the user starts another draft of the same project or another project, after 2 weeks of being unfinished, the user gets an email. A user should get no more than 3 emails in a 2 week period.

Clicking the "Submit for review" button opens a modal with a Notice of Consent for the Preregistration Challenge::
  
    Preregistration challenge
    Notice of Consent
    Articles must be published by an approved journal by December 31, 2018, to be eligible for a prize.

    Please read and agree to the terms before submitting your research plan to the Preregistration Challenge.

    After submitting your research plan for review, it is not yet registered. Your research plan will become a static, time stamped preregistration after it passes review. Please do not begin your study until it is registered. You will hear back from the review team within 2 business days.
    The published article must also be reviewed before receiving the prize.
    Prizes will be awarded at predetermined dates to eligible entrants. If more eligible entrants exist than available prizes, entrants will be ranked based on the date of registration.
    Articles must be published in an eligible journal.
    Residents of countries on the U.S. State Department's list of embargoed countries may not participate in the Preregistration Challenge.
    Entering the Preregistration Challenge requires that you agree to all of its terms.
      [check box] I agree. I understand that articles must be published by December 31, 2018, in order to be eligible for a prize.

The user must agree to the terms and click "Continue." Clicking "Cancel" returns the user to the registration preview page. Clicking "Continue" prompts the user to choose to either make the registration public immediately or choose an embargo (as in the normal workflow). After making this selection, the user lands on the "Registrations" page for the project and is presented with a dissmissable notice::

  Your submission has been received. You will be notified within two business days regarding the status of your submission. If you have questions you may contact us at prereg@cos.io. 

The preregistration appears in the "Draft registrations" tab with the label "Pending Review." There are buttons to [Preview] or [Delete] the registration. Clicking [Preview] opens the preview of the registration, with a button to go [Back] to the Registrations tab. Clicking [Delete] pops up a modal::

    Are you sure you want to delete the registration? [Cancel][Delete]

Accepted Preregistrations
-------------------------
**Purpose**: Accepted preregistrations will be eligible for the $1,000 prize.

If the reviewers of the preregistrations accept the preregistration, and all admins on the preregistration click the approval link in the confirmation email, the user receives the following email::
  
  Subject: Your research plan has been registered and accepted for the Preregistration Challenge

  Dear {user name},

  We are happy to let you know that your research plan has been verified for completeness and registered on the OSF at the following URL: <a href="${registration_url}">${registration_url}</a>.

  What happens now?
  Conduct your study: It's time to start your study and its analysis exactly as specified in your preregistration.
  Publish your study: The published study must appear online by December 31, 2018.
  Reminders: Any deviations from your preregistration (e.g. sample size, timing, analysis) must be documented and appear in the final publication. Any additional analyses must be noted separately from the registered, confirmatory, hypothesis testing analyses. Such new analyses must be described as hypothesis generating or exploratory tests. You must also refer to your preregistration in the publication by using its URL: <a href="${registration_url}">${registration_url}</a>. Publication must occur in an <a href="https://cos.io/preregjournals">eligible journal</a>.

  Submit your article for review: We will review your final, published article once you submit it on the OSF. We will verify that your study and its analyses were conducted as specified in your preregistration. In order to avoid any unintended oversights, please reach out to us (<a href="mailto:prereg@cos.io">prereg@cos.io</a>) and refer to our guidelines and FAQ on our <a href="https://cos.io/prereg">website</a> when writing up your results.

  Receive the prize! $1,000 rewards will be distributed to eligible entrants according to the schedule on our website.

  Thank you for entering the Preregistration Challenge. Feel free to submit another research plan at any time.

  Sincerely,

  The team at the Center for Open Science

  Center for Open Science210 Ridge McIntire Road, Suite 500, Charlottesville, VA 22903


Rejected Preregistrations
-------------------------
**Purpose**: If the research is non eligible for the Prereg Challenge, the user is notified with a chance to make changes and resubmit.
    
If the reviewers of the preregistration reject the preregistration and provide feedback, the user receieves the following eamil::
  
  Dear ${user.fullname},

  Thank you for submitting your research plan to the Preregistration Challenge. 

  Reviewers have made comments on your plan. We require that you address the comments found on ${draft_url} and resubmit. 

  Each submission must pass this review process in which the statistical methods of the proposed study and its analyses are checked for completeness and adherence to Preregistration Challenge eligibility requirements (https://cos.io/prereg). This review does not assess the substance of the research, or the validity of the research design or statistical methodology. This review has no impact on the independent editorial decisions of any journal.

  Prereg Challenge administrators and reviewers review the submitted study design and analysis descriptions, and determine whether all question fields are answered with enough detail to fully pre-specify the design and analysis plan, and follow the eligibility requirements. See https://osf.io/h4ga8/ to learn more about the guidelines that reviewers use when evaluating your submitted plans.

  Sincerely,

  The team at the Center for Open Science

  Center for Open Science

  210 Ridge McIntire Road, Suite 500, Charlottesville, VA 22903-5083

  Privacy Policy: https://github.com/CenterForOpenScience/cos.io/blob/master/PRIVACY_POLICY.md
  
The user can click the link in the email to be taken to their draft preregistration form. Alternatively, they can access their draft by navigating to their project and clicking the "Registrations" tab> "Draft Registrations." The draft is listed on the page in the following format::
  
  Prereg Challenge
  Initiated by: [user name]
  Started: [day month date year][hh:mm:ss] GMT -0x00 (XXX)
  
A rejected preregistration will have a message highlighted in yellow at the bottom of the listed draft that reads::
  
    Unseen Comments

At the bottom of the pages in the form that have feedback, there will be a "Comments" box where the reviewers have provided feedback::
  
  Comments
  (Comments are not included in your preregistration and are not made public)

In the "Comments" section is a text box with the reviewer's comments. The first text in the box reads::
  
    The Prereg Admin said...
    
Which is then followed by their commentary.


Creating a registered report
----------------------------
**Purpose**: the registered report landing page and workflow provides users an easy way to create and share registered reports.

The "Registered Report" landing page is accessible at https://osf.io/rr. This page gives uesrs an onboarder to create registered reports following stage 1 peer review. Users must receive an in principle acceptance by a journal following stage 1 peer review in order to be eligible for the form. 

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

Embargos
--------
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

Below the "Registration Choice" header is a drop-down menu from which the user decides to either::
    [Make registration public immediately]
    [Enter registration into embargo]

Registrations with No Embargo
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
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

Registrations with an Embargo
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
**Purpose:** Embargo periods allow the user to keep a registration private for a limited period of time.

Selecting "Enter registration into embargo" opens another text field below the dropdown titled "Embargo end date." Clicking
into the text field opens a calendar widget from which the user can choose the embargo's end date. On the selected end date,the registration will become public.

The embargo end date must be more than three days but cannot be greater than four years in the future. 

If the user chooses a date that is greater than four years, a growlbox will appear below the "Embargo End Date" field::
  
    Embargo end date must be less than four years in the future.

The user cannot click "Continue" until they have chosen an appopriate date.
    
If the user chooses a date that is less than three days in the future, the calendar will close and the chosen date will appear in the field (even though this date is invalid). A growlbox will also appear below the "Embargo End Date" field::
  
    Embargo end date must be at least three days in the future.
    
The user cannot click "Continue" until they have chosen an appopriate date.
    
When the user chooses a date within the correct date range, they can click "Continue"

After confirming the registration, the user is brought back to the registrations page for the registered project. A blue alert
is at the top of the page::

    Files are being copied to the newly created registration, and you will receive an email notification when the copying is finished.

If the registration was entered into an embargo period, a lock symbol will appear to the left of the registration's title, indicating that the project is embargoed. Before an admin approves the embargo, an additional tag reads "Pending Embargo."
These also appear to the left of component titles on the registration's overview. After the embargo is approved, the tag
reads "Embargoed" until the embargo period is concluded.

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

Visiting the embargoed registration before it is approved shows a non-dismissable alert at the top of the page::

    This project is currently pending registration, awaiting approval from project administrators. This registration will
    be final and enter the embargo period when all project administrators approve the registration or 48 hours pass,
    whichever comes first. The embargo will keep the registration private until the embargo period ends.
    [Cancel Registration]

The **Cancel Registration** button appears only for Project Administrators.

After an embargo is enacted, a red non-dismissable alert is shown at the top of the page::

    This registration is currently embargoed. It will remain private until its embargo end date, [Day, Month date, year].

After an embargo ends, the registration and its components are made public. 

The cron job runs to end an embargo at midnight.

End embargo early
-----------------
If an embargoed registration is already approved, it may be made public by the project administrators. Public components or projects cannot be made private. 

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

Below this text block are a list of institutions with which the admin or read+write user are affiliated. To the right of the institution is a greed "Add" button. Clicking **Add** adds the institution as an affiliation to the registration. The green "Add" button turns into a red "Remove" button upon click. Clicking the red "Remove" button removes the affiation, and the button turns back into the green "Add" button.
  
The institutioal logo will appear in the top left of the registration "Overview" page.
