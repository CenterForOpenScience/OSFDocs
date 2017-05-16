.. _add-ons:

Add-Ons
==========
**Purpose:** Add-ons can be used to connect a third party service to the OSF. This increases the amount of storage the user
can make use of via the OSF.

For information on linking an OSF account to an add-on, visit :ref:`User Level Add-on Settings <user-addon>`

Include linking to add-on, overview widget, files browser behavior, file detail page.


Dataverse: if they have multiple linked to their user profile then when the connect the account they can choose from a dropdown (if they don't have multiple connected...)


Amazon S3: https://github.com/CenterForOpenScience/osf.io/pull/3363
https://github.com/CenterForOpenScience/osf.io/pull/3812

Google Drive: https://github.com/CenterForOpenScience/osf.io/issues/3748

Mendeley: https://github.com/CenterForOpenScience/osf.io/pull/3900


Users with administrative and read+write privileges can connect and configure storage add-ons from their :ref:`Settings page <settings>`.
To do this from the main project page, users can click the “Settings” button in the grey navigation bar. For users
with read only privileges, the “Settings” button will be visible, but options to connect and configure add-ons will
not be available. Visitors to a project (i.e. those who are not contributors on a project) will not see the “Settings”
button and will not be able to connect and configure add-ons.


To configure any add-on, the first step is to visit the Settings page and check the corresponding box under "Select Add-ons."

.. _s3:

Configuring Amazon S3
**********
**Purpose:** Connecting to Amazon S3 allows users to create a two way connection between the OSF and Amazon S3.

Users who choose to connect their Amazon S3 account to the OSF can check appropriate box. They are presented with a
modal::

    Amazon S3 Add-on Terms
    Function | Status

    Permissions: Making an OSF project public or private is independent of making an S3 bucket public or private. The
    OSF does not alter the permissions of linked S3 buckets.
    View / download file versions: The S3 add-on supports file versions if versioning is enabled for your S3 buckets.
    Add / update files: Adding/updating files in the project via OSF will be reflected in Amazon S3.
    Delete files: Files deleted via OSF will be deleted in Amazon S3.
    Logs: The OSF keeps track of changes you make to your S3 buckets through the OSF, but not for changes made using S3 directly.
    Forking: Forking a project or component does not copy S3 authorization unless the user forking the project is the
    same user who authorized the S3 add-on in the source project being forked.
    Registering: S3 content will be registered, but version history will not be copied to the registration.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions.
    The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
    [Cancel][Confirm]

On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring Box.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button::

    Settings updated

If the user has not connected Amazon S3 to their profile before, the Amazon S3 panel will then show two text fields
labeled "Access Key" and "Secret Key." The user must enter the keys and click "Save."

If the entered keys are incorrect, red inline text appears below the "Save" button::

    Unable to list buckets. Listing buckets is required permission that can be changed via IAM

If one field is left blank, red inline text appears below the "Save button::

    All the fields above are required.

After entering correct information, green inline text appears::

    Successfully added S3 credentials.

If the user has connected to Amazon S3 previously, there are no text fields but there is a blue "Import Account from Profile"
link to the right of the section title. Clicking the link opens a modal::

    Import S3 credentials?
    Are you sure you want to authorize this project with your S3 credentials?
    [Cancel][Import]

Importing refreshes the page. Green inline success text is shown in the Amazon S3 section::

    Successfully imported S3 credentials.

Below the Amazon S3 title row is now bold text that reads "Current Folder: None." This is updated when the user selects
a folder. A blue button labeled "Change" is below the "Current Folder" text. Clicking this button expands and collapses
a dropdown below. An additional button to the right of "Change" is labeled "Create Bucket."

In the dropdown are all of the user's Amazon S3 buckets. After selecting one, the user must save their changes. Leaving the page without
saving produces no warning and will not enact the changes.

Amazon's rules for bucket naming are evolving. It is possible that a previously-created bucket will violate updated bucket naming conventions. As the US East (Northern VA) region for storage was the first location, the rules for bucket naming there are more lax than other storage locations. The laxer rules allow bucket names up to 255 characters long, consisting of uppercase letters, lowercase letters, digits, periods, hyphens, and underscores. If a user attempts to connect a bucket that violates this, they will receive an error message that the bucket must follow the stricter naming conventions (though this should not be possible). See section about creating buckets (below) about bucket naming conventions.

Alternative to selecting an existing repo, the user can create a new one by clicking "Create Repo." This opens a modal::

    Bucket Name [text field]
    Bucket Location [dropdown]
    [Cancel][Create]

If the user saves an empty name field, the modal is closed and red inline text below the dropdown reads::

    Bucket name cannot be empty

Bucket names must follow Amazon's guidelines (http://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html#bucketnamingrules): Bucket names should look like subdomains, one or more labels joined with periods. A label consists of lowercase letters, numbers, and hyphens. The first and last character of a label may not be a hyphen. The bucket name must be between 3 and 63 characters long. Any character besides those are invalid.    

The "Bucket Location" field allows the user to select the server location where they wish to store their data. "US
Standard" is selected by default.

If the user correctly creates a new bucket, it becomes the choice selected in the dropdown and green inline text appears below::

    Successfully created bucket "[bucket name]". You can now select it from the drop down list.

Clicking "Save" produces green inline text below the dropdown::

    Successfully linked S3 bucket "[bucket name]". Go to the Files page to view your content.

Clicking "Save" without making changes produces no effect.

To disconnect Amazon S3, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect S3 Account?
    Are you sure you want to remove this S3 account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the dropdown and connected repo information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile." Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.


.. _box:

Configuring Box
*******
**Purpose:** Connecting to Box allows users to create a two way connection between the OSF and Box.

Users who choose to connect their Box account to the OSF can check appropriate box. They are presented with a
modal::

    Box Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of Box privacy. The OSF does not alter the
    permissions of linked Box folders.
    View / download file versions: Box files and their versions can be viewed/downloaded via OSF.
    Add / update files: Adding/updating files in the project via OSF will be reflected in Box.
    Delete files: Files deleted via OSF will be deleted in Box.
    Logs: The OSF keeps track of changes you make to your Box content through the OSF, but not for changes made using
    Box directly.
    Forking: Forking a project or component does not copy Box authorization unless the user forking the project is the
    same user who authorized the Box add-on in the source project being forked.
    Registering: Box content will be registered, but version history will not be copied to the registration.


    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions.
    The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
    [Cancel][Confirm]

On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring Box.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button::

    Settings updated

If the user has not connected Box to their account previously, a row titled "Box" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, they will be navigated to a new window where they can confirm the
connection with Box before being taken back to the Settings page on the OSF.

If the user has connected Box to their account previously, the link in the Box row reads "Import Account from Profile."
Clicking opens a modal that reads::

    Import Box Account?
    Are you sure you want to link your Box with this project?
    [Cancel][Import]

Importing or connecting an account loads the users' Box information.

To the right of the the "Box" title is text that reads::

    Box authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads "Current Folder: None." This is updated when the user selects a folder. A blue button labeled
"Change" is below the "Current Folder" text. Clicking this button expands and collapses a table below.

The table has two columns—"Folders" and "Select." Under "Folders" is a list of all top level Box folders the user has.
Folders can be expanded and collapsed. Each folder has a corresponding radio button in the "Select" column. When the user
selects a folder, text appears at the bottom of the table::

    Connect [folder title]?

Two buttons, "Cancel" and "Save" appear below the table. Cancelling removes the two buttons and confirmatory text but the folder
is still selected.

Clicking "Save" updates the "Current Folder" text and green inline text appears below the table, replacing the buttons::

    Successfully linked "[folder title]". Go to the Files page to view your content.

To disconnect Box, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect Box Account?
    Are you sure you want to remove this Box account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the table and connected folder information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile." Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.

.. _dataverse:

Configuring Dataverse
************
**Purpose:** Connecting to Dataverse allows users to create a two way connection between the OSF and Dataverse.

Users who choose to connect their Dataverse account to the OSF can check appropriate box. They are presented with a
modal::

    Dataverse Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of making a Dataverse study public or private. The OSF allows you to release the latest draft version of a Dataverse dataset.
    View / download file versions: Files from the latest release of the selected Dataverse study can be viewed/downloaded. OSF users with write permissions can view/download draft files as well.
    Add / update files: Adding/updating files in the project via OSF will be reflected in Dataverse.
    Delete files: Files deleted via OSF will be deleted in Dataverse.
    Logs: The OSF keeps track of changes you make to your Dataverse studies through the OSF, but not for changes made using Dataverse directly.
    Forking: Forking a project or component does not copy Dataverse authorization unless the user forking the project is the same user who authorized the Dataverse add-on in the source project being forked.
    Registering: Dataverse content will be registered, but version history will not be copied to the registration.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions.
    The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.


On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring GitHub.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button::

    Settings updated

If the user has not connected Dataverse to their account previously, a row titled "Dataverse" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, a modal opens::

    Connect a Dataverse Account
    Dataverse repository: [dropdown]
    [Cancel][Save]

The dropdown instructs users to select a Dataverse to connect. The user can make a choice from the dropdown or select "Other."
If the user selects "Other" a text field appears below the dropdown requesting a URL to the Dataverse. After a Dataverse
is indicated, a text field appears on the right for the user to enter their API Token. A link above the text field sends the user
to Dataverse where a Token is provided. The user must copy this and paste it into the field on the OSF. If a user inputs a non-dataverse URL and clicks the "Get from Dataverse" link, the user will receive a 404 error. 

If the user inputs a non-dataverse URL, no API token, and clicks "save," he receives an error, "Please enter a Dataverse host and an API token."

If the user inputs an API token and no URL and clicks, "save," he receives an error, "Please enter a Dataverse host and an API token."

If the user inputs a non-dataverse ULR and characters that are not an API token, he receives an error, "Sorry, but there was a problem connecting to that instance of Dataverse. It is likely that the instance hasn't been upgraded to Dataverse 4.0. If you have any questions or believe this to be an error, please contact support@osf.io."

::todo: bad error handling was fixed for user settings page, but not for project settings page. put in bug ticket. 

If the user has connected Dataverse to their account previously, the link in the Dataverse row reads "Import Account from Profile."
Clicking this link opens a modal::

    Import Dataverse Access Token?
    Are you sure you want to authorize this project with your Dataverse access token?
    [Cancel][Import]

Importing or connecting an account loads the users' Dataverse information.

To the right of the the "Dataverse" title is text that reads::

    Dataverse authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads::

    Dataverse Repository: [connected Dataverse]

Below that is bold text that reads::
    Current Repo: None

Below this text are two dropdowns. The left dropdown ias labeled "Dataverse:" and the right "Dataset." The top choice from each
dropwdown is automatically selected.

In each dropdown are all of the user's Dataverses and Datasets belonging to the selected Dataverse. After selecting one,
the user must save their changes. Leaving the page without saving produces no warning and will not enact the changes.

Saving a change updates the "Current Dataset" field to read::

    Current Dataset: [Dataset] on [Dataverse]

Green inline text appears below the dropdowns after saving a change::

    Successfully linked dataset '[Dataset]'. Go to the Files page to view your content.

To disconnect Dataverse, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect Dataverse Account?
    Are you sure you want to remove this Dataverse account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the table and connected folder information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile." Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.

.. _dropbox:

Configuring Dropbox
************
**Purpose:** Connecting to Dropbox allows users to create a two way connection between the OSF and Dropbox.

Users who choose to connect their Dropbox account to the OSF can check appropriate box. They are presented with a
modal::

    Google Drive Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of Dropbox privacy. The OSF does not alter the permissions of linked Dropbox folders.
    View / download file versions: Dropbox files and their versions can be viewed/downloaded via OSF.
    Add / update files: Adding/updating files in the project via OSF will be reflected in Dropbox.
    Delete files: Files deleted via OSF will be deleted in Dropbox.
    Logs: OSF keeps track of changes you make to your Dropbox content through OSF, but not for changes made using Dropbox directly.
    Forking: Forking a project or component does not copy Dropbox authorization unless the user forking the project is the same user who authorized the Dropbox add-on in the source project being forked.
    Registering: Dropbox content will be registered, but version history will not be copied to the registration.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions. The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
    [Cancel][Confirm]

On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring Dropbox.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button:

    Settings updated

If the user has not connected Dropbox to their account previously, a row titled "Dropbox" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, they will be navigated to a new window where they can “Allow” the connecting
of Dropbox and the OSF. Upon clicking “Allow,” users are then taken back to the Settings page on the OSF.

If the user has connected Dropbox to their account previously, the link in the Dropbox row reads "Import Account from Profile."
Clicking opens a modal that reads::

    Import Dropbox Account?
    Are you sure you want to link your Dropbox account with this project?
    [Cancel][Import]

Importing or connecting an account loads the users' Dropbox information.

To the right of the the Dropbox title is text that reads::

    Dropbox authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads "Current Folder: None." This is updated when the user selects a folder. A blue button labeled
"Change" is below the "Current Folder" text. Clicking this button expands and collapses a table below.

The table has two columns—"Folders" and "Select." Under "Folders" is a list of all top level Dropbox folders the user has.
Folders can be expanded and collapsed. Each folder has a corresponding radio button in the "Select" column. When the user
selects a folder, text appears at the bottom of the table::

    Connect [folder title]?

Two buttons, "Cancel" and "Save" appear below the table. Cancelling removes the two buttons and confirmatory text but the folder
is still selected.

Clicking "Save" updates the "Current Folder" text and green inline text appears below the table, replacing the buttons::

    Successfully linked "[folder title]". Go to the Files page to view your content.

To disconnect Dropbox, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect Dropbox Account?
    Are you sure you want to remove this Dropbox account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the table and connected folder information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile."

If a Dropbox account is connected, only the user who connected the account can change the selected folder. Other Admins can
remove the add-on and connect another.  Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.

.. _figshare:

Configuring figshare
***********
**Purpose:** Connecting to figshare allows users to create a two way connection between the OSF and figshare.

Refer to this `Google Doc <https://docs.google.com/document/d/1T8c69at_0X2WKficbYEV0z7bfM3jNFoWkYtmNmZjVPg/edit#heading=h.f17owbri8qc3>`_ for information on the allowable figshare actions.

Users who choose to connect their figshare account to the OSF can check appropriate box. They are presented with a
modal::

    figshare Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of making figshare content public or private. The OSF does not alter the permissions of linked figshare content.
    View / download file versions: figshare content can be viewed and downloaded via OSF provided it is "published" on figshare.
    Add / update files: Files can be added but not updated.
    Delete files: figshare files cannot be deleted via OSF.
    Logs: OSF keeps track of changes you make to your figshare content through OSF, but not for changes made using figshare directly.
    Forking: Forking a project or component does not copy figshare authorization unless the user forking the project is the same user who authorized the figshare add-on in the source project being forked.
    Registering: figshare content will be registered, but version history will not be copied to the registration.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions. The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
    [Cancel][Confirm]

On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring figshare.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button:

    Settings updated

If the user has not connected figshare to their account previously, a row titled "figshare" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, they will be navigated to a new window where they can “Allow” the connecting
of figshare and the OSF. Upon clicking “Allow,” users are then taken back to the Settings page on the OSF.

If the user has connected figshare to their account previously, the link in the figshare row reads "Import Account from Profile."
Clicking opens a modal that reads::

    Import figshare Account?
    Are you sure you want to link your figshare account with this project?
    [Cancel][Import]

Importing or connecting an account loads the users' figshare information.

To the right of the the figshare title is text that reads::

    figshare authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads "Current Folder: None." This is updated when the user selects a folder. A blue button labeled
"Change" is below the "Current Folder" text. Clicking this button expands and collapses a table below.

The table has two columns—"Folders" and "Select." Under "Folders" is a list of all top level figshare folders the user has.
Folders can be expanded and collapsed. Each folder has a corresponding radio button in the "Select" column. When the user
selects a folder, text appears at the bottom of the table::

    Connect [folder title]?

Two buttons, "Cancel" and "Save" appear below the table. Cancelling removes the two buttons and confirmatory text but the folder
is still selected.

Clicking "Save" updates the "Current Folder" text and green inline text appears below the table, replacing the buttons::

    Successfully linked "[folder title]". Go to the Files page to view your content.

To disconnect figshare, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect figshare Account?
    Are you sure you want to remove this figshare account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the table and connected folder information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile."

If a figshare account is connected, only the user who connected the account can change the selected folder. Other Admins can
remove the add-on and connect another.  Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.


.. _github:

Configuring GitHub
***********
**Purpose:** Connecting to GitHub allows users to create a two way connection between the OSF and GitHub.

Users who choose to connect their GitHub account to the OSF can check appropriate box. They are presented with a
modal::

    GitHub Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of making a GitHub repo public or private.
    The OSF does not alter the permissions of linked GitHub repos.
    View / download file versions: GitHub files and their versions can be viewed/downloaded via OSF.
    Add / update files: Adding/updating files in the project via OSF will be reflected in GitHub.
    Delete files: Files deleted via OSF will be deleted in GitHub.
    Logs: GitHub dynamically updates OSF logs when files are modified outside the OSF. Changes to GitHub repos made before
    the repo is linked to the OSF will not be reflected in OSF logs.
    Forking: Forking a project or component does not copy Github authorization unless the user forking the project is the
    same user who authorized the Github add-on in the source project being forked.
    Registering: GitHub content will be registered, but version history will not be copied to the registration.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions.
    The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.


On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring GitHub.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button::

    Settings updated

If the user has not connected GitHub to their account previously, a row titled "GitHub" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, they will be navigated to a new window where GitHub authenticates the connection.
After authorizing, the user is returned to the OSF.

If the user has connected GitHub to their account previously, the link in the GitHub row reads "Import Account from Profile."

.. _todo: Log lack of confirmation modal as issue.

Importing or connecting an account loads the users' GitHub information.

To the right of the the "GitHub" title is text that reads::

    GitHub authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads "Current Repo:" Below this text is a dropdown that shows "------" by default.
To the right of the dropdown is a green button that reads "Create Repo." On the far right of this row is a green "Save" button.

In the dropdown are all of the user's GitHub repos. After selecting one, the user must save their changes. Leaving the page without
saving produces no warning and will not enact the changes.

Alternative to selecting an existing repo, the user can create a new one by clicking "Create Repo." This opens a modal::

    Name your new repo
    [text field]
    [Cancel][Save]

If the user saves an empty name field, the modal is closed and red inline text below the dropdown reads::

    Error: Your repo must have a name

If the user correctly enters a name, it becomes the choice selected in the dropdown.


Clicking "Save" produces green inline text below the dropdown::

    Settings updated

Clicking "Save" without making changes produces no effect.

To disconnect GitHub, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect GitHub Account?
    Are you sure you want to remove this GitHub account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the dropdown and connected repo information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile." Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.

.. _drive:

Configuring Google Drive
*************
**Purpose:** Connecting to Google Drive allows users to create a two way connection between the OSF and Google Drive.

Users who choose to connect their Google Drive account to the OSF can check appropriate box. They are presented with a
modal::

    Google Drive Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of Google Drive privacy. The OSF does not alter the
    permissions of linked Google Drive folders.
    View / download file versions: Google Drive files and their versions can be viewed/downloaded via OSF.
    Add / update files: Adding/updating files in the project via OSF will be reflected in Google Drive.
    Delete files: Files deleted via OSF will be deleted in Google Drive.
    Logs: The OSF keeps track of changes you make to your Google Drive content through the OSF, but not for changes made using
    Google Drive directly.
    Forking: Forking a project or component does not copy Google Drive authorization unless the user forking the project is
    the same user who authorized the Google Drive add-on in the source project being forked.
    Registering: Google Drive content will be registered, but version history will not be copied to the registration.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions. The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
    [Cancel][Confirm]

On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring Google Drive.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button:

    Settings updated

If the user has not connected Google Drive to their account previously, a row titled "Google Drive" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, they will be navigated to a new window where they can “Accept” the terms &
conditions of connecting Google Drive to the OSF. Upon clicking “Accept,” users are then taken back to the Settings
page on the OSF.

If the user has connected Google Drive to their account previously, the link in the Google Drive row reads "Import Account from Profile."
Clicking opens a modal that reads::

    Import Google Drive Account?
    Are you sure you want to link your Google Drive account with this project?
    [Cancel][Import]

Importing or connecting an account loads the users' Google Drive information.

To the right of the the "Google Drive" title is text that reads::

    Google Drive authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads "Current Folder: None." This is updated when the user selects a folder. A blue button labeled
"Change" is below the "Current Folder" text. Clicking this button expands and collapses a table below.

The table has two columns—"Folders" and "Select." Under "Folders" is a list of all top level Google Drive folders the user has.
Folders can be expanded and collapsed. Each folder has a corresponding radio button in the "Select" column. When the user
selects a folder, text appears at the bottom of the table::

    Connect [folder title]?

Two buttons, "Cancel" and "Save" appear below the table. Cancelling removes the two buttons and confirmatory text but the folder
is still selected.

Clicking "Save" updates the "Current Folder" text and green inline text appears below the table, replacing the buttons::

    Successfully linked "[folder title]". Go to the Files page to view your content.

To disconnect Google Drive, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect Google Drive Account?
    Are you sure you want to remove this Google Drive account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the table and connected folder information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile." Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.

.. _external link:
Configuring External Link
*************
**Purpose:** Adding an external link allows users to redirect project visitors to the provided URL. 

Users can create external links to external sites as well as to internal pages within the OSF, such as projects, components, and registrations, etc.

When a user checks the box next to the external link add-on, the "Settings" page reloads, and a Configure Add-ons pane appears below the "Select Add-ons" section of the "Settings" page. The text reads::

    External Link
    URL [field]
    Label [field]
    [Save]

The user can then enter the URL into the URL field. The user has the option to add a label to the external link in the Label field, but this step is not required. After the user enters the information and clicks "Save," a confirmation message appears below the Label field that reads::

    Successfully linked to [URL].
    
Now, when a user goes to that project or component and lands on its "Overview" page, a modal will immediately appear::
  
  This project contains a forward to
  [URL]
  [Cancel] [Redirect]

Clicking "Cancel" will keep the user on the project or component "Overview" page. Clicking "Redirect" will take the user to the site of the URL.

If a user has access to private projects/components or embargoed registrations, the user can create an external link to point to them; however, if project A is public and points to Project B which is private, a visitor who does not have access to Project B will still be prompted by the modal. The visitor can still click "Redirect," but they will be taken to a "Forbidden" page and will not be able to access the private project/component.

.. _mendeley:

Configuring Mendeley
*************
**Purpose:** Connecting to Mendeley allows users to create a two way connection between the OSF and Mendeley.

Users who choose to connect their Mendeley account to the OSF can check the appropriate box. They are presented with a
modal::

    Mendeley Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of making a Mendeley folder public or private.
    The OSF does not alter the permissions of a linked Mendeley folder.
    Forking: Forking a project or component does not copy Mendeley authorization unless the user forking the project is
    the same user who authorized the Mendeley add-on in the source project being forked.
    Registering: Mendeley content will not be registered.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions.
    The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
    [Cancel][Confirm]

On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring Box.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button::

    Settings updated

If the user has not connected Mendeley to their account previously, a row titled "Mendeley" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, they will be navigated to a new window where they can confirm the
connection with Mendeley before being taken back to the Settings page on the OSF. When they return to the OSF a modal appears::

    Import Mendeley access token
    Are you sure you want to link your Mendeley account with this project?
    [Cancel][Import]

If the user has connected Mendeley to their account previously, the link in the Mendeley row reads "Import Account from Profile."
Clicking opens a modal that reads::

    Import Mendeley access token
    Are you sure you want to link your Mendeley account with this project?
    [Cancel][Import]

Importing an account loads the users' Mendeley information.

To the right of the the Mendeley title is text that reads::

    authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads "Current Folder: None." This is updated when the user selects a folder. A blue button labeled
"Change" is below the "Current Folder" text. Clicking this button expands and collapses a table below.

The table has two columns—"Folders" and "Select." Under "Folders" is a list of all top level Mendeley folders the user has.
Folders can be expanded and collapsed. Each folder has a corresponding radio button in the "Select" column. When the user
selects a folder, text appears at the bottom of the table::

    Connect [folder title]?

Two buttons, "Cancel" and "Save" appear below the table. Cancelling removes the two buttons and confirmatory text but the folder
is still selected.

Clicking "Save" updates the "Current Folder" text and green inline text appears below the table, replacing the buttons::

    Successfully linked "[folder title]". Go to the Overview page to view your citations.

To disconnect Mendeley, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect Mendeley Account?
    Are you sure you want to remove this Mendeley account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the table and connected folder information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile." Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.

.. _zotero:

Configuring Zotero
**************
**Purpose:** Connecting to Zotero allows users to create a two way connection between the OSF and Zotero.

Users who choose to connect their v account to the OSF can check appropriate box. They are presented with a
modal::

    Zotero Add-on Terms
    Function | Status
    Permissions: Making an OSF project public or private is independent of making a Zotero folder public or private.
    The OSF does not alter the permissions of a linked Zotero folder.
    Forking: Forking a project or component does not copy Zotero authorization unless the user forking the project is
    the same user who authorized the Zotero add-on in the source project being forked.
    Registering: Zotero content will not be registered.

    This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions.
    The OSF is not responsible for the service or for your use thereof.
    This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
    [Cancel][Confirm]

On this modal, users can click “Cancel” to cancel this action and close the window or “Confirm” to continue configuring Box.

If user clicks “Confirm” but does not click “Apply,” and navigates away from page, a browser popup appears asking user to
confirm navigation away from the page because pending add-on changes were not saved.

After confirming, users will see a green “Apply” button appear at the bottom of the Select Add-ons panel. Clicking “Apply”
will apply the settings. Green inline text appears for a few seconds below the "Apply" button::

    Settings updated

If the user has not connected Zotero to their account previously, a row titled "Zotero" is listed in the
Configure Add-ons panel with a link—"connect account."

When users click the "connect account" link, they will be navigated to a new window where they can confirm the
connection with Zotero before being taken back to the Settings page on the OSF. When they return to the OSF a modal appears::

    Import Zotero access token
    Are you sure you want to link your Zotero account with this project?
    [Cancel][Import]

If the user has connected Zotero to their account previously, the link in the Zotero row reads "Import Account from Profile."
Clicking opens a modal that reads::

    Import Zotero access token
    Are you sure you want to link your Zotero account with this project?
    [Cancel][Import]

Importing an account loads the users' Zotero collections.

To the right of the the Zotero title is text that reads::

    authorized by [user who configured add-on]

The "Connect Account" link is replaced by a red "Disconnect Account" link.

Below that row is bold text that reads "Current Folder: None." This is updated when the user selects a folder. A blue button labeled
"Change" is below the "Current Folder" text. Clicking this button expands and collapses a table below.

The table has two columns—"Folders" and "Select." Under "Folders" is a list of all top level Zotero folders the user has.
Folders can be expanded and collapsed. Each folder has a corresponding radio button in the "Select" column. When the user
selects a folder, text appears at the bottom of the table::

    Connect [folder title]?

Two buttons, "Cancel" and "Save" appear below the table. Cancelling removes the two buttons and confirmatory text but the folder
is still selected.

Clicking "Save" updates the "Current Folder" text and green inline text appears below the table, replacing the buttons::

    Successfully linked "[folder title]". Go to the Overview page to view your citations.

To disconnect Zotero, the user clicks the red "Disconnect Account" link. This opens a modal::

    Disconnect Zotero Account?
    Are you sure you want to remove this Zotero account?
    [Cancel][Disconnect]

Clicking "Disconnect" removes the table and connected folder information. The "Disconnect Account" link is replaced by a link
that reads "Import Account from Profile." Alternatively, the user can uncheck the add-on from the "Select Add-ons" list and save their
changes.

Viewing Amazon S3 Files
***********
**Purpose:** The file tree and file details pages allow users to view and interact with Amazon S3 files.

Amazon S3 appears in in the file tree as an item in the component to which it has been added. It is on the same level as OSF Storage.
The tree identifies the project::

    Amazon S3: [bucket name]

File names from an Amazon S3 bucket are shown in the file tree on the OSF.

Selecting the Amazon S3 add-on in the file tree shows a "Download as zip" button in the toolbar. Clicking downloads the entire
contents of the bucket as a zip folder.

A "Create Folder" button is also shown when the add-on is selected. The user types a folder name and confirms creation. The folder
is then shown inside the Amazon S3 add-on. Files can be moved into and out of the folder. Folders can be removed by selecting the
folder and clicking "Delete Folder" in the toolbar. A modal opens::

    Delete "folder"?
    This folder and ALL its contents will be deleted. This action is irreversible.
    [Cancel][Delete]

Users with editing permissions can select an Amazon S3 file to rename it. Clicking the "Rename" button that appears in the file
tree's toolbar opens a text box where the new name can be entered and saved.

When a user with editing permissions selects Amazon S3 in the file tree, an “Upload” button appears. Clicking on “Upload”
opens a modal that allows you to select files from within your computer to upload. Admins and read+write contributors
can also drag and drop files onto the Amazon S3 add-on to upload a file.

If a new version of an already existent file is uploaded, the new version will replace the existing one.

If an Amazon S3 file is selected by a user, a "View" button appears in the toolbar. Clicking this button or clicking the file title
brings the user to the details (rendering) page where the file is rendered. No link is provided to view the file on Amazon S3.

On the file's detail page, the image is rendered in the default "view" pane. Users with editing permissions see a "Delete"
button in the top right.

    Delete file?
    Are you sure you want to delete [file name]?
    [Cancel][Delete]

Confirming the deletion brings the user to the file tree page where that file has been removed.

A blue "Download" button is also available on the detail page. Clicking downloads the file.

Text and code files can be edited from the file detail page by users with edit permissions. Clicking "Edit" opens a pane
to the right of the rendered text where the user can revise the contents of the file. Saving updates the contents of the file.
Edits are not rendered in the view of the file on the left. No formatting options are available.

Selecting the "Revisions" button on the detail page opens the revisions pane. Only the most recent version of the Amazon S3 file
is listed. The date of the upload is available, and a download button is shown on the right side of the pane.

Selecting a file from the file tree shows a "Download" button in the toolbar.  No "Download Multiple" button
is ever available, even if multiple Amazon S3 files are selected. Download counts are not available for Amazon S3.

If the user has editing privileges, clicking on an Amazon S3 file in the file tree shows a "Delete" button in the toolbar.
Clicking this button opens a modal::

    Delete "[file title]"?
    This action is irreversible.
    [Cancel][Delete]

If the user selects multiple files, a "Delete Multiple" button appears in the toolbar. Clicking opens a modal::

    Delete "[file title]"?
    This action is irreversible.

    [list of file titles]

    [Cancel][Delete]

After confirming, the files are removed from the OSF and Amazon S3.

Files from other storage add-ons can be moved into Amazon S3 by dragging and dropping. Files from Amazon S3 can be moved
into other add-ons as well.

Viewing Box Files
***********
**Purpose:** The file tree and file details pages allow users to view and interact with Box files.

Box appears in in the file tree as an item in the component to which it has been added. It is on the same level as OSF Storage.
The tree identifies the project::

    Box: [folder name]

File names from the indicated Box folder are shown in the file tree on the OSF.

Selecting the Box add-on in the file tree shows a "Download as zip" button in the toolbar. Clicking downloads the entire
contents of the folder as a zip file.

A "Create Folder" button is also shown when the add-on is selected. The user types a folder name and confirms creation. The folder
is then shown inside the Box add-on. Files can be moved into and out of the folder. Folders can be removed by selecting the
folder and clicking "Delete Folder" in the toolbar. A modal opens::

    Delete "folder"?
    This folder and ALL its contents will be deleted. This action is irreversible.
    [Cancel][Delete]

Users with editing permissions can select a Box file to rename it. Clicking the "Rename" button that appears in the file
tree's toolbar opens a text box where the new name can be entered and saved.

When a user with editing permissions selects Box in the file tree, an “Upload” button appears. Clicking on “Upload”
opens a modal that allows you to select files from within your computer to upload. Admins and read+write contributors
can also drag and drop files onto the Box add-on to upload a file.

If a new version of an already existent file is uploaded, the new version will replace the existing one.

If a Box file is selected by a user, a "View" button appears in the toolbar. Clicking this button or clicking the file title
brings the user to the details (rendering) page where the file is rendered. No link is provided to view the file on Box.

On the file's detail page, the image is rendered in the default "view" pane. Users with editing permissions see a "Delete"
button in the top right.

    Delete file?
    Are you sure you want to delete [file name]?
    [Cancel][Delete]

Confirming the deletion brings the user to the file tree page where that file has been removed.

A blue "Download" button is also available on the detail page. Clicking downloads the file.

Text and code files can be edited from the file detail page by users with edit permissions. Clicking "Edit" opens a pane
to the right of the rendered text where the user can revise the contents of the file. Saving updates the contents of the file.
No formatting options are available.

Selecting the "Revisions" button on the detail page opens the revisions pane. Only the most recent version of the Box file
is listed. The date of the upload is available, and a download button is shown on the right side of the pane.

Selecting a file from the file tree shows a "Download" button in the toolbar.  No "Download Multiple" button
is ever available, even if multiple Box files are selected. Download counts are not available for Box.

If the user has editing privileges, clicking on a Box file in the file tree shows a "Delete" button in the toolbar.
Clicking this button opens a modal::

    Delete "[file title]"?
    This action is irreversible.
    [Cancel][Delete]

If the user selects multiple files, a "Delete Multiple" button appears in the toolbar. Clicking opens a modal::

    Delete "[file title]"?
    This action is irreversible.

    [list of file titles]

    [Cancel][Delete]

After confirming, the files are removed from the OSF and Box.

Files from other storage add-ons can be moved into Box by dragging and dropping. Files from Box can be moved
into other add-ons as well.

Viewing Dataverse Files
***********
**Purpose:** The file tree and file details pages allow users to view and interact with Dataverse files.

Dataverse appears in in the file tree as an item in the component to which it has been added. It is on the same level as OSF Storage.
The tree identifies the project::

    Dataverse: [Dataset name] (Draft)[Draft]

File names from the indicated Dataset are shown in the file tree on the OSF. By default, the draft Dataset is shown.

Selecting the Dataverse add-on in the file tree shows a dropdown in the toolbar titled "Version:" From the dropdown, the user can
select the published Dataset or the draft Dataset. Changing the selection will show the appropriate Dataset. User will only see the options relevant to the dataset (if there is no draft version, only "published" will display, and vice versa).

When the add-on is selected and the Dataverse and Dataset have not been published, a "Publish" button is shown in the toolbar.
Clicking opens a modal::

    Publish this Dataverse and dataset?
    This dataset cannot be published until [Dataverse title] is published.
    By publishing this Dataverse and dataset, all content will be made available through the Harvard Dataverse
    using their internal privacy settings, regardless of your OSF project settings.
    Do you want to publish this Dataverse AND this dataset?

    [Cancel][Publish Dataverse and dataset]

When the add-on is selected and the Dataverse  has been published but the Dataset has not, a "Publish" button is shown in the toolbar.
Clicking opens a modal::

    Publish this Dataverse and dataset?
    By publishing this dataset, all content will be made available through the Harvard Dataverse using their internal
    privacy settings, regardless of your OSF project settings.
    Are you sure you want to publish this dataset?

    [Cancel][Publish dataset]

Confirming the choice to publish opens another modal::

    Your content has been published.
    [Okay]

When a draft dataset is selected, the "Publish" button is available even if it has been published. If the user clicks "Publish"
for a draft that has been published, the confirmation modal appears. On confirming, another modal appears::

    This dataset version has already been published.
    [Okay]

When a draft dataset from a published Dataverse is selected, the add-on row in the file tree reads::

    Dataverse: [Dataset] (Draft)

When a published dataset from a published Dataverse is selected, the add-on row in the file tree reads::

    Dataverse: [Dataset] (Published)

"Version:" dropdown is available for published Datasets, but no other add-on specific buttons are available in the toolbar.

If the user selects a published file in the file tree, a "Download" button is added to the toolbar. Clicking will download the
file. No "Download Multiple" button is ever available, even if multiple Dataverse files are selected. Download
counts are not available for Dataverse.

No "Upload" is available for published Datasets. Attempting to drag and drop onto a published dataset produces no action.

On the file tree, when a draft Dataset is selected by a contributor with editing privileges, an "Upload" button is
available in the toolbar to the left of the "Publish" button. Clicking opens the file selector. Files can also be
dragged and dropped into the file tree by users with editing privileges.

If a file cannot be uploaded, a red growlbox error shows in the upper right corner::

    Error
    Unable to reach the provider, please try again later. If the problem persists, please contact support@osf.io.

Even if an error was shown, if the user refreshes, the file may be uploaded to the draft Dataverse.

Files from other storage add-ons cannot be moved into Dataverse, nor can any Dataverse files be moved out.

If a new version of an already existent file is uploaded, the versions will not combine. Two identically titled files will be shown;
on refresh, the newer file will have an integer appended to the end to identify it as a subsequent copy.

If the user has editing privileges, clicking on a draft Dataverse file in the file tree shows a "Delete" button in the toolbar.
Clicking this button opens a modal::

    Delete "[file title]"?
    This action is irreversible.
    [Cancel][Delete]

If the user selects multiple draft files, a "Delete Multiple" button appears in the toolbar. Clicking opens a modal::

    Delete "[file title]"?
    This action is irreversible.

    [list of file titles]

    [Cancel][Delete]

After confirming, the files are removed from the OSF and Dataverse.

If any Dataverse file is selected by a user in the file tree, a "View" button appears in the toolbar. Clicking this button or clicking the file title
brings the user to the details (rendering) page where the file is rendered. No link is provided to view the file on Dataverse.

When viewing the detail page of a published file, a red "Delete" button is available in the top right. Clicking this button results
in a red growlbox error::

    Error
    Could not delete file

Draft files can be deleted. Clicking "Delete" opens a confirmation modal::

    Delete file?
    Are you sure you want to delete [file name]?
    [Cancel][Delete]

Confirming the deletion brings the user to the file tree page where that file has been removed.

A blue "Download" button is also available on the detail page. Clicking downloads the file.

The revisions view shows up to two versions: published and draft. The options present depend on if the file has ever been published and
if a draft version has been deleted. Clicking on the draft version shows the draft of the file, clicking on published shows the published version.
The "Delete" and "Download" buttons are available on the detail page for both published and draft files.

From the detail page of a file, the left hand panel displaying the file tree will show the Dataset that the viewed file belongs to—
draft or published. If the user visits a different version by selecting it in the revisions pane, the file tree will update to reflect
the current dataset.

To non-contributors, draft Dataverse files cannot be seen. If a dataset is completely unpublished, this means that the Dataverse add-on
does not appear in the file tree. Published files can be viewed and downloaded.


Viewing Dropbox Files
***********
**Purpose:** The file tree and file details pages allow users to view and interact with Dropbox files.

Dropbox appears in in the file tree as an item in the component to which it has been added. It is on the same level as OSF Storage.
The tree identifies the project::

    Dropbox: /[folder name]

File names from the indicated Dropbox folder are shown in the file tree on the OSF.

Selecting the Dropbox add-on in the file tree shows a "Download as zip" button in the toolbar. Clicking downloads the entire
contents of the folder as a zip file.

A "Create Folder" button is also shown when the add-on is selected. The user types a folder name and confirms creation. The folder
is then shown inside the Dropbox add-on. Files can be moved into and out of the folder. Folders can be removed by selecting the
folder and clicking "Delete Folder" in the toolbar. A modal opens::

    Delete "folder"?
    This folder and ALL its contents will be deleted. This action is irreversible.
    [Cancel][Delete]

Users with editing permissions can select a Dropbox file to rename it. Clicking the "Rename" button that appears in the file
tree's toolbar opens a text box where the new name can be entered and saved.

When a user with editing permissions selects Dropbox in the file tree, an “Upload” button appears. Clicking on “Upload”
opens a modal that allows you to select files from within your computer to upload. Admins and read+write contributors
can also drag and drop files onto the Box add-on to upload a file.

If a new version of an already existent file is uploaded, the new version will replace the existing one.

If a Dropbox file is selected by a user, a "View" button appears in the toolbar. Clicking this button or clicking the file title
brings the user to the details (rendering) page where the file is rendered. No link is provided to view the file on Dropbox.

On the file's detail page, the image is rendered in the default "view" pane. Users with editing permissions see a "Delete"
button in the top right.

    Delete file?
    Are you sure you want to delete [file name]?
    [Cancel][Delete]

Confirming the deletion brings the user to the file tree page where that file has been removed.

A blue "Download" button is also available on the detail page. Clicking downloads the file.

Text and code files can be edited from the file detail page by users with edit permissions. Clicking "Edit" opens a pane
to the right of the rendered text where the user can revise the contents of the file. Saving updates the contents of the file.
No formatting options are available.

Selecting the "Revisions" button on the detail page opens the revisions pane. Revisions from the last 30 days are available.
The date of upload for each version is shown, and a download button is shown on the right side of the pane.

Selecting a file from the file tree shows a "Download" button in the toolbar.  No "Download Multiple" button
is ever available, even if multiple Dropbox files are selected. Download counts are not available for Dropbox.

If the user has editing privileges, clicking on a Dropbox file in the file tree shows a "Delete" button in the toolbar.
Clicking this button opens a modal::

    Delete "[file title]"?
    This action is irreversible.
    [Cancel][Delete]

If the user selects multiple files, a "Delete Multiple" button appears in the toolbar. Clicking opens a modal::

    Delete "[file title]"?
    This action is irreversible.

    [list of file titles]

    [Cancel][Delete]

After confirming, the files are removed from the OSF and Dropbox.

Files from other storage add-ons can be moved into Dropbox by dragging and dropping. Files from Dropbox can be moved
into other add-ons as well.

From the :ref:`project overview <overview>` a Dataverse panel is visible below the file tree. The panel displays four
fields: Dataset, Global ID, Dataverse, and Citation. The titles and DOI assigned by Dataverse are available in the appropriate fields.
The citation generated by Dataverse is available in the Citation field. The DOI ("Global ID") and Dataverse fields
link to the dataset on the Dataverse website.


Viewing figshare Files
***********
**Purpose:** The file tree and file details pages allow users to view and interact with figshare files.

Refer to this `Google Doc <https://docs.google.com/document/d/1T8c69at_0X2WKficbYEV0z7bfM3jNFoWkYtmNmZjVPg/edit#heading=h.f17owbri8qc3>`_ for more information on allowabel figshare actions

figshare appears in in the file tree as an item in the component to which it has been added. It is on the same level as OSF Storage.
The tree identifies the project::

    figshare: [project title]

File names from a figshare project are shown in the file tree on the OSF—not the names assigned to them on figshare. Names of
both published, public files and private, draft files are shown in the tree. figshare files cannot be renamed. Folders cannot
be created within the figshare add-on.

If an OSF project is private and figshare is connected, a nondismissable blue alert is visible at the top of each page, regardless
of the privacy of the figshare files::

    Warning: This OSF component is private but figshare project 5022 may contain some public files or filesets.

If the OSF project is public, no alert is shown, regardless of the privacy of the figshare files. The titles of all figshare files are shown
in public projects.

If a figshare project is deleted from the figshare website, it no longer appears in the file tree, but is still visible as the
selected project on the project settings page.

When a user with admin or read+write permissions selects figshare in the file tree a “Upload” button appears. Clicking on “Upload”
opens a modal that allows you to select files from within your computer to upload. Admins and read+write contributors
can also drag and drop files onto the figshare add-on to upload a file. Uploading a file adds it to that
project on figshare as a draft.

If a new version of an already existent file is uploaded, two files with the exact same name will
appear in the add-on folder—they are not combined. Both these files will also appear in Figshare.

If a figshare file is selected by a user, a "View" button appears in the toolbar. Clicking this button or clicking the file title
brings the user to the details (rendering) page. Draft figshare files cannot be rendered. If the user clicks to render
a draft figshare file, in place of the rendered image is a blue alert::

    The file "[file name]" is still a draft on figshare.
    To view it on the OSF publish it on figshare.

No link is provided to view the file on figshare.

Public, published files on figshare are rendered on the OSF. Above the rendering is a link that reads::

    View this file on figshare.

Clicking this link sends the user to the figshare website.

When on the details page of a draft figshare file, no Download" button available. Users with editing permissions see a "Delete"
button on the details page of a draft file; clicking opens a confirmation modal::

    Delete file?
    Are you sure you want to delete [file name]?
    [Cancel][Delete]

Confirming the deletion brings the user to the file tree page where that file has been removed.

Public, published files cannot be deleted from the details page. A "Download" button is available.

If the user has editing privileges, clicking on a draft figshare file in the file tree shows a "Delete" button in the toolbar.
Clicking this button opens a modal::

    Delete "[file title]"?
    This action is irreversible.
    [Cancel][Delete]

If the user selects multiple draft files, a "Delete Multiple" button appears in the toolbar. Clicking opens a modal::

    Delete "[file title]"?
    This action is irreversible.

    [list of file titles]

    [Cancel][Delete]

After confirming, the files are removed from the OSF and figshare.

If the file is published, no "Delete" button is ever available from the file tree page. Two additional buttons
do show instead: "Download" and "View on figshare." Clicking "Download" will download a copy of the file.
Download counts are not available for figshare files. Clicking "View on figshare" will send the user to figshare
in that same browser window.

If multiple published files are selected, a "Download Multiple" button is available.

The user cannot select multiple published and draft files at once.

If the user attempts to move a draft file from figshare to OSF Storage, a red dismissable growlbox alert message will appear saying::

	Copy failed
	Cannot download private files.

The user receives an email as well::

    Hello,

    An error has occurred, and the file from [prject title] on The Open Science Framework was not successfully copied. Please
    log in and try this action again. If the problem persists, please email support@osf.io.

    The Open Science Framework Robot

Public, published figshare files can be copied to OSF storage. A copy of the file will be available in the figshare add-on and
the OSF Storage folders.

Files from other storage add-ons can be moved into figshare. These files are moved—not copied.

If the user moves a file with multiple versions into figshare, only the current version will be saved. All other versions will be lost.
Visiting the "revisions" view on a file's detail page shows a yellow alert in the revisions panel::

    figshare does not support file revisions.


Viewing GitHub Files
***********
**Purpose:** The file tree and file details pages allow users to view and interact with GitHub files.

GitHub appears in in the file tree as an item in the component to which it has been added. It is on the same level as OSF Storage.
The tree identifies the project::

    GitHub: [repo name] (branch)

File names from the indicated GitHub repo are shown in the file tree on the OSF.

Selecting the GitHub repo shows an "Open" button in the toolbar. Clicking sends the user to the GitHub website where the repo's
contents are shown.

A "Download" button appears when any user selects the GitHub repo. Clicking downloads the contents of the repo as a zip file.

A "Create Folder" button is shown when the add-on is selected by a user with editing permission. The user types a
folder name and confirms creation. The folder is then shown inside the GitHub add-on. Files can be moved into and out
of the folder. If moving a file fails, a red growlbox alert appears::

    Move failed.
    Please refresh the page or contact support@cos.io if the problem persists.

Depending on the error, a different alert may appear::

    Move failed.
    Update is not a fast forward

Even if an error is shown, refreshing the page may show the file has been successfully moved.

Folders cannot be deleted.

If a file from a folder in GitHub is moved elsewhere or a new file is uploaded to a location in GitHub where a file
of the same name exists, a modal appears::

    Replace "[file name]"?
    An item named "[file name]" already exists in this location.
    [Cancel][Keep Both][Replace]

Choosing "Replace" creates a new version of the file. Choosing "Keep Both" adds an integer to the end of the moved file's title
to indicate the difference.

When a user with editing permissions selects GitHub in the file tree, an “Upload” button appears. Clicking on “Upload”
opens a modal that allows you to select files from within your computer to upload. Admins and read+write contributors
can also drag and drop files onto the GitHub add-on to upload a file. If a new version of an already existent file is
uploaded, the new version will replace the existing one.

Selecting the GitHub add-on also shows a "Branch:" dropdown. The dropdown lists all existing branches of the repo. It is visible
even if only one branch is available.

Selecting a file from the file tree shows a "Download" button in the toolbar.  No "Download Multiple" button
is ever available, even if multiple GitHub files are selected. Download counts are not available for GitHub.

If the user has editing privileges, clicking on a GitHub file in the file tree shows a "Delete" button in the toolbar.
Clicking this button opens a modal::

    Delete "[file title]"
    This action is irreversible.
    [Cancel][Delete]

After confirming, the file is removed from the OSF and GitHub.

Files from other storage add-ons cannot be moved into GitHub. Files from GitHub can be copied into other add-ons by dragging
and dropping, however.

Users with editing permissions can select a GitHub file to rename it. Clicking the "Rename" button that appears in the file
tree's toolbar opens a text box where the new name can be entered and saved.

If the connected repo is public, any user can select a file and see the "View on GitHub" button in the toolbar. Clicking
sends the user to the GitHub website where the file is displayed. If the repo is private, neither contributors nor visitors
see this button.

If a GitHub file is selected by a user, a "View" button appears in the toolbar. Clicking this button or clicking the file title
brings the user to the details (rendering) page where the file is rendered. No link is provided to view the file on GitHub. The file detail page will show the branch on the left hand file navigation bar. 

No actions can be performed if the user selects multiple files.

On the file's detail page, the image is rendered in the default "view" pane. Users with editing permissions see a "Delete"
button in the top right.

    Delete file?
    Are you sure you want to delete [file name]?
    [Cancel][Delete]

Confirming the deletion brings the user to the file tree page where that file has been removed.

A blue "Download" button is also available on the detail page. Clicking downloads the file.

Text and code files can be edited from the file detail page by users with edit permissions. Clicking "Edit" opens a pane
to the right of the rendered text where the user can revise the contents of the file. Saving updates the contents of the file.
No formatting options are available.

Selecting the "Revisions" button on the detail page opens the revisions pane. All commited versions of the file are listed.
The version ID, the date of the commit, and the user name of the editor is available. A download button is shown on the
right side of the pane.

All changes to GitHub via the OSF are logged as individual commits.

If a private repo is connected to a private project that is then made public, a warning appears in the confirmation modal
for making the project public::

    This component is connected to a private GitHub repository. Users (other than contributors) will not be able to see
    the contents of this repo unless it is made public on GitHub.

When the user confirms, contributors see a non-dismissable blue alert at the top of the page::

    Warning: This OSF component is public, but the GitHub repo [repo name] is private. Users can
    view the contents of this private GitHub repository through this public project.

If the GitHub repo connected is public, but the OSF project is private, a blue non-dismissable alert is visible at the top
of the page for all contributors::

    Warning: This OSF component is private, but the GitHub repo [repo name] is public. The files in this GitHub repo can
    be viewed on GitHub here.

Viewing Google Drive Files
***********
**Purpose:** The file tree and file details pages allow users to view and interact with Google Drive files.

Google Drive appears in in the file tree as an item in the component to which it has been added. It is on the same level as OSF Storage.
The tree identifies the project::

    Google Drive: [folder name]

File names from the indicated Google Drive repo are shown in the file tree on the OSF.

A "Download as zip" button appears when any user selects the Google Drive add-on. Clicking downloads the contents of the folder as a zip file.

A "Create Folder" button is shown when the add-on is selected by a user with editing permission. The user types a
folder name and confirms creation. The folder is then shown inside the Google Drive add-on. Files can be moved into and out
of the folder. To delete a folder, users with editing permissions must select the folder and click on the "Delete Folder" button in the toolbar.
A modal opens::

    Delete "[folder]"?
    This folder and ALL its contents will be deleted. This action is irreversible.
    [Cancel][Delete]

When a user with editing permissions selects GitHub in the file tree, an “Upload” button appears. Clicking on “Upload”
opens a modal that allows you to select files from within your computer to upload. Admins and read+write contributors
can also drag and drop files onto the Google Drive add-on to upload a file. If a new version of an already existent file is
uploaded, the new version will replace the existing one.

Selecting a file from the file tree shows a "Download" button in the toolbar.  No "Download Multiple" button
is ever available, even if multiple Google Drive files are selected. Download counts are not available for Google Drive.

If the user has editing privileges, clicking on a Google Drive file in the file tree shows a "Delete" button in the toolbar.
Clicking this button opens a modal::

    Delete "[file title]"
    This action is irreversible.
    [Cancel][Delete]

If the user selects multiple files, a "Delete Multiple" button is shown in the toolbar. Clicking opens a confirmation modal::

    Delete "[file title]"?
    This action is irreversible.
    [list of file titles]
    [Cancel][Delete]

After confirming, the files are removed from the OSF and Google Drive.

Files from other storage add-ons can be dragged and dropped into Google Drive. Google Drive files can also be moved into other
add-ons, though the versions will not be kept (no warning is given).

Users with editing permissions can select a Google Drive file to rename it. Clicking the "Rename" button that appears in the file
tree's toolbar opens a text box where the new name can be entered and saved.

Any user can select a file and see the "View on Google Drive" button in the toolbar. Clicking
sends the user to the Google Drive website where the file is displayed.

If a Google Drive file is selected by a user, a "View" button appears in the toolbar. Clicking this button or clicking the file title
brings the user to the details (rendering) page where the file is rendered.

On the file's detail page, the file is rendered in the default "view" pane. Users with editing permissions see a "Delete"
button in the top right.

    Delete file?
    Are you sure you want to delete [file name]?
    [Cancel][Delete]

Confirming the deletion brings the user to the file tree page where that file has been removed.

A blue "Download" button is also available on the detail page. Clicking downloads the file.

Text and code files can be edited from the file detail page by users with edit permissions. Clicking "Edit" opens a pane
to the right of the rendered text where the user can revise the contents of the file. Saving updates the contents of the file.
No formatting options are available.

Selecting the "Revisions" button on the detail page opens the revisions pane. All saved versions of the file are listed.
The version ID and the date of the commit are available. A download button is shown on the right side of the pane.

Viewing External Link
******
**Purpose:** Users can connect a project to an external link. They are prompted to redirect to this link upon entering the OSF project. 

 Once this add-on is configured, visitors to the project will immediately receive a window that reads::

    This project contains a forward to URL
    [Cancel] [Redirect]

Canceling will cause the user to enter the OSF project. Clicking the link or "Redirect" will replace the current tab with the external link. 

Viewing Mendeley Content
******
**Purpose:** Users can share their citations associated with a project using Mendeley.

From a project's :ref:`overview page <overview>`, Mendeley content can be viewed in a panel below the file tree. The panel is
titled "Mendeley."

At the top of the panel is a dropdown with placeholder text::
    Citation STyle (e.g."APA")

Below this are the citations that the user who connected the add-on has stored in the linked folder. Citations are listed in a table.
Below the "Citation" column is the citation for each resource, formatted according to the style selected in the dropdown.
In the "Actions" column there is a paper icon. Hovering over the icon shows a tooltip that reads "Copy Citation." Clicking the paper icon
copies the citation to the user's clipboard.

Users can change the citation style from the default APA by clicking in the dropdown and beginning to type a citation style. Suggestions
based on the input will appear as items in the dropdown. If the user selects one, the citations in the Citation column are
reformatted accordingly.

Viewing Zotero Content
******
**Purpose:** Users can share their citations associated with a project using Zotero.

From a project's :ref:`overview page <overview>`, Zotero content can be viewed in a panel below the file tree. The panel is
titled "Zotero."

At the top of the panel is a dropdown with placeholder text::
    Citation Style (e.g."APA")

Below this are the citations that the user who connected the add-on has stored in the linked folder. Citations are listed in a table.
Below the "Citation" column is the citation for each resource, formatted according to the style selected in the dropdown.
In the "Actions" column there is a paper icon. Hovering over the icon shows a tooltip that reads "Copy Citation." Clicking the paper icon
copies the citation to the user's clipboard.

Users can change the citation style from the default APA by clicking in the dropdown and beginning to type a citation style. Suggestions
based on the input will appear as items in the dropdown. If the user selects one, the citations in the Citation column are
reformatted accordingly.

Viewing OSF Storage Files
******
**Purpose**: OSF Storage allows users to store and share files. 

Users can obtain and distribute links for their documents in public projects on the OSF so others can then view the same rendered files. In addition, users are provided two different methods of embedding those documents, one in which the iFrame is dynamically rendered and another which provides the iFrame directly.

If the user is an admin on the project, the following buttons are visible to them in the top right of the "File Details" page::

    Delete
    Share
    Download
    View
    Revisions

To any visitor viewing a file on a public project, only the "Share,""Download," "View," and "Revisions" buttons are visible in the top right of the "File Details" page.

When the user clicks the **Share** button, a popover appears with the following two tabs::
    
    [Share][Embed]

The "Share" tab provides a URL and a button to copy the URL to the user's clipboard. Below the URL field are Twitter, Facebook, LinkedIn, and email buttons to share the URL on social media.

The "Embed" tab provides two entries::
  
    Dynamically Render iFrame with JavaScript (with the associated javascript in a box below)
    
    Direct iFrame with Fixed Height and Width (with the assocated HTML in a box below)
    
When the user clicks the **Download** button, the file is downloaded onto their computer.

The user can toggle the "View" and "Revisions" buttons on and off. The selected button is blue and the unselected button is gray. The "View" button is automatically blue and selected for the user so that the file is displayed in the MFR when the user arrives on the "File Details" page. The "Revisions" button is automatically gray when the user arrives on the page.

When the user clicks the **Revisions** button, the "View" button turns gray and the "Revisions" button turns blue. Clicking the **Revisions** button shows a table of the different versions that the file has gone through (in the order of the most recent version to the oldest). The table format appears as follows::
  
    Version ID | Date | User | Download | MD5 [?]| SHA2 [?]

The "Version ID" column displays the version number (e.g. 1,2,3, etc.).

The "Date" column displays the date when the file version was created.

The "User" column displays the user's name which, when clicked, links to their profile page.

The "Download" column displays the number of times the file version has been downloaded.

The "MD5" column displays the MD5 algorithm and a button that the user can click to save the MD5 to their clipboard. The user can hover over the "?" to bring up a tooltip that explains MD5::
  
    MD5 is an algorithm used to verify data integrity.

The "SHA2" column displays the SHA2 algorithm and a button that the user can click to save the SHA2 to their clipboard. The user can hover over the "?" to bring up a tooltip that explains SHA2::
  
    SHA-2 is a cryptographic hash function designed by the NSA used to verify data integrity.

The user can click the most recent version ID to display the file in the MFR on the "File Details" page. When the user does this, the "View" button is selected and the "Revisions" button is grayed out in the top right of the page. Only the most recent file version can be displayed in the MFR.