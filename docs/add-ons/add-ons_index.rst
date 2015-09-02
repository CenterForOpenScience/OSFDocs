.. _add-ons:

Add-Ons
==========
**Purpose:** Add-ons can be used to connect a third party service to the OSF.

For information on linking an OSF account to an add-on, visit :ref:`User Level Add-on Settings <user-addon>`

Include linking to add-on, overview widget, files browser behavior, file detail page.



Dataverse: if they have multiple linked to their user profile then when the connect the account they can choose from a dropdown (if they don't have multiple connected...)


Amazon S3: https://github.com/CenterForOpenScience/osf.io/pull/3363
https://github.com/CenterForOpenScience/osf.io/pull/3812

Google Drive: https://github.com/CenterForOpenScience/osf.io/issues/3748

Mendeley: https://github.com/CenterForOpenScience/osf.io/pull/3900

.. _s3:

Amazon S3
**********

.. _box:

Box
*******

.. _dataverse:

Dataverse
************

.. _dropbox:

Dropbox
************

.. _figshare:

figshare
***********

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

GitHub
***********

.. _drive:

Google Drive
*************

.. _mendeley:

Mendeley
*************

.. _zotero:

Zotero
**************
