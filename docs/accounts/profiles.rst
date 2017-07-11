.. _profiles:

**Purpose:**  A user's public profile is a homepage for information about the user and their public OSF projects.

The contents of public profiles are visible to any OSF visitor or user. An OSF user can access their public profile by clicking
on their name in the :ref:`navigation bar <navigation-bar>` or by visiting osf.io/profile. Every user is assigned a
unique URL that can also be used to view their public profile. This URL is listed on the public profile page
below the user's name. Searching the OSF for a user and clicking on their name in the search results will direct you to their profile,
using the unique URL.

All public profiles show the user's name, their sign up date (listed as "Member Since [date]"), their public profile's unique URL,
their public projects and components, as well as their activity points. Optional information includes links to their social
network accounts, their education history, and employment history. These optional fields are shown on the top right of the user's
public profile. They are grouped into tabs; social information is shown by default, employment history is the next tab, and education
history is the final tab.

Social information is listed in rows. The social name (e.g. LinkedIn or Twitter) and logo are listed on the left and a link to the user's profile is on the right.

Employment information is listed in a table. Table headers include "institution/employer," "department/institute,"
"job title," "start date," and "end date." If no employment information is shared, the following message appears when a user clicks the "Employment" tab::
    
    Not provided

A user's public projects and components are displayed at the bottom of the profile page in the following two respective columns::
  
  Public Projects    Public Components

