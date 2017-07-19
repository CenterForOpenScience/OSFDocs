
**Purpose:** Accessing add-on settings through the user’s settings allows the user to have a complete view of their add-on
use and can disable an add-on globally.

To get to the user level add-on settings, the user must visit their settings by clicking on the gear in the
:ref:`navigation bar <navigation-bar>`. Then, in the left hand navigation the user must click on “Configure Add-on Accounts.”
From this page, users can connect their OSF account to third-party services, disconnect those services, and view the project
that have specific add-ons associated with them.

Connections to particular projects must be managed through the :ref:`project’s settings <project-settings>`.

Amazon S3
-----------
**Purpose:** Configuring Amazon S3 from the user’s settings page allows the user to manage their connection between the OSF and Amazon S3.
To connect Amazon S3 to an OSF account via the user settings page, the user must enter their Access Key and Secret Key.
Empty fields for each are available below the Amazon S3 title. Clicking the “Save” button or hitting the return key allows
the user to submit their keys.

When the user types in the Access Key field, the text is visible. When they enter text into the Secret Key field, the text
is obfuscated so that each character appears as a dot.

If the user submits the correct keys, a green inline alert appears below the “Save” button that reads::

    Settings updated

The save button is still active and can be repressed, producing the same alert. On refresh, the key fields are gone.
Next to the Amazon S3 title is muted text that reads::

    authorized by [OSF user name]

To the right of this is a red link titled “Disconnect Account.” Clicking this link pulls up a modal that reads::

    Disconnect S3 Account?
    Are you sure you want to disconnect the S3 account? This will revoke access to S3 for all projects you have associated with this account.
    [Cancel][Disconnect]

Confirming the disconnect refreshes the page and the empty fields are visible again.

If the user enters only their Access Key or only their Secret Key, a red inline alert appears below the “Save” button that reads::

    All the fields above are required.

Refreshing the page empties the fields.

If the user enters incorrect keys, a red inline alert appears below the “Save” button that reads::

    Unable to list buckets. Listing buckets is required permission that can be changed via IAM

Refreshing the page empties the fields.

After the add-on has been configured a user can connect it to a project. If it has been connected to a project, below the
Amazon S3 title is a table titled “Authorized Projects.” In this table are the titles of all connected projects. The titles
are links to the project overview page. To the right of the titles is a column with red ‘x’s. Clicking an ‘x’ pulls up a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the Amazon S3 account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If all projects are disconnected, the table is no longer visible.
If the user visits a disconnected project’s settings page, they will see that the add-on is still selected but is not configured.

Box
--------
**Purpose:** Configuring Box from the user’s settings page allows the user to manage their connection between the OSF and Box.

To connect a Box account via the user settings page, the user must click the blue “Connect Account” link to the right of
the Box title. This will bring the user to a new page where they provide their Box login information and confirm the connection.
After submitting their login information, they are brought back to the OSF.

Next to the Box title is muted text that reads::

    authorized by [Box user name]

Green text appears below the Box title::

    Add-on successfully authorized. To link this add-on to an OSF project, go to the settings page of the project, enable
    Box, and choose content to connect.

To the right of the title is a red link titled “Disconnect Account.” Clicking this link pulls up a modal that reads::

    Disconnect Box Account?
    Are you sure you want to disconnect the Box account? This will revoke access to Box for all projects you have associated with this account.
    [Cancel][Disconnect]

Confirming the disconnect refreshes the page; the green text is gone and the “Disconnect Account” link is replaced by “Connect Account."

When the user has a project that is connected to Box, a table appears below the Box title. The header reads::

    Authorized Projects:

Below the header row is the name of each project that Box is connected to.  Clicking the project name sends you to the
project's overview page. On the right side of the table is a red 'x.' Clicking
the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the Amazon S3 account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If all projects are disconnected, the table is no longer visible.
If the user visits a disconnected project’s settings page, they will see that the add-on is still selected but is not configured.


Dataverse
------------
**Purpose:** Configuring Dataverse from the user’s settings page allows the user to manage their connection between the OSF and Dataverse.

To connect a Dataverse account from the user's settings page, the user must click the blue “Connect Account” link to the right of the Dateverse title.
This will pull up a modal that reads::

    Connect a Dataverse Account
    Dataverse Repository
    [dropdown options: dataverse.harvard.edu, dataverse-demo.iq.harvard.edu, apitest.dataverse.org, Other (please specify)]
    [cancel] [save]

The user must select a Dataverse repository to connect. After selecting an option from the dropdown, a second blank field appears
to the right, titled "API Token" muted text to the right of the title reads "Get from Dataverse" and links to a new tab that connects
the user to the Dataverse website where an authenticated user can generate a token.

If the user selects the "Other" option, an additional field is shown below the dropdown. The text field is empty but is preceded with "https://"
and there is blue information text below that reads:

    Only Dataverse repositories v4.0 or higher are supported.

