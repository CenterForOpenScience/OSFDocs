**Purpose:** A user’s account settings allow them to configure their login and password information, as well as close out
their OSF account.

Account Settings can be accessed by clicking on the gear button on the top right hand of the navigation bar when logged in.
In the left hand navigation that appears, the user clicks on “Account Settings” to find the appropriate page.

Merging Accounts (Connected Emails)
--------------------
**Purpose:** Account merging allows users to consolidate multiple OSF accounts into one and allows the user to login using multiple emails.

Primary and Alternate Emails
^^^^^^^^^^^^
**Purpose:** Primary emails are the emails to which all correspondence from the OSF will be sent. When merging accounts,
their :doc:`profile information <../profiles/profiles_index>` is kept while the alternate accounts’ is lost.

The email that the user signs up for the OSF with is their primary email. If the user merges an account, the primary email
is whichever was used to log in at the time that the merge was initiated.

An alternate email is another email or existing account that is added to the primary account.

To change a primary email, the user visits Account Settings. An alternate email must exist already—otherwise they must add
an alternate email. The user can click “make primary” next to the alternate email they wish to promote to their primary
email. A green, dismissable growlbox alert appears at the top of the page that reads::

    Made Primary
    [New primary email]

The newly promoted email is then listed under “Primary Email” and the old primary email is moved under “Alternate Emails.”

The user receives an email at their *previous* primary email that reads::

    Hello [User Name],
    I just wanted to let you know, the primary email address for your OSF account has been changed to [New Primary Email].
    If you did not request this action, let us know at contact@cos.io.
    Sincerely yours,
    The OSF Robot

Adding an Alternate Email
^^^^^^^^^^^^^^
**Purpose:** Adding an alternate email initiates the merge process.

Users can merge their accounts by logging into the account they wish to make primary and visiting their Account Settings.
Under “Connected Accounts,” and then "Unconfirmed emails," the user sees the message::

    To merge an existing account with this one or log in with multiple email addresses, add an alternate email address below.

Following this message is an "i" icon which, when a user mouses over, displays a toolip::
    
    Merging accounts will move all projects and components associated with two emails into one account. All projects and components will be displayed under the email address listed as primary. 

Here the user enters the login email for the account they wish to merge into (alternate) the primary account under “Unconfirmed Emails” and clicks “Add Email” or hits the return key.

Users cannot add the primary email as an alternate email; attempting to do so produces an inline error, below the “Add Email” button::

    Duplicate Email

Clicking “Add Email” before entering text into the address field produces a popover on the field that reads::

    ! Please fill out this field.

If the user enters text without an @ symbol, a popover on the field reads::

    ! Please include an '@' in the email address. [Entered text] is missing an '@'.

If the user enters an email address with an '@' symbol but no subsequent text, a popover on the field reads::

    ! Please enter a part following '@'. [Entered text] is incomplete.

If the user enters an email address with characters preceding and following an @ symbol, but it is not a valid email address (e.g. includes
no ".com"), after submitting their entry a red dismissable error message appears in the top right corner of the page::

    Error
    Invalid Email

If the user submits multiple such invalid email addresses, another identical message appears above the last alert.

After successfully adding an email, it is listed below “Unconfirmed Emails” and above the email address field. A modal appears::

    Confirmation email sent
    [Secondary Email] added to your account. You will receive a confirmation email at [Secondary Email]. Please log out of this account and check your email to confirm this action. 

An email is sent to the alternate email::

    Hello [Primary Account Username],
    This email is to notify you that [Primary Account Email] has an initiated an account merge with your account on the Open
    Science Framework (OSF). This merge will move all of the projects and components associated with [Alternate Email]
    and with [Primary Account Email] into one account. All projects and components will be displayed under [Primary Account Email].
    Both [Primary Account Email] and [Alternate Email] can be used to log into the account. However, [Alternate Email]
    will no longer show up in user search.
    This action is irreversible. To confirm this account merge, click this link: URL.
    If you do not wish to merge these accounts, no action is required on your part. If you have any questions about this
    email, please direct them to support@osf.io.

Clicking on the provided link sends the user to the OSF, logged in as whichever user last was logged in on that computer. The page reads::

    Confirmation Required: Merge Accounts
    This email is confirmed to another account. Would you like to merge [alternate email] with the account [primary email]?
    [Confirm Merge]

Clicking “Confirm Merge” sends the user to their “Account Settings” page where the email is listed as an alternate email.

