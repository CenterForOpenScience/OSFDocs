Public Profiles
****************

**Purpose:**  A user's public profile is a homepage for information about the user and their public OSF projects.

The contents of public profiles are visible to any OSF visitor or user. An OSF user can access their public profile by clicking
on their name in the :doc:`navigation bar <../navigation/navigation>` or by visiting osf.io/profile. Every user is assigned a
unique URL that can also be used to view their public profile. This URL is listed on the public profile page
below the user's name. Searching the OSF for a user and clicking on their name in the search results will direct you to their profile,
using the unique URL.

All public profiles show the user's name, their sign up date (listed as "Member Since [date]"), their public profile's unique URL,
their public projects and components, as well as their activity points. Optional information includes links to their social
network accounts, their education history, and employment history. These optional fields are shown on the top right of the user's
public profile. They are grouped into tabs; social information is shown by default, employment history is the next tab, and education
history is the final tab.

Social information is listed in rows. The social account name (e.g. LinkedIn or Twitter) is listed on the left and a link to the
profile is on the right.

Employment information is listed in a table. Table headers include "institution," "department,"
"title," "start date," and "end date." If no employment information is shared, only the table headers are visible.

.. todo:: describe each display format for social.



To edit profile information, users can visit their User Settings. By default, the "Profile Information" page is shown, and the "Name" tab
is selected.

User Names
------------

**Purpose:** Configuring their user name allows the user to change how they are listed in search results and contributor lists as well as
in citations.

Several text fields on the "Name" tab on the "Profile Information" allow the user to configure their citation and user name preferences. At the bottom of
the page is a "Cancel" and a "Save" button.

The first field is titled::

    Full Name (e.g. Rosalind Eslie Franklin)

This field is automatically filled in with the name the user provided on sign up. The user can click in this field to edit their name.

Below this field is muted text that reads::

    Your full name, above, is the name that will be displayed in your profile. To control the way your name will appear
    in citations, you can use the "Auto-fill" button to automatically infer your first name, last name, etc., or edit
    the fields directly below.

If the user tries to delete the contents and save an empty field, a red text alert appears below the "Save" button::

    Could not update settings

The text disappears after several seconds.

There is no minimum character limit for the user's Full Name, nor is there a maximum. If the user updates their name and presses the "Save"
button, a green text alert is shown below the "Save" button::

    Settings updated

The text disappears after several seconds.

The "Full Name" field corresponds to the user name. After saving changes to this field, to see the user name updated in the navigation bar,
the page must be refreshed. If the user name is too long, it will be shortened in the navigation bar by the insertion of an elipses so
that the beginning and end of the username are visible, but the middle portion of the name is hidden.

Below the "Full Name" field is a button labeled "Auto-fill." Below this button are four additional text fields: "Given Name,"
"Middle Name(s)," "Family Name," and Suffix. Clicking the "auto-fill" button transfers the first word from the "Full Name" field to
the "Given Name" field. The last word is transferred to the "Family Name" field and any interevening words are added to the "Middle Name" field.
If any recognizable suffixes are listed last in the "Full Name" field, such as Jr, Sr, or roman numerals, these will be aded to the "Suffix" field.
Titles are removed. Words entered in quotes are interpreted as nicknames and are removed.

If the user enters their name as "Last name, First name" then the words preceding the comma are entered in as the "Family Name."

The user can edit the four individual name fields (i.e. given, middle, family, and suffix) individually, rather than using the auto-fill function.
To do so, the user clicks into the field and saves their changes. These four fields do not affect the user name—what is shown in
contributor lists and the navigation bar—but they do affect citations. Any or all of these fields can be left blank. There is no character limit.
As the user updates and saves these fields, the citation preview is updated, indicating what a :doc:`citation <../projects/citations>` of their
work will look like. After saving changes to any of these fields, a green text alert is shown below the "Save" button::

    Settings updated

.. todo:: Report bug: they should be required to have at least a last name.

If the user tries to navigate to another tab within the "Profile Information" page with unsaved changes, a dismissable
red alert appears in the top right of the page::

    There are unsaved changes to your settings.
    Please save or discard your changes before switching tabs.

If the user tries to click to another page, a browser alert appears, requesting confirmation::

    Confirm Navigation
    There are unsaved changes to your settings.
    Are you sure you want to leave this page?
    [Stay on this Page] [Leave this Page]

Social Information
-------------------

**Purpose:** A user's social information can be edited and shared to allow visitors to easily find the user's relevant social media account.

Social information can be edited by visiting the "Social" tab on the "Profile Information" page. There are eight social profiles
that users can connect to their OSF profile: personal site, ORCID, ResearcherID, Twitter, GitHub, LinkedIn, ImpactStory, and Google Scholar.

Each option is listed as a header above a text field with example entries entered as placeholder text.