If the user has selected the "Other" option but does not specify a web address or provides an invalid one, a red alert appears
below the three fields::

    Sorry, but there was a problem connecting to that instance of Dataverse. It is likely that the instance hasn't been
    upgraded to Dataverse 4.0. If you have any questions or believe this to be an error, please contact support@osf.io.

.. todo:: Log this as a bug—if it's empty, it should not say that it's likely that it's because it hasn't been updated.

If the user types in the web address of one of the drop-down options, the entry is still valid.

If the user tries to save the form without filling in the API token but has provided a valid Dataverse repository, a red
inline alert appears below the dropdown::

    Your Dataverse API token is invalid.

If the user enters an incorrect API token, that same alert appears.

If the user submits a valid response to each field and clicks "Save" a table row appears below the the Dataverse title.
The top row reads::

    Authorized on [Dataverse Repository URL]

There is a red "Disconnect Account" link to the right of the "Authorized on" text.

Users can connect to multiple Dataverse repositories. To connect to a second repository, they can click on "Connect Account" after
having already connected to one. The same four dropdown options are available. If the user attempts to connect to a repository
that is already connected, saving simply produces no changes. Each new repository creates a new row in the table.

.. todo:: You shouldn't have the option of connecting to a repo that is already connected. Log this bug.

Users can disconnect repositories by clicking the "Disconnect Account" link to the right of the repository name. Clicking
there opens a modal that reads::

    Disconnect Dataverse Account?
    Are you sure you want to disconnect the Dataverse account on [Dataverse Repository URL]? This will revoke access to Dataverse
    for all projects associated with this account.
    [Cancel][Disconnect]

Clicking "Disconnect" removes the repository from the table list.

When the user has a project that is connected to Dataverse, it is listed below the appropriate "Authorized on" row.
Clicking the project name sends you to the
project's overview page. On the right side of the table is a red 'x.' Clicking the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the Dataverse account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If a Dataverse has no connected projects but it is still
authorized to connect to the user's account, the "Authorized On" row is still visible. If the user visits a disconnected
project’s settings page, they will see that the add-on is still selected but is not configured.


Dropbox
------------
**Purpose:** Configuring Dropbox from the user’s settings page allows the user to manage their connection between the OSF and Dropbox.

To connect a Dropbox account from the user's settings page, the user must click the blue “Connect Account” link to the right of the Dropbox title.
This will bring the user to a new page where Dropbox requests confirmation. After the user allows the connection, they will be
returned to their settings page. The "Connect Account" text will be replaced by a red "Disconnect Account" link. To the right of the
Dropbox title is muted text that reads::

    authorized by [Dropbox Username]

Below this is green text that reads::

    Add-on successfully authorized. To link this add-on to an OSF project, go to the settings page of the project, enable Dropbox,

and choose content to connect.

When the user has a project that is connected to Dropbox, a table appears below the Dropbox title. The header reads::

    Authorized Projects:

Below the header row is the name of each project that Dropbox is connected to. Clicking the project name sends you to the
project's overview page. On the right side of the table is a red 'x.' Clicking
the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the Dropbox account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If all projects are disconnected, the table is no longer visible.
If the user visits a disconnected project’s settings page, they will see that the add-on is still selected but is not configured.

figshare
----------
**Purpose:** Configuring figshare from the user’s settings page allows the user to manage their connection between the OSF and figshare.

To connect a figshare account from the user's settings page, the user must click the blue “Connect Account” link to the right of the figshare title.
This will bring the user to a new page where figshare requests confirmation. After the user allows the connection, they will be
returned to their settings page. The "Connect Account" text will be replaced by a red "Disconnect Account" link. To the right of the
figshare title is muted text that reads::

    authorized by [OSF Username]

When the user has a project that is connected to figshare, a table appears below the figshare title. The header reads::

    Authorized Projects:

Below the header row is the name of each project that figshare is connected to. On the right side of the table is a red 'x.' Clicking
the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the figshare account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If all projects are disconnected, the table is no longer visible.
If the user visits a disconnected project’s settings page, they will see that the add-on is still selected but is not configured.

GitHub
----------
**Purpose:** Configuring GitHub from the user’s settings page allows the user to manage their connection between the OSF and GitHub.

To connect a GitHub account from the user's settings page, the user must click the blue “Connect Account” link to the right of the GitHub title.
This will bring the user to a new page where GitHub requests confirmation. After the user allows the connection, they will be
returned to their settings page. The "Connect Account" text will be replaced by a red "Disconnect Account" link. To the right of the
GitHub title is muted text that reads::

    authorized by [GitHub Username]

When the user has a project that is connected to GitHub, a table appears below the GitHub title. The header reads::

    Authorized Projects:

