Sign Up
*********

**Purpose:** The sign-up form creates an OSF account.

The sign-up form can be accessed only while logged out, from the OSF homepage (osf.io). This form requests the user’s full name, contact email, confirmation of their contact email, and a password. After successfully submitting, the user cannot click into any of the fields.

If the user does not complete a field, but clicks into a subsequent field or returns to a previous field or submits the form, an alert below the field(s) reads::

    This field is required.

If the user enters a name that has fewer than three characters, but clicks into a subsequent field or submits the form, an alert written in red below the name field reads::

    Please enter at least 3 characters.

If the user enters no email address, but clicks into another field or submits the form, an alert below the field reads::

    This field is required.

If the user does not enter a complete email address, but clicks into another field, an alert written in red below the email field reads::

    Please enter a proper email address.

If the user enters two different email addresses and clicks into another field, an alert written in red below the field reads::

    Emails must match.

If the user does not enter a password that has at least 6 characters, but clicks into another field, an alert written in red below the email field reads::

    Please enter at least 6 characters.

If the user enters a password that is longer than 256 characters, but submits the form, an alert written in red below the email field reads::

    Please enter at least 6 characters.

Clicking “Sign up free” while any error alert is still showing produces no result.


If the user tries to sign-up with an unregistered email, an inline success alert is shown on the page. The user is told::

    Registration successful. Please check [email] to confirm your email address.


If the user tries to sign-up with a registered but unconfirmed email, an inline success alert is shown on the page. The user is told::

    Registration successful. Please check [email] to confirm your email address.

The user receives an email::

    Hello [User Name],
    Please confirm your email address by visiting this link:
    URL
    From the Open Science Framework Robot

If the user tries to sign-up with an email that had been listed as an" :doc:`alternate </account_settings>` but that was removed, an inline success alert is shown on the page. The user is told::

    Registration successful. Please check [email] to confirm your email address.

The user receives an email::

    Hello [User Name],
    Please confirm your email address by visiting this link:
    URL
    From the Open Science Framework Robot

If the user tries to sign-up with a registered email, an inline red alert is shown on the page. The user is told::

    The email [email] has already been registered

No email is sent.

If the user tries to sign-up with a :doc:`deactivated </account_settings>` account's email, an inline red alert is shown on the page. The user is told::

    The email [email] has already been registered

No email is sent.

Confirming an Unregistered User Account
---------------

**Purpose:** Users can be added as contributors to an OSF :doc:`project <../projects/project_index>` without having an account. In this case can claim an account so that they may access the material.


Claiming an Account Via Email
^^^^^^^^^^^^^^^^
**Purpose:** Claiming an account via email allows a user who has been added as a contributor to a project to create an account following their addition.

If a user is added as a contributor to a project, but does not have an OSF account, they will receive an email in their inbox instructing them that they can set a password for their account::

    Hello [Name of account being claimed],
    You have been added by  [User who added unclaimed account as contributor] as a contributor to the project "[Project Name]" on the Open Science Framework. To set a password for your account, visit:
    URL
    Once you have set a password, you will be able to make contributions to [Project Name].
    Sincerely,
    The OSF Team
    If you are not [Name of account being claimed] or you are erroneously being associated with [Project Name] then email contact@osf.io with the subject line "Claiming Error" to report the problem.

If the user has confirmed their account and is signed into the OSF, but follows the email’s link again, they are brought to a page that informs them they are already a contributor.

If the user has confirmed their account and is not signed into the OSF, but follows the email’s link again, they are brought to a page that informs them that the account has already been claimed.

.. todo:: what if they do it right?

Claiming an Account Via the OSF
^^^^^^^^^^
**Purpose:** Claiming an account via the OSF allows a person who does not have an OSF account to identify themselves as a contributor on a project.

If a user finds their name listed on an OSF project but does not have an OSF account, they can claim their account. To do so, the user clicks on their name in contributor list. This name is not linked to a :doc:`public profile <../profiles/profiles_index>`. Hovering over their name shows a tooltip that says “Is this you?  Click to claim.” After clicking, a popover appears. The popover is titled “Claim account” and a blank text field instructs the user to enter their email. The user enters their email into the field and clicks the check mark to the right. Alternatively, the user can click the ‘x’ to the right of the check mark to cancel.