If the user does not have public projects, the following message will appear at the top of the "Public Projects" column::
  
  You have no public projects.
  Find out how to make your projects public [links to the help guides' landing page].
  
If the user does not have public components, the following message will appear at the top of the "Public Components" column::
  
  You have no public components.
  Find out how to make your components public [links to the help guides' landing page].

To edit profile information, users can visit their user "Settings." Alternatively, they can visit their public profile
and then click the "Edit your profile" link. The user is taken to their "Settings" page. The "Settings" page has six pages within it that the user can access using the sidebar. By default, the "Profile Information" page is selected from the sidebar and is shown on the "Settings" page. On the "Public Information" page, the "Name" tab is selected by default.

Usernames
------------

**Purpose:** Configuring their username allows the user to change how they are listed in search results, contributor lists, and in citations.

Several text fields in the "Name" tab on the "Profile Information" allow the user to configure their citation and username preferences. At the bottom of
the page are "Discard changes" and "Save" buttons.

Each time the user clicks **Save**, the "Save" button temporarily changes to "Saving," and then changes back to "Save."

The first field is titled::

    Full name (e.g. Rosalind Elsie Franklin)

This field is automatically filled in with the name the user provided when signing up for their OSF account. The user can click inside this field to edit their name.

If the user deletes the contents from the "Full name" field and clicks **Save**, a black alert appears below the "Full name" field::

    This field is required.

If the user clicks **Save** again, a red alert appears below the previous black one::
  
    This field is required.

There is no minimum character limit for the user's full name, nor is there a maximum. If the user updates their name and clicks **Save**, a temporary green alert appears below the "Save" button::

    Settings updated

The alert disappears after several seconds.

The "Full Name" field corresponds to the username. After saving changes to this field, to see the username updated on the far right of the navigation bar,
the user must refresh the page. If the username is too long, it will be shortened in the navigation bar by the insertion of an ellipsis so
that the beginning and end of the username are visible, but the middle part of the name is hidden.

Below the "Full name" field is muted text that reads::

    Your full name, above, is the name that will be displayed in your profile. To control the way your name will appear
    in citations, you can use the "Auto-fill" button to automatically infer your first name, last name, etc., or edit
    the fields directly below.
    [Auto-fill]

Below the "Auto-fill" button are the following four fields: "Given name (e.g. Rosalind)," "Middle name(s) (e.g. Elsie)," "Family name" (e.g. Franklin), "Suffix."

Clicking the **Auto-fill** button automatically fills in these fields with the user's full name as provided in the "Full name (e.g. Rosalind Elsie Franklin)" field: The first word from the "Full Name" field is added to
the "Given name" field; the last word is added to the "Family name" field; any interevening words are added to the "Middle name(s)" field; if any recognizable suffixes are listed last in the "Full name" field, such as Jr, Sr, or roman numerals, these will be aded to the "Suffix" field.
Titles are removed. Words entered in quotes are interpreted as nicknames and are removed.

If the user enters their name as "Last name, First name" then the words preceding the comma are entered in as the "Family Name."

The user can edit the four individual name fields (i.e. given, middle, family, and suffix) individually, rather than using the auto-fill function.
To do so, the user clicks inside the field and clicks **Save** to save their changes. These four fields do not affect the username—what is shown in
contributor lists and the navigation bar—but they do affect citations. Any or all of these fields can be left blank. There is no character limit.
As the user updates and saves these fields, the citation preview is updated, indicating what a :ref:`citation <citations>` of their
work will look like. After saving changes to any of these fields, a green alert appears below the "Save" button::

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

Clicking "Discard changes" after making changes prompts the following modal to appear::

    Discard changes?
    Are you sure you want to discard your unsaved changes?
    [Cancel][Discard]

Social Information
-------------------
**Purpose:** A user's social information can be edited and shared to allow visitors to easily find the user's relevant social media account.

Social information can be edited by visiting the "Social" tab on the "Profile Information" page. There are eight social profiles
that users can connect to their OSF profile: personal site, ORCID, ResearcherID, Twitter, GitHub, LinkedIn, ImpactStory, and Google Scholar.

Each option is listed as a header above a text field with example entries entered as placeholder text.

The "Save" button can be pressed any number of times—it is always active.

Clicking "Cancel" after making changes pulls up a modal that reads::

    Discard changes?
    Are you sure you want to discard your unsaved changes?
    [Cancel][Discard]

Personal Site
^^^^^^^^^^^^
**Purpose:** Personal websites can be provided to link users and visitors to a user's personal webpage.

To update the "Your website" field, the user clicks into the field and enters a web address. By default, there is an empty field for one website. Below the field is a button labeled "Add website" to add additional fields. The order of the websites can be adjusted by dragging and dropping. 

If the user enters a web address
with no protocol indicated, when they click out of the field the protocol will be automatically added. Entering a domain with no TLD (e.g. .com or .org)
or entering a TLD and no domain and attempting to save the changes by clicking the "Save" button produces red text below the button::

    Could not update settings

The text disappears after several seconds.

Entering a valid URL and saving produces green text below the "Save" button that reads::

    Settings updated

The text disappears after several seconds.

Entering special characters at invalid places in the URL (i.e. in the domain) and attempting to save the changes produces red text below the "Save"
button::

    Could not update settings

There is no validation that the webpage belongs to the user.


ORCID
^^^^^^^^
**Purpose:** ORCIDs can be provided to link users and visitors to a user's ORCID page, listing their published works.

To update the "ORCID" field, the user clicks into the field and enters their 16 digit ORCID. Hyphens can be omitted.

If the user enters less than or greater than 16 digits, the settings can still be updated. If the user enters non-digit characters, the settings can
still be updated.

.. todo:: log all of the above as a bug (also spaces are allowed)

There is no validation that the ORCID belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

ResearcherID
^^^^^^^^^^^^^
**Purpose:** ResearcherIDs can be provided to link users and visitors to a user's ResearcherID page, listing their published works.

To update the "ResearcherID" field, the user clicks into the field and enters their nine character ResearcherID. Hyphens must be included to produce
a valid link, though omitting them does not produce an error.

If the user enters less than or greater than nine characters, the settings can still be updated. If the user enters special characters, the settings can
still be updated.

.. todo:: log the above as a bug (also spaces are allowed)

If the user types "researcherid.com/rid/[user ID]" into the field, clicking away automatically removes the domain name from the field.

There is no validation that the ResearcherID belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

Twitter
^^^^^^^^
**Purpose:** Twitter handles can be provided to link users and visitors to a user's Twitter profile.

To update the "Twitter" field, the user clicks into the field and enters their Twitter handle. If the user enters special characters, the settings can still be updated.

.. todo:: log the above as a bug (also spaces are allowed)

Including or not including an '@' symbol before the Twitter handle does not impact the efficacy of the link displayed in the user's Public Profile.
If the user types "twitter.com/[handle]" the domain name is automatically removed from the field when they click away.

There is no validation that the Twitter handle belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

GitHub
^^^^^^
**Purpose:** GitHub usernames can be provided to link users and visitors to a user's GitHub profile.

To update the "GitHub" field, the user clicks into the field and enters their GitHub username. If the user enters special characters, the settings can still be updated.

.. todo:: log the above as a bug (also spaces are allowed)

If the user has connected their GitHub account to their OSF account, a blue "Import" button is visible
to the right of the text field. Users can click this button to automatically import their GitHub username. Clicking this
button changes the contents of the text field to reflect the GitHub username linked to the OSF account.

There is no validation that the GitHub account belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

If the user types "github.com/[username]" into the field and then clicks away, the domain name is automatically removed from the field.

LinkedIn
^^^^^^^^^
**Purpose:** LinkedIn usernames can be provided to link users and visitors to a user's LinkedIn profile.

To update the "LinkedIn" field, the user clicks into the field and enters their LinkedIn user ID, pub ID, or profile ID. If the user enters special
characters, the settings can still be updated.

.. todo:: should remove "linkedin.com/" if typed into the field. should also not allow special characters or spaces. log as bug.

There is no validation that the LinkedIn account belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated


ImpactStory
^^^^^^^^^^^
**Purpose:** ImpactStory usernames can be provided to link users and visitors to a user's ImpactStory profile, listing their publications and other work.

To update the "ImpactStory" field, the user clicks into the field and enters their ImpactStory username. The format for an ImpactStory username is as followers::
  
    impactstory.org/u/USERNAME

If the user enters special characters, the settings can still be updated.

.. todo:: log the above as a bug (also spaces are allowed)

If the user types "impactstory.org/[username]" into the field and then clicks away, the domain name is automatically removed from the field.

There is no validation that the LinkedIn account belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

Google Scholar
^^^^^^^^^^^^^^^
**Purpose:** Google Scholar IDs can be provided to link users and visitors to a user's Google Scholar profile, listing their publications.

To update the "Google Scholar" field, the user clicks into the field and enters their Google Scholar ID. If the user enters their ID
or copies and pastes the link to their Google Scholar profile, the resulting link will be valid. If the domain name is included in the field,
it is automatically removed when the user clicks away.

.. todo:: spaces should not be allowed in user ID

There is no validation that the Google Scholar account belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

ResearchGate
^^^^^^^^^^^^^
**Purpose:** ResearchGate profile IDs can be provided to link users and visitors to a user's ResearchGate profile. 

To update the "ResearchGate" field, the user clicks into the field and enters their ResearchGate profile ID. If the domain name is included in the field,
it is automatically removed when the user clicks away.

There is no validation that the ResearchGate account belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

Academia.edu
^^^^^^^^^^^^^
**Purpose:** Academia.edu profile IDs can be provided to link users and visitors to a user's Academia.edu profile. 

To update the "Academia" field, the user clicks into the first field and enters their Institution, then clicks into the second field and enters their profile ID. If the user does not enter one or the other field, the results are accepted anyway. The link in their profile does not work properly.

.. todo:: User should receive error message if one of academia.edu fields is blank. 

There is no validation that the Academia.edu account belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

Baidu Scholar
^^^^^^^^^^^^^
**Purpose:** Baidu Scholar IDs can be provided to link users and visitors to a user's Academia.edu profile. 

To update the "Baidu Scholar" field, the user clicks into the field and enters their Baidu Scholar profileID. If the domain name is included in the field, it is automatically removed when the user clicks away.

There is no validation that the Baidu Scholar account belongs to the user.

Saving changes produces a green text alert below the "Save" button::

    Settings updated

Employment Information
---------------------
**Purpose:** Users can share their employment information to help visitors and other users identify them and inform them of their credentials.

Employment information can be updated by clicking on the "Employment" tab on the "Profile Information" page. By default,
there are empty fields provided for one position. This is indicated by a well labeled "Position 1." The empty fields for the
user to fill in are: "Institution/Employer," "Department/Institute," "Job Title," "Start Date," and "End Date" or "Ongoing." The
"Ongoing" option is a checkbox. Below the "Ongoing" option is a green button labeled "Add another." Below this button are "Cancel" and "Save" buttons.

Clicking the "Add another" button adds new empty fields under the heading "Position 2." When multiple positions are listed,
to the right of the position number are instructions::

    [Drag to reorder]

To the right of this is a red "Remove" link.  Clicking the "Remove" link immediately removes the position and its corresponding
fields.

Users can enter any text into the first three fields of a position—"Institution/Employer," "Department/Institute," and "Job Title." If the user
tries to enter information for any field but does not fill in the "Institution/Employer" field, a popover appears over the latter that reads::

    Please fill out this field.

Once information has been entered and saved into the Position 1 fields, those fields can be edited to include different information, but
they cannot be cleared. If the user attempts to clear the fields and save the empty form, a popover will appear over the
"Institution/Employer" field that reads::

    Please fill out this field.

The "Start Date" and "End Date" fields each have a dropdown labeled "--Month--." Each of the months are listed in chronological order. The user
can select a month from the dropdown. The "Year" field to the right is a text entry box. Neither is required. If the user tries to
enter a year that is before 1900, however, a red text alert appears below the position's "Ongoing" field::

    Date must be greater than or equal to 1900.

If the user attempts to enter a year that is after the current date, a red text alert appears below the position's "Ongoing" field::

    Please enter a date prior to the current date.

If the user includes special or alphabet characters into the "Year" field, a red text alert appears below the position's "Ongoing" field::

    Please enter a valid year.

If the user selects the checkbox for the "Ongoing" field, then the "End Date" fields are removed. Unchecking the box returns the fields, empty.

Entering valid information and pressing the "Save" button at the bottom of the page produces a green text alert below the "Save" button::

    Settings updated

To reorder positions, the user can click on a position's well and drag it into a new order. All corresponding fields will follow. The
changes must be saved.

If the user makes changes and tries to click to a new tab on the "Profile Information" page, a red dismissable alert appears in the top
right corner::

    There are unsaved changes to your settings.
    Please save or discard your changes before switching tabs.

If the user tries to click to another page, a browser alert appears, requesting confirmation::

    Confirm Navigation
    There are unsaved changes to your settings.
    Are you sure you want to leave this page?
    [Stay on this Page] [Leave this Page]

Clicking "Cancel" after making changes pulls up a modal that reads::

    Discard changes?
    Are you sure you want to discard your unsaved changes?
    [Cancel][Discard]

Education Information
-----------------
**Purpose:** Users can share their education information to help visitors and other users identify them and inform them of their credentials.

Education information can be updated by clicking on the "Education" tab on the "Profile Information" page. By default,
there are empty fields provided for one position. This is indicated by a well labeled "Position 1." The empty fields for the
user to fill in are: "Institution," "Department," "Degree," "Start Date," and "End Date" or "Ongoing." Below the
"Ongoing" option is a green button labeled "Add another." Below this button are "Cancel" and "Save" buttons.

Clicking the "Add another" button adds new empty fields under the heading "Position 2." When multiple positions are listed,
to the right of the position number are instructions::

    [Drag to reorder]

To the right of this is a red "Remove" link.  Clicking the "Remove" link immediately removes the position and its corresponding
fields.

Users can enter any text into the first three fields of a position—"Institution," "Department," and "Degree." If the user
tries to enter information for any field but does not fill in the "Institution" field, a popover appears over the latter that reads::

    Please fill out this field.

Once information has been entered and saved into the Position 1 fields, those fields can be edited to include different information, but
they cannot be cleared. If the user attempts to clear the fields and save the empty form, a popover will appear over the "Institution" field that reads::

    Please fill out this field.

The "Start Date" and "End Date" fields each have a dropdown labeled "--Month--." Each of the months are listed in chronological order. The user
can select a month from the dropdown. The "Year" field to the right is a text entry box. Neither is required. If the user tries to
enter a year that is before 1900, however, a red text alert appears below the position's "Ongoing" field::

    Date must be greater than or equal to 1900.

If the user attempts to enter a year that is after the current date, a red text alert appears below the position's "Ongoing" field::

    Please enter a date prior to the current date.

If the user includes special or alphabet characters into the "Year" field, a red text alert appears below the position's "Ongoing" field::

    Please enter a valid year.

If the user selects the checkbox for the "Ongoing" field, then the "End Date" fields are removed. Unchecking the box returns the fields, empty.

Entering valid information and pressing the "Save" button at the bottom of the page produces a green text alert below the "Save" button::

    Settings updated

To reorder positions, the user can click on a position's well and drag it into a new order. All corresponding fields will follow. The
changes must be saved.

If the user makes changes and tries to click to a new tab on the "Profile Information" page, a red dismissable alert appears in the top
right corner::

    There are unsaved changes to your settings.
    Please save or discard your changes before switching tabs.

If the user tries to click to another page, a browser alert appears, requesting confirmation::

    Confirm Navigation
    There are unsaved changes to your settings.
    Are you sure you want to leave this page?
    [Stay on this Page] [Leave this Page]

Clicking "Cancel" after making changes pulls up a modal that reads::

    Discard changes?
    Are you sure you want to discard your unsaved changes?
    [Cancel][Discard]
