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

Alternative to selecting an existing repo, the user can create a new one by clicking "Create Repo." This opens a modal::

    Bucket Name [text field]
    Bucket Location [dropdown]
    [Cancel][Create]

If the user saves an empty name field, the modal is closed and red inline text below the dropdown reads::

    Bucket name cannot be empty

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
to Dataverse where a Token is provided. The user must copy this and paste it into the field on the OSF.

.. todo:: update after bug is fixed (presently, no validation of url and no api token needed)

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

figshare
***********
**Purpose:** Connecting to figshare allows users to create a two way connection between the OSF and figshare.


**Purpose:** Figshare is a particular third party storage service users can connect to the OSF to house a variety of file types, either publicly or privately

Settings page
>>>>>>>>>>>>>

**Purpose:** The settings page is where you connect add-ons to a specific project. This can be done by Admin and Read-Write contributors. Read only contributors cannot connect add-ons, nor can they see that this is even an option.

Admins will see a list of potential add-ons with check-boxes next to them. After clicking on the check-box next to figshare, they will see the following pop-up::

	figshare Add-on Terms
	Function	Status
	Permissions	Making an OSF project public or private is independent of making figshare content public or private. The OSF does not alter the permissions of linked figshare content.
	View / download file versions	figshare content can be viewed and downloaded via OSF provided it is "published" on figshare.
	Add / update files	Files can be added but not updated.
	Delete files	figshare files cannot be deleted via OSF.
	Logs	OSF keeps track of changes you make to your figshare content through OSF, but not for changes made using figshare directly.
	Forking	Forking a project or component does not copy figshare authorization unless the user forking the project is the same user who authorized the figshare add-on in the source project being forked.
	Registering	figshare content will be registered, but version history will not be copied to the registration.
	This add-on connects your OSF project to an external service. Use of this service is bound by its terms and conditions. The OSF is not responsible for the service or for your use thereof.
	This add-on allows you to store files using an external service. Files added to this add-on are not stored within the OSF.
	[Cancel][Confirm]

Users can either click “Cancel” to cancel the action, or “Confirm” to continue configuring the add-on. No matter which option they choose, the pop-up disappears. 

If they try to leave the page at this point, they will get a pop-up (from the browser, not OSF) which says::

	Are you sure you want to leave this page?
	The changes on addon setting are not submitted!

There will be no notice on the project page that figshare has not been configured. This is the same for contributors and visitors. 

If they click on the green “Apply” button, the page will update and a new section will appear called ‘Configure Add-ons’ with the figshare logo and figshare underneath it. If the user does not click the ‘Apply’ button

**If figshare has already been added to the User account**, to right of the figshare logo, users have the options to ‘Import Account from Profile’. Clicking on this opens up a pop-up that reads::

	Import figshare Account?
	Are you sure you want to link your figshare account with this project?

Users can either ‘Cancel’ this action which makes the pop-up go away, or ‘Import’. This causes the page to change and a list of their figshare folders appear, with radial buttons to the right of them so they can choose which folder to connect to their account. They can only choose one folder. Note that in this case, what the OSF lists as ‘folders’ correspond to figshare ‘Projects’ or ‘Filesets’. Individual pieces from ‘My data’ on figshare are not listed as possible things to connect to the OSF. Additionally, to the right of the figshare logo is shows who authorized the add-on, and admins/read-write contributors have an option to ‘Disconnect Account’ listed in red.

**If figshare has not been added to the user account***, users have the option to ‘Connect Account’. Clicking on this takes them to figshare, where they have to login. After loving in, they see::

	Allow Open Science Framework to:Read & write draft dataRead & write private dataRead & write public data [Deny][Allow]

Clicking ‘Allow’ take the user back to their OSF project settings page. Users see the ‘Change’ button, but the folders section is not visible until after users click on the ‘Change’ button. Then the page appears as above.


Once a user clicks on a particular radial button, a message appears in blue saying::

	Connect “<name of folder>”?