Alternate accounts cannot be merged into the primary account if they have add-ons connected to a project. The Mendeley and
Zotero add-ons are exceptions to this rule, however. If a secondary account has a project with an add-on connected to it
or an add-on token associated with the account, clicking “Confirm Merge” brings the user to a page that reads::

    Cannot Merge Accounts
    Accounts cannot be merged due to a possible conflict with add-ons. Please deactivate any add-ons authorized on the account
    to be merged and try again.

If, when adding an email/account, the user enters an unregistered email into the field, the growlbox alert still shows and
the unregistered email is still listed as an alternate email. The user receives a confirmation email at that unregistered email::

    Hello [Primary Account Username],
    Please confirm your email address by visiting this link:
    URL
    From the Open Science Framework Robot

Clicking the link in the email sends them to their “Account Settings” page where the email is listed as an alternate email.

After adding alternate emails, the user can login to their OSF account with the primary or alternate emails.

The primary account can resend the confirmation email by clicking “resend confirmation” next to the unconfirmed secondary
email. The email is resent but the URL to follow changes. If the user follows the link from the first confirmation email
they were sent, they are sent to a page that reads::

    Invalid Token
    This confirmation link is invalid. Please log in to continue.

If the user makes changes to their alternate account’s projects or profile after the primary account requests the merge,
but prior to the confirmation, those changes are reflected in the merged projects.

If the user merges an account that had an alternate email of its own, both emails are made alternate in the new primary account.

Removing Emails
^^^^^^^^^^
**Purpose:** Unconfirmed and alternate emails can be removed to reduce the number of login emails available.

A primary email cannot be removed. Alternate or unconfirmed emails can be removed by clicking the ‘x’ to the right of the
email address under “Connected Emails” on the Account Settings page. If the user remove an alternate email, a modal appears
asking them to confirm the removal::

    Remove Email?
    Are you sure that you want to remove [unconfirmed email] from your email list?
    [cancel][Remove]

Cancelling closes the modal and produces no change. Clicking “Remove” removes the email from the “Unconfirmed Emails” list.
A green, dismissable growlbox alert appears at the top of the page::

    Email Removed
    [removed email address]

When an alternate email is removed, both the primary and alternate emails receive an email. The primary reads:

.. todo:: add email content here when bug is fixed.

The email sent to the removed alternate reads::

    Hello [User Name],
    I just wanted to let you know, the email address [alternate email] has been removed from your account. For security
    purposes, a copy of this message has also been sent to you account's primary email address ([primary email]).
    If you did not request this action, let us know at contact@cos.io.
    Sincerely yours,
    The OSF Robot

After removing an alternate email, no project or profile content changes.

If the user removes an unconfirmed email, a modal appears asking them to confirm the removal::

    Remove Email?
    Are you sure that you want to remove [unconfirmed email] from your email list?
    [cancel][Remove]

Cancelling closes the modal and produces no change. Clicking “Remove” removes the email from the “Unconfirmed Emails” list.
A green, dismissable growlbox alert appears at the top of the page::

    Email Removed
    [removed email address]

If the user follows the emailed confirmation link after an unconfirmed email was removed (i.e. the addition was cancelled),
they are brought to an error page that reads::

    Invalid Token
    This confirmation link is invalid. Please log in to continue.

Effects of a Merge
^^^^^^^^^^^^^^
**Purpose:** An account merge should condense OSF content into one account, but remove old user information.

Any projects that were associated with one of the alternate emails are added to :ref:`Project Organizer <organizer>`. If
one of the alternate accounts had collections in the Project Organizer, those are not added to the merged account. The
primary account’s :doc:`User Profile <../profiles/profiles_index>` information is saved while the alternate’s are lost.
Logs from before the merge will show the old user name—if it was different—but contributor lists will show the primary account’s name.

If the user had a different user name for an account that was made alternate, searching the OSF for that old username does
not return the old profile. Similar names may produce relevant results, however.

.. todo:: What if you have different permissions for two accounts on one project?

Changing Passwords
-------------

**Purpose:** Passwords can be changed at the user’s request to increase security, make it more memorable, or gain access to the account.

Changing a Password Via Account Settings
^^^^^^^^^^^^
**Purpose:** A user’s account settings can be used to change their password for any reason.

To change a password while logged into the OSF, the user visits their Account Settings. Under “Change Password” there are
three fields: “Old password,” “New password,” and “Confirm new password.” The user completes each field and clicks “Update
password” or presses the return key to confirm the change. The page refreshes and the relevant alert is shown; all fields are empty.

Password test is obfuscated so that the characters appear as dots after the user types them.