Below the header row is the name of each project that GitHub is connected to. On the right side of the table is a red 'x.' Clicking
the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the GitHub account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If all projects are disconnected, the table is no longer visible.
If the user visits a disconnected project’s settings page, they will see that the add-on is still selected but is not configured.

Google Drive
----------
**Purpose:** Configuring Google Drive from the user’s settings page allows the user to manage their connection between the OSF and Google Drive.

To connect a Google Drive account from the user's settings page, the user must click the blue “Connect Account” link to the right of the Google Drive title.
This will bring the user to a new page where Google Drive requests confirmation. After the user allows the connection, they will be
returned to their settings page. The "Connect Account" text will be replaced by a red "Disconnect Account" link. To the right of the
Google Drive title is muted text that reads::

    authorized by [Google Username]

When the user has a project that is connected to Google Drive, a table appears below the GitHub title. The header reads::

    Authorized Projects:

Below the header row is the name of each project that Google Drive is connected to. On the right side of the table is a red 'x.' Clicking
the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the GitHub account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If all projects are disconnected, the table is no longer visible.
If the user visits a disconnected project’s settings page, they will see that the add-on is still selected but is not configured.

Mendeley
----------
**Purpose:** Configuring Mendeley from the user’s settings page allows the user to manage their connection between the OSF and Mendeley.

To connect a Mendeley account from the user's settings page, the user must click the blue “Connect Account” link to the right of the Mendeley title.
This will bring the user to a new tab where Mendeley requests confirmation. After the user allows the connection, they will be
returned to their settings page and the new tab will be closed.

A table row is then listed below the Mendeley title. In muted text, the row reads::

    Authorized by [Mendeley Username]

To the right, a red "Disconnect Account" link allows the user to cancel the connection.

Below the table is green text that reads::

    Add-on successfully authorized. To link this add-on to an OSF project, go to the settings page of the project, enable Mendeley,
    and choose content to connect.

Clicking on the "Disconnect Account" link opens a modal::

    Disconnect Mendeley Account?
    Are you sure you want to disconnect the Mendeley account [Mendeley username]? This will revoke access to Mendeley
    for all projects you have authorized.
    [Cancel][Disconnect]

Clicking "Disconnect" removes the repository from the table list.

Users can connect to multiple Mendeley accounts. To connect to an additional account, they click the blue "Connect Account" link
and authorize a new connection. The new connection will add another row to the table, listing the "Authorized by" information for the
appropriate username. If the user tries to connect to the same Mendeley account twice, no error is shown but no changes are made.

When the user has a project that is connected to Mendeley, it is listed below the appropriate "Authorized on" row. Clicking the project
name sends you to the
project's overview page. On the right side of the table is a red 'x.' Clicking the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the Mendeley account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If Mendeley has no connected projects but it is still
authorized to connect to the user's account, the "Authorized by" row is still visible. If the user visits a disconnected
project’s settings page, they will see that the add-on is still selected but is not configured.

Zotero
----------
**Purpose:** Configuring Zotero from the user’s settings page allows the user to manage their connection between the OSF and Zotero.

To connect a Zotero account from the user's settings page, the user must click the blue “Connect Account” link to the right of the Zotero title.
This will bring the user to a new tab where Zotero requests confirmation. After the user allows the connection, they will be
returned to their settings page and the new tab will be closed.

A table row is then listed below the Zotero title. In muted text, the row reads::

    Authorized by [Zotero Username]

To the right, a red "Disconnect Account" link allows the user to cancel the connection.

Below the table is green text that reads::

    Add-on successfully authorized. To link this add-on to an OSF project, go to the settings page of the project, enable Zotero,
    and choose content to connect.

Clicking on the "Disconnect Account" link opens a modal::

    Disconnect Account?
    Are you sure you want to disconnect the Zotero account [Zotero username]? This will revoke access to Zotero
    for all projects you have authorized.
    [Cancel][Disconnect]

Clicking "Disconnect" removes the repository from the table list.

Users can connect to multiple Zotero accounts. To connect to an additional account, they click the blue "Connect Account" link
and authorize a new connection. The new connection will add another row to the table, listing the "Authorized by" information for the
appropriate username. If the user tries to connect to the same Zotero account twice, no error is shown but no changes are made.

When the user has a project that is connected to Zotero, it is listed below the appropriate "Authorized on" row. Clicking the
project name sends you to the
project's overview page. On the right side of the table is a red 'x.' Clicking the 'x' opens a modal that reads::

    Remove addon?
    Are you sure you want to disconnect the Zotero account from this project?
    [Cancel][Remove]

Clicking “Remove” disconnects the add-on from the project. If Zotero has no connected projects but it is still
authorized to connect to the user's account, the "Authorized by" row is still visible. If the user visits a disconnected
project’s settings page, they will see that the add-on is still selected but is not configured.