Users can either ‘Cancel’ this, which makes the message go away, or ’Save’. If the click on ‘Cancel’ and only have one folder, that radial button will still be selected, and clicking on it again will not bring back the ‘Cancel’ and ‘Save’ options. If you refresh the page, the folder section area will not show up automatically, just the ‘Change’ button and nothing underneath it. If you click on ‘Change’ the folder selection area will reappear. 

If the user clicks on ‘Cancel’ or does not click on anything, the file tree on the project page does not show the add-on, or does it show any warning message. Visitors see the same thing. 

If the user clicks ‘Save’, the following shows up below this area::

	Successfully linked "Documentation testing". Go to the Files page to view your content.


**Disconnecting an add-on***

If a user clicks on the ‘Disconnect Account’ option, a pop-up appears saying::

	Disconnect figshare Account?
	Are you sure you want to remove this figshare account? 
	[Cancel][Disconnect]

If the user clicks “Cancel” the pop-up goes away. If they click “Disconnect” the folders under the add-on disappear and the ‘Import Account from Profile’ option re-appears. This behavior is identically whether the user is disconnected a figshare add-on connect by them, or by another contributor on the project.



File Tree Page (as admin & read-write contributors)
>>>>>>>>>>>>>>

**Purpose:** The file tree page allows users to see and interact with only the file-tree of the project. 


**As an admin & read-write contributor**
When a user selects the figshare add-on storage, “Upload” and “Search” buttons appear. Clicking on “Upload” causes a pop-up to appear which allows you to select files from within your computer to upload. Uploading a file adds it to that project on figshare. If a new version of an already existent file is uploaded, two files with the exact same name will appear in the add-on folder. Both these files will also appear in Figshare. Clicking on “Seach” causes a search bar to appear just above the file tree, which searches through file names from any part of the project (not just the figshare add-on section).

For published figshare file seres, when a users selects a specific file, “Download”, “View”, “View on figshare” and “Search” buttons appear. 

For non-published figshare projects or file sets, when a user selects a file within figshare storage, “View”, “Delete”, and “Search” buttons appear. 

Clicking on “View” takes you to the file view page for that particular file. Clicking on “View on figshare” takes you to the file on figshare. Clicking on “Download” downloads the file. Clicking on the “Delete” button brings up a pop-u which says::

	Delete "week6d_time_sharing.sas"?
	This action is irreversible.
	[Cancel][Delete]

Clicking on “Cancel” makes the pop-up go away makes the pop-up disappear. Clicking “Delete” deletes the file from figshare.

For non-published projects and datasets, files can be moved into figshare projects from OSF storage. If you move a file with multiple versions into figshare, only the current version will be moved in. All other versions will be lost. If you attempt to move a from figshare to OSF storage, an error message will appear saying::

	Copy failed
	Cannot download private files.

For published figshare datasets, moving a file from figshare to OSF storage will retain the file in figshare and create another copy of the file in OSF storage. Copying a file from OSF storage to figshare appears to work (the file moves), but it does not show up in the published figshare project on figshare, and unlike published files on figshare shows a “Delete” option.

**As a visitor**

When a visitor selects the figshare add-on storage, nothing changes. The “Search” buttons is still visible.

When a visitor selects a file within figshare storage, “View” and “Search” buttons appear. Clicking on “View” takes you to the file view page for that particular file.


File View Page
>>>>>>>>>>>>>>

**Purpose:** The file view page allows users to see and, for some, interact with files uploaded to add-ons/OSF storage.

The revisions tab reads::

	Revisions
	figshare does not support file revisions.


For non-published figshare files, users see the following message::

	The file "inflammation-01.csv" is still a draft on figshare. 
	To view it on the OSF publish it on figshare.

For published figshare files, the file renders (if OSF supports that format). Above the rendered file, users see the options to::
	
	View this file on figshare

Clicking on the link will take them to the content on figshare.


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

.. _mendeley:

Mendeley
*************

.. _zotero:

Zotero
**************