If the user does not enter any information into any of the three fields but submits the form, a popover appears under the
“Old password” field that reads::

    ! Please fill out this field

The password is not reset.

If the user enters an incorrect old password but submits the form, the page refreshes and a yellow, dismissable alert
appears at the top of the page::

    Old password is invalid

The password is not reset.

If the user enters a new password and the confirmation password does not match, the page refreshes and a yellow, dismissable
alert appears at the top of the page::

    Password does not match the confirmation.

The password is not reset.

If the user enters the old password as the new password, the page refreshes and a yellow, dismissable alert appears at the top of the page::

    Password cannot be the same.

The password is not reset.

If the new password is less than six characters, the page refreshes and a yellow, dismissable alert appears at the top of the page::

    Password should be at least six characters.

The password is not reset.

If the new password is more than 256 characters, the page refreshes and a yellow, dismissable alert appears at the top of the page::

    Password should not be longer than 256 characters.

The password is not reset.

If more than one of these errors are relevant, they show on separate lines within the same alert.

If the user enters the old password correctly and confirms a new password, the page refreshes and a green dismissable alert
appears at the top of the page::

    Password updated successfully

No email is sent to confirm the change.

The user is able to copy and paste into any of the three fields.

Resetting a Forgotten Password
^^^^^^^^^^^^^^
**Purpose:** If a user forgets their password and cannot log in to their OSF account, their password can be reset.

There is no limit to the number of times a user can reset their password.

When attempting to :ref:`log in <login>` from the :ref:`navigation bar <navigation-bar>` or the login page, users
can click on the “Forgot Password?” link. This link directs user to https://osf.io/forgotpassword/. The page is titled
“Password Reset Request” and there is a field for the user to enter their email address into. A “Reset Password” button
allows the user to submit the form. A link that reads “Back to OSF” links the user to the OSF homepage.

If a user tries to reset a password for an unregistered email, a yellow dismissable alert is shown on the page. The user is told::

    An email with instructions on how to reset the password for the account associated with [email] has been sent. If you do
    not receive an email and believe you should have please contact OSF Support.

No email is sent.

If the user tries to reset a password for a deactivated email, a yellow dismissable alert is shown on the page. The user is told::

    An email with instructions on how to reset the password for the account associated with [email] has been sent. If you do
    not receive an email and believe you should have please contact OSF Support.

The user receives an email. They are brought to the reset page. Submitting a new password brings them to a page that says in red::

    This account has been disabled. Please contact support@osf.io to regain access.

If a user tries to reset a password for a registered email, a yellow dismissable alert is shown on the page. The user is told::

    An email with instructions on how to reset the password for the account associated with [email] has been sent. If you do
    not receive an email and believe you should have please contact OSF Support.

The page refreshes and shows a sign in form that has a field for the user’s email address and password, as well as the same
“Forgot Your Password?” link. The user receives an email that reads::

    Follow this link to reset your password
    URL

The link leads the user to a page on the OSF titled “Reset Password.” The user is given two fields to enter their desired
password and to verify that password. A “Reset Password” button allows them to submit the form.

Clicking “Reset Password” without entering anything into either field refreshes the page; a yellow, dismissable alert
appears at the top of the page. It reads::

    Password is required

If the user only fills in the first field but submits the form, a yellow dismissable alert appears at the top of the page. It reads::

    Passwords must match

If the user only fills in the second field but submits the form, two yellow dismissable alerts appear at the top of the page. They read::

    Passwords must match

and ::

    Password is required

If the user enters the old password as the new password, the form submits successfully and the user is brought to their Account Settings page.

If the user enters a new password and confirms it, on submission they are brought to their Account Settings page.

If the user follows the link after having already reset the password, they are brought to a page that reads::

    Invalid url.
    The verification key in the URL is invalid or has expired.

If the user enters their email to reset their password, but does not follow the confirmation link, their password remains the same.

Security Settings
------------
**Purpose:** Security settings are available to allow the user to configure how much protection they have on their OSF account and data.

Security Settings are found under Account Settings.

Enabling Two-factor Authentication
^^^^^^^^
**Purpose:** Two-factor Authentication allows the user to add an additional step to the login process—making it more secure.

To enable Two-factor Authentication, the user visits their Security Settings on their Account Settings page. A description
of two-factor authentication is provided below the title. The user must click the link that reads “Enable Two-Factor
Authentication.” This opens a modal that reads::

    Enable Two-factor Authentication
    Enabling two-factor authentication will not immediately activate this feature for your account. You will need to follow
    the steps that appear below to complete the activation of two-factor authentication for your account.
    [Cancel][Enable]