After submitting, a dismissable success growl-box alert appears in the upper right corner of the page. It reads “Email will arrive shortly. Please check [email].” An email is sent automatically to the entered address. The email does not allow them to sign into the account, but instead informs them that their request to claim the account has been received::

    Hello [Name of account being claimed],
    We received your request to claim an OSF account and become a contributor for "[Project name]".
    To confirm your identity, has been sent an email to forward to you with your confirmation link.
    This link will allow you to complete your registration.
    Thank you for your patience.
    Sincerely,
    The OSF Team

The user who added the unclaimed account as a contributor is also sent an email. This email asks the user to forward the message to the correct person::

    Hello [User who added unclaimed account as contributor],
    You recently added [Name of account being claimed] to "[Project Name]". [Name of account being claimed] wants to claim their account, but the email address they provided is different from the one you provided.  To maintain security of your project, we are sending the account confirmation to you first.
    IMPORTANT: To ensure that the correct person is added to your project please forward the message below to [Name of account being claimed].
    After [Name of account being claimed] confirms their account, they will be able to contribute to the project.
    ----------------------
    Hello [Name of account being claimed],
    You have been added by  [User who added unclaimed account as contributor] as a contributor to the project "[Project Name]" on the Open Science Framework. To set a password for your account, visit:
    URL
    Once you have set a password, you will be able to make contributions to [Project Name].
    Sincerely,
    The OSF Team

 After being forwarded the email, the user claiming the account is sent to a “Set Password” page. This page asks the user to “set a password to claim your account.” The email they are registering with is shown, but not editable. The user is asked to create a password and confirm it. There is a note that reads::

    If you are not [User name], or if you were erroneously added as a contributor to the project described in the email invitation, please email contact@osf.io.

The user can save their input and is then brought to their :doc:`profile information <profiles>` page.

Login
------------

**Purpose:** The login form allows a user to access their existing OSF account.

When signed out, users can login by clicking the “sign in” button at the top right of the page in the :doc:`navigation bar <../navigation/navigation>`. Clicking this button opens a dropdown menu with a field for the login email and password. Below the submit (reads “login”) button, is a link that reads “Forgot Password?”

If the user tries to login via the navigation bar, but enters an unregistered email or an incorrect password, they are brought to the login page. There, below the password field, an inline red alert reads::

    The email or password you entered is incorrect.

If a logged out user tries to access a :doc:`private <../projects/privacy>` OSF project, they are brought to the login page (accounts.osf.io/login).

The login page asks for their login email and password. A “Forgot Password?” link is available, as well as a link that reads “Back to OSF” that sends the user to the OSF homepage. A check box that is labeled “Remember me” allows the user to save their form input so that it appears the next time they visit this page.

If the user tries to log in—on the login page—with a registered (primary or alternate) email and the right password, they are brought to their dashboard. No alert is shown.

If the user tries to log in—on the login page—with a registered (primary or alternate) email with the wrong password, an inline red alert is shown on the page. The user is told::

    The email or password you entered is incorrect.

No email is sent.

If the user tries to log in—on the login page—with an unregistered email, an inline red alert is shown on the page. The user is told::

    The email or password you entered is incorrect.

No email is sent.

If the user tries to log in—on the login page—with a deactivated email, they are brought to a page that says in red::

    This account has been disabled. Please contact support@osf.io to regain access.

No email is sent.

If the user tries to log in—on the login page—with an alternate email that has been removed, an inline red alert is shown on the page. The user is told::

    The email or password you entered is incorrect.

No email is sent.

If the user tries to log in—on the login page—with a deactivated email with the wrong password, an inline red alert is shown on the page. The user is told::

    The email or password you entered is incorrect.

No email is sent.

Logging in with Two-factor Authentication
^^^^^^^^^^^^^^^

**Purpose:** Two-factor authentication provides added security to the user. It requires one additional step to ensure that the user logging in is, in fact, the account holder.

To log in with two-factor authentication enabled, the user enters their email and password into the empty fields on the login screen or from the navigation bar. After submitting, the user is asked for a two-factor authentication passcode. The passcode is accessible via the authenticator (likely `Google Authenticator <https://support.google.com/accounts/answer/1066447?hl=en>`_) app on their mobile device. Entering the passcode and clicking “Verify” or pressing the return key brings the user to their dashboard.

If the user submits a blank form, a red inline error is shown below the empty passcode field::

    Passcode is a required field.

If the passcode the user enters is incorrect, a red inline error is shown below the empty passcode field::

    The passcode you entered is incorrect.