Clicking “Enable” closes the modal. The “Enable Two-Factor Authentication” link has turned to a red link that reads “Disable
Two-Factor Authentication.” Instructions appear under the Two-Factor Authentication title. Below the verification code field,
a green inline alert reads::

    Successfully enabled two-factor authentication.

The message disappears after a few seconds.

The user must then user their authenticator app on their phone or mobile device to scan the provided QR code or enter the
secret key, written and highlighted in red above the QR code.

The user must then enter their verification code—if they do not, Two-Factor Authentication will not be fully enabled.

The user enters their verification code, provided via their phone, into the field labeled “Enter your verification code:”
and presses “Submit” or hits the return key.

If the verification code that is entered is incorrect, an inline red alert appears below the field that reads::

    Verification failed. Please enter your verification code again.

The message disappears after a few seconds. The incorrect code is still visible in the field.

If the verification code is correct, the page is refreshed and the instructions are removed—only the option to disable
Two-Factor Authentication is still visible.

If the user disables Two-factor Authentication but then re-enables it, they must set up a new authenticator on their phone
(i.e. they must rescan the QR code or re-enter the secret key into their phone). If they do not do so, the verification
code will not be correct.

Disabling Two-Factor Authentication
^^^^^^^^^^^^^^^
**Purpose:** Disabling Two-Factor Authentication allows the user to remove the second step of the login process that they
had previously enabled.

To disable Two-Factor Authentication, the user must visit their Security Settings. Next to the title for “Two-factor
Authentication” is a red link that reads “Disable Two-Factor Authentication.” Clicking this link pulls up a modal that reads::

    Disable Two-factor Authentication
    Are you sure you want to disable two-factor authentication?
    [Cancel][Disable]

Clicking “Disable” turns the red disable link into a blue link that reads “Enable Two-Factor Authentication.” A description
of two-factor authentication is provided below the title.

After disabling Two-Factor Authentication, the user can login without the extra verification step.

Export Account Data
--------------
**Purpose:** Some users may wish to leave the OSF or to have an additional copy of their OSF content; in these events,
exporting account data allows the user to get a copy of the contents of their entire OSF account.

To export a user’s account data, the user must visit their Account Settings and scroll to “Export Account Data.” A
description of the service is above a button titled “Request Export.”

Clicking “Request Export” brings up a modal that reads::

    Request account export?
    Are you sure you want to request account export?
    [Cancel][Request]

After clicking “Request,” a green dismissible growlbox alert appears at the top of the page that reads::

    Success
    An OSF administrator will contact you shortly to confirm your export request.

The request is sent to support@osf.io and administrators contact the user via email.

The “Request Export” button becomes disabled, but is re-enabled on refresh.

Deactivating an Account
-------------
**Purpose:** Users should be able to make an OSF account and ostensibly remove the desired content from the OSF.

Users can deactivate their account by visiting their Account Settings and scrolling to “Request Deactivation.” A yellow
warning within the “Deactivate Account” section reads::

    Warning: This action is irreversible.

Clicking the “Request Deactivation” button displays a modal asking user to confirm they want to request deactivation::

    Request account deactivation?
    Are you sure you want to request account deactivation? An OSF administrator will review your request. If accepted,
    you will NOT be able to reactivate your account.
    [Cancel][Request]

Clicking the “Request” button displays green, dismissible growlbox notification that reads::

    Success
    An OSF administrator will contact you shortly to confirm your deactivation request.

An email is sent to support@osf.io listing OSF user’s GUID and primary email address. The “Request Deactivation” button
is disabled. On refresh, a message appears::

    Your account is currently pending deactivation. 

This message persists until the account is deactivated.

When a request is sent, a team evaluates the situation before communicating with user.

.. todo:: Elaborate on the following:

    * If a user has no projects: Email is sent to user, asking to confirm deactivation.

    * User has only private projects, and user is the only contributor on those projects: Email is sent to user indicating
    that we will delete the projects upon confirmation of deactivation request. User is invited to delete these projects
    prior to confirming deactivation request, if user wishes.

    * User has only private projects, and projects have other contributors: Team checks if user is sole admin on the projects.
    If not, then communicate to user that s/he will be turned to unregistered user on those projects (name will appear as
    contributor, but not linked to anything else). User can remove him/herself from projects before deactivation if s/he wishes.

    * User has private and public projects with no other contributors

    * User has private and public projects with other contributors

    * User’s name is still listed? Can they click it to reclaim it?