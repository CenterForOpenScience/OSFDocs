**Purpose:** Sharing a preprint helps the user quickly disseminate their work and receive feedback from peers without having to wait for journal peer review. 

Anyone with an OSF account can create a preprint and upload it to OSF Preprints or a community preprint server. A user can upload a new preprint or turn an existing OSF project or component into a preprint. 

When a user uploads a new preprint (and does not use an existing project or component), an OSF project is automatically created to connect to it. The connected OSF project allows the user to upload supplemental files to their preprint. When a user turns an existing OSF project or component into a preprint, the user can add supplemental files to that project and access the files that they previously added to that project.

A user can access their preprint through their OSF project or component. On the project or component’s Overview page, there will be an alert saying “This [project] [component] represents a preprint. Learn more (this links to preprints help guides] about how to work with preprints.” A user can also access their preprint through the “My Projects” tab and  clicking “All my preprints” from the left sidebar and then clicking the preprint they want to view. 

A user can edit their preprint and upload new versions. Once a preprint is shared, it should be assumed that it will always be public and available.

OSF Preprints
-------------
**Purpose:** To search for preprints, upload a preprint, and access the preprint community servers.

To navigate to the OSF Preprints landing page, the user clicks the **OSF Home** tab from the navigation bar and then clicks **OSF Preprints** from the drop-down menu.

On the OSF Preprints landing page, there is a search field to search for preprints, a green [Add a preprint] button below the search field, and a section titled "Browse by subject" that shows the 10 top-level subject areas provided by Bepress (see the `Search Preprints`_ section).

In the top right, there's a toolbar with the following actions:

* An "Add a preprint" tab that takes the user to the "Add a preprint" page.
* A "Search" tab that takes the user to the Preprint Archive Search page.

The following tabs appear in the navigation bar when the user is logged out OSF Preprints:

* OSF Preprints. Clicking this tab causes a drop-down menu to appear with the following options: 

    * OSF Home: Clicking this link takes the user to their dashboard. 
    * OSF Preprints: Clicking this link takes the user to the OSF Preprints landing page https://osf.io/preprints/.
    * OSF Registries: Clicking this link takes the user to the OSF Registries landing page https://osf.io/registries/.
    * OSF Meetings: Clicking this link takes the user to the OSF for Meetings landing page https://osf.io/meetings/.
    
* Add a preprint: Clicking this link takes the user to the sign-in page https://accounts.osf.io/login?service=https%3A%2F%2Fosf.io%2Flogin%2F%3Fnext%3D%252Fpreprints%252Fsubmit.
* Search: Clicking this link takes the user to the Preprints Discover page https://osf.io/preprints/discover/.
* Support: Clicking this link takes the user to the landing page for the preprints help guides http://help.osf.io/m/preprints/.

* Sign Up: Clicking this tab takes the user to the :ref:`Create a free account page <sign-up>` where the user needs to fill out a form to create an OSF account.
* Sign In: Clicking this tab takes the user to the :ref:`OSF sign-in page <login>`. After logging in, the user is taken to the OSF Preprints landing page.

The community preprint servers are listed with their logos below the search field. Clicking on a community preprint server logo takes the user to that preprint server's landing page.

When logged in, the navigation bar is the same except that the "Sign up" and "Sign in" buttons are replaced with the user drop-down menu.

Community Preprint Servers
--------------------------
**Purpose:** To search for preprints within and upload preprints to a given preprint server.

When a user navigates to a community preprint server, the landing page is the same as OSF Preprints, except for different color schemes and different actions in the :ref:`navigation bar <navigation-bar>`. The top-level subject areas highlighted on a community preprint server's landing page vary in subject and number by each provider. If the preprint provider has chosen their own custom taxonomy as well as highlighted subjeccts, the "Browse by subjects" section is instead titled "Browse by featured subjects." When the section is "Browse by featured subjects," a link is included below the title to "See all subjects available," that, when clicked, takes the user to the "Discover" page to view all subjects available.

The following tabs appear in the navigation bar when the user is logged out:

* "Add a preprint": Clicking this tab takes the user to the :ref:`OSF sign-in page <login>`.
* "Search". Clicking this tab takes the user to the preprint server's Discover page https://osf.io/preprints/preprintserver/discover.
* "Sign Up". Clicking this tab takes the user to the :ref:`Create a free account page <sign-up>` where the user needs to fill out a form to create an OSF account in order to be able to upload a preprint to the community preprint server. 
* "Sign In". Clicking this tab takes the user to the :ref:`OSF sign-in page <login>`. After logging in, the user is taken to their OSF dashboard.

When logged in, the navigation bar is the same except that it contains a "My OSF Projects" tab which, when clicked, takes the user to https://osf.io/myprojects/ and the "Sign up" and "Sign in" buttons are replaced by the user drop-down menu.

.. _adding-preprint: 

Adding a Preprint
-----------------
**Purpose**: To submit a preprint, the user must upload their file and fill out required information related to their preprint in the following form.
  
Clicking the green "Add a preprint" button takes the user to the Add Preprint page where the user must follow five steps in order to share a preprint:

* Upload: The user adds their preprint file and enters a preprint title.
* Discipline: The user adds disciplines to their preprint.
* Basics: The user adds a license and includes an abstract of at least 20 characters.
* Authors: The user adds coauthors, but can also choose to be the only author.
* Submit: The user uploads their preprint to the preprint server.

After a user clicks "Save and continue" in each widget, a confirmation message appears in to top right corner of the widget::
  
    Changes Saved!

A user must complete the required steps within each widget before they can upload their preprint. Abandoning the preprint by navigating away from the page will create the OSF project, but will not create the preprint. If the user navigates away from the page, a browser alert appears, confirming that the user wants to leave the page. This alert gets triggered when the user is on the "Upload" step.
    
Upload
^^^^^^
**Purpose**: Allows the user to upload their preprint file.

There is an additional section at the start of the preprint form for OSF Preprints: "Select a preprint service." This widget is not available on community preprint services. This widget gives users the choice to upload their preprint to OSF Preprints or a community preprint service. This widget consists of a carousel showing the preprint service logos that the user must select to choose a preprint service. The "OSF Preprints" logo is selected by default. Hovering over a logo shows the name of the preprint provider in a tooltip. The user can click the navigational arrows to navigate through the carousel. 

If the user clicks inside another widget before saving their changes, a temporary, red error message appears in the top right of the page::
  
    Please select a preprint service before continuing

At the bottom of the widget are "Discard changes" and "Save and continue" buttons. The "Discard changes" button is disabled. It becomes enabled if the user clicks **Save and continue**, reopens the widget, and selects a different preprint service. Clicking **Discard changes** re-selects the first preprint service from the list, and disables the "Discard changes" button. Clicking **Save and continue** closes the "Select a preprint service" widget, where a temporary, green confirmation message appears in the top right::
  
    Changes Saved!
    
The "Select a preprint service" widget shows the service that was selected::
  
    Preprint service: <preprint service name>

Once the "Select a preprint service" widget closes, the "Upload" widget opens (this widget is auto-expanded for community preprint services).

If the user does not complete the upload widget and clicks inside another widget, has not completed the steps within a widget and clicks inside another widget, an alert will appear in the top right corner of the Add preprint page::

    Please complete upload section before continuing
    
The alert has an animated reverse progress bar that functions as a timer. When the animation completes, the alert disappears, and the Upload widget remains open.

The widget contains two options for adding a preprint file::

    [Upload new preprint][Connect preprint to existing OSF project]

.. _new-preprint:

**Upload new preprint**

When the user clicks "Upload new preprint," a box in which the user uploads their preprint file appears with instructions that read::
      
    Drop preprint file here to upload

There are two buttons to the bottom right of the file box::
    [Back][Save and continue]

The user cannot click "Save and continue" until they have uploaded their file and entered a title for their preprint. If the user tries to click "Save and continue," a hazard symbol appears on the tail of the cursor, and the user is unable to click the button to progress to the next widget.

The user can add their preprint file in two different ways:

1. The user can drag and drop their file into the file box
2. The user can click inside (double click for Windows) the file box to open a dialog box from which they can select and upload their file. The dialog box will close when the user clicks the "Choose" button. 

After the user adds their preprint file, the file appears in the middle of the file box, where the preprint's filename and the file size are listed. The user has the option to upload a new preprint file to replace the one they previously added. Below the filename and file size, the instructions in the box now read::
    
    Click or drag another preprint file to replace

After uploading the preprint file, the preprint title field appears below the file box, with instructions that read::
    
    Enter preprint title
    
The user must enter a title for their preprint into the field before they can continue to the next widget.

If a user clicks inside the title field without entering a title, and then clicks elsewhere within the widget, a growlbox appears below the title field that reads::
  
      Title can't be blank

After entering a title, the user can click "Save and continue" or press the **return** key (Mac) or the **enter** key (Windows) on their computer to continue on to the "Discipline" widget.

An alert confirming the upload will appear in the top right of the page::
  
    Preprint file uploaded!

This alert has an animated reverse progress bar that functions as a timer. When the animation completes, the alert disappears.

**Connect preprint to existing OSF project**

Clicking the Connect Preprint to existing OSF project brings up the Choose Project box::

    Click to select
    [drop-down selections][a list of the user's OSF projects and components]
    **The list of projects appearing in the selector are projects and components for which you have admin access. Registrations are not included here.
    
Clicking inside the menu opens a drop-down menu with the following helper text::
  
    Type to search.

Typing into the field, shows the following loading message::
  
    Loading options...
    
A maximum of 7 projects are shown at a time from the menu. If there are more than 7, the user can scroll through the menu.
    
After the user types in and selects a project or component from the drop-down list, the Choose Project section closes, and the Choose File section appears below it. The Choose Project section is still viewable and accessible to the user. The box reads::

    Choose Project
    [project or component name]
    *Click to Edit*

The user can click anywhere inside the Choose Project section to open it. When reopening the box, the user can choose a different project or component.

In the Choose File section two options appear for uploading a preprint file to the OSF project or component::
  
    [Upload preprint][Select existing file as preprint]

If the user clicks "Upload preprint," the file box appears with instructions that read::
  
    Drop preprint file here to upload
    
After the user uploads their preprint file, the file box briefly shows the filename and file size before the Choose File section closes, and the Organize section appears below it.

If the user clicks "Select existing file as preprint," the Choose File section will show the files uploaded to the project or component's OSF storage (files uploaded to storage add-ons are not available to use as preprints).

After the user chooses the file they want to use for their preprint, the Choose File section will close and the Organize box will appear below it.

The Choose File section is still viewable and accessible to the user. The box reads::

    Choose File (this is a link that the use can click to expand the box)
    [filename]
    *Click to Edit*

The user can click anywhere inside the Choose File section to open it. When reopening the section, the user can choose a different file from OSF storage to use for their preprint.
    
After the user has finished choosing and uploading their preprint file, the Organize section will appear.

If the user previously chose to upload their preprint to an OSF project, the Organize secion will display two options for connecting a preprint to a project::
  
    You can organize your preprint by storing the file in this project or in its own new component. If you select 'Make a new component', the prperint file will be stored in a new component inside this project. If you  select 'Use the current project', the preprint file will be stored in this project. If you are unsure, select 'Make a new component'.
    [Make a new component][Use the current project]
    
If the user clicks "Make a new component," the Finalize Upload section will appear below the Choose Project, Choose File, and Organize sections::

    Enter preprint title (this is a field)
    You have selected and organized your preprint file. Clicking "Save and continue" will immediately make changes to your OSF project. You will not be able to delete your Preprint file, but you will be able to update or modify it
    [Save and continue]

The user cannot click "Save and continue" until they have entered a preprint title.
    
If the user clicks "Use the current project," a growlbox will appear below the two options with an exclamation point icon to the left of the message::
  
    Your project details will be saved as you continue to work on this form.
    Changes you make on this page are saved immediately. Create a new component under this project to avoid overwriting its details.
    [Create a new component][Continue with this project]
    
If the user clicks "Create a new component," the Finalize Upload section will appear below the Choose Project, Choose File, and Organize sectioms where the user will need to enter a preprint tile before moving on to the next widget::
  
  Enter preprint title (this is a text field)
  You have selected and organized your preprint file. Clicking "Save and continue" will immediately make changes to your OSF project. You will not be able to delete your Preprint file, but you will be able to update or modify it
  [Save and continue]
  
The user cannot click "Save and continue" until they have entered a preprint title.

If the uesr clicks "Continue with this project," the Finalize Upload box will appear below the Choose Project, Choose File, and Organize boxes, where the user will need to enter a preprint tile before moving on to the next widget::
  
  Enter preprint title (this is a text field)
  You have selected and organized your preprint file. Clicking "Save and continue" will immediately make changes to your OSF project. You will not be able to delete your Preprint file, but you will be able to update or modify it
  [Save and continue]

The user cannot click "Save and continue" until they have entered a preprint title.

If the user previously chose to upload their preprint to a component, the Organize box will display two options for connecting a preprint to a component::
  
    You can organize your preprint by storing the file in this component or in its own new component. If you select ‘Make a new component’, the preprint file will be stored in a new component inside this component. If you select ‘Use the current component’, the preprint file will be stored in this component. If you are unsure, select ‘Make a new component’.
    [Make a new component][Use the current component]
        
If the user clicks "Make a new component," the Finalize Upload section will appear below the Choose Project, Choose File, and Organize sections::

    Enter preprint title (this is a text field)
    You have selected and organized your preprint file. Clicking "Save and continue" will immediately make changes to your OSF project. You will not be able to delete your Preprint file, but you will be able to update or modify it
    [Save and continue]

The user cannot click "Save and continue" until they have entered a preprint title.

If the user clicks "Use the current component," a growlbox will appear below the two options with an exclamation point icon to the left of the message::

  Your component details will be saved as you continue to work on this form.
  Changes you make on this page are saved immediately. Create a new component under this component to avoid overwriting its details.
  [Create a new component][Continue with this component]

If the user clicks "Create a new component," the Finalize Upload section will appear below the Choose Project, Choose File, and Organize sectionz, where the user will need to enter a preprint tile before moving on to the next widget::
  
  Enter preprint title (this is a text field)
  You have selected and organized your preprint file. Clicking "Save and continue" will immediately make changes to your OSF project. You will not be able to delete your Preprint file, but you will be able to update or modify it
  [Save and continue]
  
The user cannot click "Save and continue" until they have entered a preprint title.

If the user clicks "Continue with this component," the Finalize Upload section will appear below the Choose Project, Choose File, and Organize sections, where the user will need to enter a preprint tile before moving on to the next widget::
  
  Enter preprint title (this is a text field)
  You have selected and organized your preprint file. Clicking "Save and continue" will immediately make changes to your OSF project. You will not be able to delete your Preprint file, but you will be able to update or modify it
  [Save and continue]
  
The user cannot click "Save and continue" until they have entered a preprint title.

When the user enters a preprint title and clicks "Save and continue," the Upload widget closes, and the Discipline widget expands.

The user can return to the Upload widget to make changes at any point throughout the preprint upload process. 

When closed, the Upload widget appears as follows::
  
    *Preprint location:* [project or component name]
    *Preprint file:* [file name] *(Version: [number]*
    *Preprint title:* [preprint title]
    *Click to Edit*

When returning to the Upload widget, the user can click inside the the widget to open it. The user can only make changes to the preprint file (can upload a new file as long as it has the same name as the previous file) and edit the preprint title. The user cannot change their OSF project or component. At the bottom of the Upload widget, there is a message and two buttons that read::
  
    Edits to this preprint will update both the preprint and the OSF project.
    [Discard changes][Save and continue]
  
The user cannot click "Discard changes" unless they have made changes to the preprint file or title. Once the user has made changes, they can click this button or click within whichever widget they are currently working on to discard the changes they made to the Upload widget.
    
Discipline
^^^^^^^^^^
**Purpose:** Allows the user to add disciplines and subdisciplines (optional) to their preprint to make it more discoverable.

The taxonomy for the disciplines comes from BePress.

At the top of the Discipline widget, there is a message that reads::
  
    Select a discipline and subdiscipline, if relevant. Add more by clicking on a new discipline or subdiscipline.

There are three columns that sort the hierarchies of the disciplines and subdisciplines (aka the *discipline chooser*).

There are two buttons in the bottom right of the widget::
  
    [Discard changes][Save and continue]

In the left column, all of the disciplines available in OSF Preprints are listed::

    Architecture
    Arts and Humanities
    Business
    Education
    Engineering
    Law
    Life Sciences
    Medecine and Health Sciences
    Physical Sciences and Mathematics
    Social and Behavioral Sciences
    
When selecting a discipline, the user must click on a top-level discipline from the left column, and it will be added to their preprint. Their disciplines will appear above the discipline chooser.

When selecting a subdiscipline, the user must click on a top-level discipline to show its subsdisciplines in the middle column. The user can click on a subdiscipline from the middle column to show its subdisciplines in the right column.

To remove disciplines from their preprint, the user can click the white "x" to the right of their added disciplines.

The user can click inside any other widget prior to adding disciplines; however, the user must add at least one discipline to their preprint before they can upload it.

Until the user adds a discipline, they will not be able to click "Discard changes" or "Save and continue."

When the user clicks "Save and continue," the Discipline widget will close, and the Basics widget will open.

The user can return to the Discipline widget to make changes at any point throughout the preprint upload process. 

Basics
^^^^^^
**Purpose:** The Basics widget is where the user can add a license, DOI, tags, and an abstract to their preprint.

In the bottom right of the Basics widget, there are two buttons::
  
    [Discard changes][Save and continue]

These buttons are disabled until the user has filled the required fields. The required sections and fields for this widget are:

* Choose a license
* Abstract

If the user chooses the No license option from the Choose a license drop-down menu, the two fields that appear below the menu are also required:
* Year
* Copyright Holders

**License**

In the license section, the user has the following options::
    
    **Choose a license:** (required)
    [Drop-down selections]
    License FAQ (this links to the license FAQ page)
    Show full text (clicking this shows an explanation of the license selected)
    Hide full text (this appears in place of Show full text when the user clicks to view the text)

The licenses available vary by preprint provider. OSF Preprints offers No license, CC0 1.0 Universal, and CC-By Attribution 4.0 International. If the user selects "No license" from the drop-down menu, the "Year" and "Copyright Holders" fields appear below the menu.

These two fields are required. In the "Year" field, the current year is listed automatically. If the user deletes the current year - e.g. "2017"- from the field, the year will reappear automatically in the field. To enter a different year, the user can delete the last 1-3 numbers and type in the correct year from there. If the user deletes the first number- e.g. "2"- the year will reappear automatically in the field.

There is an option to "Apply this preprint license to my OSF project." The user can select "Yes" or "No" to either extend or not extend the preprint license to their OSF project. "Yes" is selected automatically. Note that if the user selects "No license" option from the drop-down menu, they can choose to extend this license to their OSF project, as well.

**The DOI section**
A DOI is automatically generated for a preprint upon submission, and is minted through Crossref. Each preprint provider has a unique DOI prefix. If the  preprint has been published in a journal, the user can enter the peer-reviewed DOI into the "Peer-reviewed publication DOI (optional)" field.
    
If the user enters an invalid DOI, a red error message appears below the field::
  
    Please use a valid DOI
    
The error message disappears when the user removes the invalid DOI.

**Original Publication Date**

If their preprint has been previously published, the user can include the publication year, month, and day into this field. Clicking inside this field opens a calender picker from which the user can select and apply the publication date.

This publication date will appear in the preprint's metadata, as well as in the preprint citations.

**The Keywords section**
    
In the Keywords section, the user can add tags to their preprint in the text box that has the instructions::
  
    Add a tag

**The Abstract section**

In the Abstract section, the textbox has instructions that read::
  
    Add a brief summary of your preprint

If the user starts typing into the Abstract textbox and deletes what they have written, a growlbox will appear below the textbox that reads::
  
    Abstract can't be blank

When the user starts typing their abstract and the content is--so far--less than 20 characters long, a growlbox will appear below the textbox that reads::
  
    Abstract is too short (minimum is 20 characters)

The growlbox disappears once the user has typed 20 characters. When the abstract is less than 20 characters, the textbox is outlined in blue, but when the abstract reaches 20 characters and more, the textbox is outlined in green.

When the user has filled out all of the required sectons and fields, they can either click [Discard changes][Save and continue]

Clicking "Discard changes" will cause a growlbox to appear below the Abstract textbox that reads::
  
    Abstract can't be blank

**Finishing the Basics Widget**
 
In the event that the user chooses "No license" from the drop-down menu and fills out the "Year" and "Copyright Holders" fields as their last steps before they finish the Basics widget, the user can press the **return** key (Mac) or the **Enter** key (Windows) on their computer to close the Basics widget and open the Authors widget.

The user can also click [Save and continue] to close the Basics widget and open the Authors widget.

This is how the widget appears when closed::
  
    Basics (this is a link that the user can use to click to open the widget; the user can click anywhere inside the widget to open it)
    License: [license type]
    DOI: [DOI] (or) None (if no DOI is provided)
    Abstract:
    [abstact content]
    Click to Edit
    
The user can click inside the Basics widget to open it and make changes at any point throughout the preprint upload process. When the user reopens the Basics widget, they cannot click "Discard changes" unless they have made changes to the information they previously provided in the widget. Once the user has made changes to the information, the user can click "Discard changes."

Authors
^^^^^^^
**Purpose:** The Authors widger is where the user can add and reorder their preprint authors.

A user can search for and add authors to their preprint.

At the top of the Authors widget, there are instructions that read::
  
    Add preprint authors and order them appropriately. All changes to authors are saved immediately. Search looks for authors that have OSF accounts already. Unregistered users can be added and invited to join the preprint.

**Search for an author:** To add an author, the user must type the author's name into the search field. The search field has a message within it that reads::
    
    Search by name [magnifying glass symbol]

When the user types the author's name into the search field, the user can either press enter on their keyboard or click the magnifying glass symbol.

Once the user enters their search query, a gray box appears below the search field that reads::
  
    Can't find the user you're looking for?
    [Add author by email address]

If the author does not have an OSF account, a Results section will appear below the gray box that reads::
  
    No results found.

If the user clicks the "Add author by email address" button, the gray box will disappear, and the Add author by email section will appear below the search field with the following form::
  
    Add author by email
    Full Name
    [full name field] Full name
    Email
    [email field] Email
    We will notify the user that they have been added to your preprint.
                                                          [Cancel][Add]
                                                
If the user clicks inside the Full Name and Email fields without entering information and then clicks outside of these fields, the following growlbocs appear below each respective field::
  
    Full Name can't be left blank (the full name field)
    This field can't be blank (the email field)

If the user enters an author's name that is less than three characters, a growlbox appears below the Full Name field that reads::
  
    Full Name is too short (minimum is 3 characters)

If the user enters an invalid email address into the Email field, a growlbox appears below the Email field that reads::
  
    This field must be a valid email address
  
Until the user enters the information correctly into these fields, the fields will be outlined in blue, and the green "Add" button will be unclickable. The user can, however, click the "Cancel" button.

When the user enters in the information correctly, the fields will be outlined in green, and the user can click the green "Add" button.

When the user clicks the green "Add" button, the author will be added to the Authors section on the right side of the widget below the user's name.
  
If the author who the user searches for has an OSF account, a Results section will appear below the gray box, and the author's name will be listed in the Results section with a green "Add" button to the right of their name.

When the user clicks the green "Add" button, the author will be added to the Authors section on the right side of the widget below the user's name.

**Reorder Authors:**
If the user adds more than one author, each author will be added according to the order in which the user adds them.

At the top of the Authors section, there are instructions that read::
  
    Drag and drop authors to change authorship order.

In each author row, there are four columns: Name, Permissions, Citation, and a red "Remove" button.

To the left of each author row, there is a hamburger that the user can click to drag and drop the authors into a different order.

Under the Permissions column, each author (except for the user uploading the preprint, who is listed as the administrator) has a Permissions menu. In the Permissions menu, the Read + Write permissions are selected automatically. The user can click inside the menu to open a pop-over from which the user can assign different permissions to their authors. The permissions options are: Read, Read + Write, and Administrator. There is a question mark to the right of the Permissions header. When the user hovers over the question mark, a tooltip appears that explains the permissions levels::
  
    Read
        *View a preprint
    Read + Write
        *Read privileges
        *Add and configure preprint
        *Add and edit content
    Administrator
        *Read and write privileges
        *Manage authors
        *Public-private settings

Under the Citation column, there is a checkbox in each author's row. The checkbox is selected automatically. When the checkbox is selected, the corresponding author will appear in citations. When the checkbox is unchecked, the author will not be included in citations but can read and modify the preprint, according to their permissions. There is a question mark below the Citation header. When the user hovers over the question mark, a tooltip appears that explains what checking and unchecking the Citation box means::
  
    Only checked authors will be included in preprint citations. Authors not in the citation can read and modify the preprint as normal.

Clicking the red "Remove" button will delete the author from the preprint. The author will not aware that they were added or deleted.

When the user is finished filling out the Authors widget, they can click the blue "Next" button in the bottom right of the widget.

After the user clicks the "Next" button, the widget will close and the Submit widget will open. 

The user can click inside the Authors widget to make changes to the information after the user has continued on to the next widget. When the user reopens the Authors widget, they can click the "Next" button at any time, with or without making changes to the information within the widget.

Submit
^^^^^^

At the top of the Submit widget, there are instructions that read::
  
    When you create this preprint, it will be assigned a DOI and become publicly accessible via <preprint server>. The preprint file cannot be deleted, but it can be updated or modified. The related OSF project can be used to manage supplementary materials, appendices, data, or protocols for your preprint.

    By creating this preprint, you confirm that all contributors agree with sharing it and that you have the right to share this preprint.
    [Cancel][Create]
    
If the preprint server uses post-moderation, the instructions will read::
  
    When you submit this paper, it will be assigned a DOI. The paper file cannot be deleted, but it can be updated or modified. The related OSF project can be used to manage supplementary materials, appendices, data, or protocols for your paper.

    By creating this paper, you confirm that all contributors agree with sharing it and that you have the right to share this paper.

    <preprint server> uses post-moderation. Therefore, your paper will become publicly accessible after creation and will only become private if rejected by a moderator.  
    [Cancel][Create]

If the preprint server uses pre-moderation, the instructions will read::
  
  When you submit this preprint, it will be assigned a DOI. The preprint file cannot be deleted, but it can be updated or modified. The related OSF project can be used to manage supplementary materials, appendices, data, or protocols for your preprint.

  By submitting this preprint, you confirm that all contributors agree with sharing it and that you have the right to share this preprint.

  <preprint server> uses pre-moderation. Therefore, your preprint will not become publicly accessible until a moderator accepts the submission.
  [Cancel][Submit]


If the user has not finished all required sections, and they click the **Create** button, a message will appear below the instructions that reads with a list of the unfinished sections::
  
    The following section(s) must be completed before sharing this preprint.
    <widget title(s)>
    
The user could skip the Author widget (either by not clicking inside the widget at all or by not clicking the **Next** button) and submit their preprint without any message or growlbox appearing.

When the user is ready to submit their preprint, they can click the blue "Share" button. Clicking "Share" causes a modal to appear::

    Create Preprint
    Once this preprint is made public, you should assume that it will always be public. Even if you delete it, search engines or others may access the files before you do so.
    [Cancel][Create preprint]
    
Clicking "Cancel" will return the user to the "Add Preprint" page with all of their preprint upload information still intact.

Clicking the final button will take the user directly to the Preprint Detail page. 

The authors will receive an email notification that they have been added as authors to the preprint. If the recipient is a non-registered user, they will receive the following email notification::
  
   Hello [username],
   
   You have been added by [username] as a contributor to the preprint “[preprint name]” on the Open Science Framework. To set a password for your account, visit:
   
   https://osf.io/user/GUID/GUID/claim/?token=[string]
   
   Once you have set a password, you will be able to make contributions to “[preprint name]” and create your own preprints and projects. You will automatically be subscribed to notification emails for this project. To change your email notification preferences, visit your project or your user settings: https://staging.osf.io/settings/notifications/
   To preview “Measurements of Newtonian Fluids” click the following link: https://osf.io/GUID/

   (NOTE: if this project is private, you will not be able to view it until you have confirmed your account)

   If you are not [username] or you are erroneously being associated with “[preprint name]” then email contact@osf.io with the subject line “Claiming Error” to report the problem.
   
If the recipient is a registered user, they will receive the following email notification::
    
    Hello [username],
    [username] has added you as a contributor to the preprint “[preprint name]” on the Open Science Framework: https://osf.io/GUID/

    You will be automatically subscribed to notification emails for this project. To change your email notification preferences, visit your project or your user settings: https://staging.osf.io/settings/notifications/

    If you are erroneously being associated with “[preprint name],” then you may visit the project's “Contributors” page and remove yourself as a contributor.

Upon submitting the preprint, the user will receive the following call-to-action email titled "Confirmation of your submission to OSF Preprints."

For OSF Preprints::
      
  Hello <user name>,

  Your preprint <preprint title> has been successfully submitted to OSF Preprints.

  Now that you've shared your preprint, take advantage of more OSF features:
  * Upload supplemental, materials, data, and code to the OSF project associated with your preprint. Learn how <http://help.osf.io/m/preprints/l/685323-add-supplemental-files-to-a-preprint>
  * Preregister your next study. Read more <http://help.osf.io/m/registrations/l/524205-register-your-project>
  * Or share on social media: Tell your friends through:   twitter	 facebook	 LinkedIn
  
  Learn more about OSF Preprints or OSF.

  Sincerely,
  Your OSF team
  
In the last line of the email, "OSF Preprints" and "OSF" link to the "OSF Preprints" landing page and OSF dashboard, respectively.

For community preprints services::
    
  Hello <user name>,

  Your preprint <preprint title> has been successfully submitted to <preprint service>.

  Now that you've shared your paper, take advantage of more OSF features:
  * Upload supplemental, materials, data, and code to the OSF project associated with your paper. Learn how <http://help.osf.io/m/preprints/l/685323-add-supplemental-files-to-a-preprint>
  * Preregister your next study. Read more <http://help.osf.io/m/registrations/l/524205-register-your-project>
  * Or share on social media: Tell your friends through:   twitter	 facebook	 LinkedIn
  
  You will receive a separate notification informing you of any status changes.
  Learn more about <preprint service> or OSF.


  Sincerely,
  Your <preprint service> and OSF teams

In the last line of the email, the "preprint service" and "OSF" link to the preprint service landing page and OSF dashboard, respectively.

Preprint Detail Page
--------------------
 **Purpose:** The "Preprint Detail" page is the main page where the user reads and downloads a given preprint.

The preprint title appears at the top of the "Preprint Detail" page. Below the title is a list of the co-authors on the preprint. If a co-author is a registered contributor, their name will be linked to their OSF profile page. The date when the preprint was shared and the date when the preprint was last edited are listed below the preprint's title.

On the left half of the page, the preprint appears in an MFR, below which a "Download preprint" button, and the supplemental files (if the user has uploaded any) are shown. The preprint file will also be listed below the MFR but only in the event that there are supplemental files.

On the right half of the page, the preprint's abstract, license, disciplines, Preprint DOI (when clicked takes the user to the "Preprint Detail" page), Peer-Review Publication DOI (optional - appears if the user's preprint has been previously published and they have provided it in the metadata when uploading their preprint), Original Publication Date, tags, and citation styles (MLA, APA, and Chicago) are listed.

It can take up to 24 hours for a preprint to be minted, in which case the DOI is listed, but not linked, and the following message appears below the Preprint DOI:
  
    DOIs are minted by a third party, and may take up to 24 hours to be registered

If the user has entered a peer-reviewed DOI and an original publication date, these metadata will appear in the citations (not all citation styles use DOIs). If the user has not entered a peer-reviewed DOI, the preprint DOI is used in the citations.

If an abstract is long, there will be a **See more** button below the abstract that the user can click to expand the remaining text. When the abstract is expanded, the button changes to **See less**. When the user clicks the **See less** button, the abstract shrinks back to its shorter length, and the **See more** button returns.

In the top right of the Preprint Detail page, there is a gray box that includes a series of actions for downloading and sharing a preprint::

   [Download preprint], the number of downloads [Downloads: x], and social media sharing options

At the bottom right of the page, there is a gray box that reads::
     
    The project for this paper is available on the OSF
   [Visit project] (links to the OSF project connected to a preprint)

Admins can see a green "Edit preprint" button in the top right of the Preprint Detail page. Contributors with read access or read+write acces and visitors to a Preprint Detail page cannot see this button.
   
Moderated preprints
^^^^^^^^^^^^^^^^^^^
**Purpose**: Preprints will be pending until accepted or rejected by a moderator. Banners help inform the user of the state of their preprint. These banners are only visible to the preprint authors and moderator.

If the user submitted to a preprint service that uses pre-moderation, they will receive a confirmation email upon submission titled "Confirmation of your submission to <preprint service>"::
  
  Hello Rebecca Rosenblatt,

  Your preprint <preprint title> has been successfully submitted to <preprint service>.

  <preprint service> has chosen to moderate their submissions using a pre-moderation workflow, which means your submission is pending until accepted by a moderator. You will receive a separate notification informing you of any status changes.

  Learn more about <preprint service> or OSF.

  Sincerely,
  Your <preprint service> and OSF teams

In the last line of the email, the "preprint service" and "OSF" link to the preprint service landing page and OSF dashboard, respectively.

The premoderated preprint will be private until a moderator accepts or rejects it. While the preprint is pending, a yellow banner will appear at the top of the page::
  
    Pending: <preprint service> uses pre-moderation. this preprint is not publically available or searchable until approved by a moderator.

If the user submitted to a preprint service that uses post-moderation, the user will receive a confirmation email upon submission titled "Confirmation of your submission to <preprint service>"::
  
  Hello <user name>,

  Your preprint <preprint title> has been successfully submitted to <preprint service>.

  <preprint service> has chosen to moderate their submissions using a post-moderation workflow, which means your submission is public and discoverable, while still pending acceptance by a moderator. You will receive a separate notification informing you of any status changes.

  Learn more about <preprint service> or OSF.

  Sincerely,
  Your <preprint service> and OSF teams

In the last line of the email, the "preprint service" and "OSF" link to the preprint service landing page and OSF dashboard, respectively.
  
The preprint will be public upon submission. Until a moderator accepts or rejects the preprint, a blue banner will appear at the top of the page::

    Pending: OSF uses post-moderation. This preprint is publically available and searchable but is subject to removal by a moderator.

If the moderator accepts the preprint, a green banner will appear at the top of the preprint page::
  
    Accepted: <preprint service> uses [pre][post]-moderation. This preprint has been accepted by a moderator and is publically available and searchable.

The user will receive a call-to-action email titled "OSF Notifications".

For pre-moderation::
  
  Hello <user name>,

  Your submission <preprint title>, submitted to <preprint service> has been accepted by the moderator and is now discoverable to others.

  Now that you've shared your preprint, take advantage of more OSF features:
  * Upload supplemental, materials, data, and code to the OSF project associated with your preprint. Learn how <http://help.osf.io/m/preprints/l/685323-add-supplemental-files-to-a-preprint>
  * Preregister your next study. Read more <http://help.osf.io/m/registrations/l/524205-register-your-project>
  * Or share on social media: Tell your friends through:   twitter	 facebook	 LinkedIn
  
  Learn more about <preprint service> or OSF.

  Sincerely,
  Your <preprint service> and OSF teams
  
For post-moderation::
  
  Hello <user name>,

  Your submission <preprint title>, submitted to <preprint service> has been accepted by the moderator and remains discoverable to others.

  Now that you've shared your preprint, take advantage of more OSF features:
  * Upload supplemental, materials, data, and code to the OSF project associated with your thesis. Learn how <http://help.osf.io/m/preprints/l/685323-add-supplemental-files-to-a-preprint>
  * Preregister your next study. Read more <http://help.osf.io/m/registrations/l/524205-register-your-project>
  * Or share on social media: Tell your friends through:   twitter	 facebook	 LinkedIn
  
  Learn more about <preprint service> or OSF.

  Sincerely,
  Your <preprint service> and OSF teams
  
In the last line of the email, the "preprint service" and "OSF" link to the preprint service landing page and OSF dashboard, respectively.
      
If the moderator rejects the preprint, the user will receive an email notification titled "OSF Notifications"::
  
  Hello <user name>,

  Your submission <preprint title>, submitted to <preprint service> has not been accepted. Contributors with admin permissions may edit the preprint and resubmit, at which time it will return to a pending state and be reviewed by a moderator.

  Learn more about <preprint service> or OSF.

  Sincerely,
  Your <preprint service> and OSF teams
    
A red banner will appear at the top of the preprint page::

    Rejected: <preprint service> uses [pre][post]-moderation. This preprint has been rejected by a moderator and is not publically available or searchable.

Upon rejection, the preprint will be made private.

If the moderator provides feedback with their decision, there will be a **Moderator feedback** button on the right side of the banner. Clicking this button opens a drop-down. If accepted, the drop-down will read::
  
    Moderator feedback
    Accepted
    This preprint has been accepted by a moderator and is publically available and searchable.

The moderator's feedback will follow, along with their name (or not, if anonymized).

If rejected, the drop-down will read::
  
    Moderator Feedback
    Rejected
    This preprint has been rejected by a moderator and is not publically available or searchable.

The moderator's feedback will follow, along with their name (or not, if anonymized).


Edit a Preprint
---------------
**Purpose:** To upload a new version of a preprint and/or edit the preprint's metadata.

Clicking the green "Edit preprint" button in the top right of the Preprint Detail page takes the user to the Edit Preprint page. 

The user can edit the widgets in any order, but the user cannot leave any of the required information blank, just as they could not during the :ref:`preprint upload process <adding-preprint>`. If the user leaves required information blank and clicks the "Complete" button inside the Update widget to apply their changes, the original metadata will still appear on the Preprint Detail page.

The preprint editing process is the same as the preprint uploading process. The only differences are that the Upload widget has a different workflow, and the submit widget and "Share" button are now called the Upload widget and the "Complete" button, respectively.

Editing the Upload Widget
^^^^^^^^^^^^^^^^^^^^^^^^^
The user cannot edit the Preprint Location section (i.e. the OSF project or component to which their preprint is connected). The Preprint Location section is grayed out and has a lock symbol next to the project/component name.

To upload a new version of their preprint, the user must click to open the Preprint File section. There is a message at the top of this section::
  
    Update preprint file version. File must have the same name as the original.

The user can then drag and drop the new version of their preprint file onto the page in the same way as when they uploaded the :ref:`first version of their preprint <new-preprint>`. If the user uploads a file with a different filename from the original, an alert will appear in the top right of the page::
  
    This is not a version of the current preprint file.

The alert has an animated reverse progress bar that functions as a timer. When the animation completes, the alert disappears, and the Preprint File section closes. 

If the user uploads a new version of their preprint file with the same filename as the original, the Preprint File section will close after the user drags and drops the file onto the page. The filename will appear in the section with a version number next to it::
    
    [filename](Version:x)

The OSF Project
---------------
**Purpose**: Allows the user to add supplemental files to the preprint as well as to view and access the preprint from the OSF side.

On the bottom right of the Preprint Detail page, there is a gray box and a button::
  
    The project for this paper is available on the OSF.
    [Visit project]
    
Clicking the "Visit project" button takes the user to the Project Overview page. A preprint's Project Overview has the same layout as the :ref:`Project Overview page <overview>`, except with the following preprint alert and buttons::
  
    This project represents a preprint. Learn more about how to work with preprint files.[Edit preprint][View preprint]

Clicking the "Edit preprint" button takes the user to the Edit Preprint page.

Clicking the "View preprint" button takes the user to the Preprint Detail page.

If the user makes the OSF project/component private, the preprint will also be set to private and will not appear on the preprint server. The following banner will appear on the project or component Overview page::
  
    This [node_type] has a preprint, but has been made Private. Make your preprint discoverable by making this [node_type] Public.

Clicking the **Make Public** button on the Overview page will make the preprint public, and the preprint will appear again on the designated preprint server.

Adding Supplemental Files
-------------------------
**Purpose:** Allows the user to add supplemental files, code, and other matierals to their preprint.

Adding supplemental files to a preprint works in the same way as adding files to a regular OSF project using the :ref:`OSF storage <OSF-storage>`. The user can only add supplemental files at the top level. Files uploaded to storage add-ons will not appear as *supplemental files* on the Preprint Detail page.

On the Preprint Detail page, supplemental files appear below the MFR. The user can click on a file and the file will appear in the MFR. If there are more than six files (including the primary file) below the MFR, the files will appear in a carousel, and the user can click the right arrow to navigate through the rest of the files. When the user clicks the right arrow to navigate through the files, a left arrow will appear for the user to navigate back through the first set(s) of files.

The metadata and citation styles for the preprint stay the same along the right side of the page, even if the user clicks to read a supplemental file.

If a user clicks on a supplemental file (any file that is not labelled "Primary"), the "Download preprint" button located below the MFR changes to "Download file." The "Download preprint" button located in the top right of the page stays the same and downloads the primary preprint file even if a supplemental file is displayed in the MFR.

Search Preprints
----------------
**Purpose**: To search for and browse preprints in OSF Preprints and other preprint servers.

OSF Preprints is an aggregator of several preprint servers and is powered by SHARE. On the OSF Preprints and community preprint servers' landing pages, the user can enter a query to search for preprints. The search results will appear on the respective "Discover" page. 

The user can search by preprint title by entering the title into the search field. To search by an author(s) or a tag(s), the user can use the boolean operaters AND (including x and x) and OR (including x or x). The accepted formats for searching one or more authors is as follows:
  
  * author:(albert einstein)
  * author: "albert einstein"
  * author: 'albert einstein'
  
  * authors:(nosek AND spies)
  * authors: "nosek AND spies"
  * authors:'nosek AND spies'
  
The accepted formats for searching one or more tags is as follows:

  * tags:"multimedia"
  * tags:(multimedia)
  * tags: 'multimedia'
  
  * tags:"computer AND science"
  * tags:(computer AND science)
  * tags:'computer AND science'

  * tags:"psychology OR neuroscience"
  * tags:(psychology OR neuroscience)
  * tags:'psychology OR neuroscience'

To browse by subject area, there is a list of subject areas on the OSF Preprints and community preprint servers' landing pages. Clicking a subject area will yield preprints within that subject on the "Discover" page.

On the "Discover" page, there is a Provider side bar that shows all of the preprint servers aggregated in that particular preprint server. The user can select a preprint server to search for preprints uploaded to that server. If searching by subject area from the landing page, that subject will be expanded in its hierarchy in the sidebar when the user gets to the "Discover" page. Some community preprint services will have the top-level subjects expanded by default in the sidebar.

Below the Provider sidebar, there is a Subject sidebar that is sorted hierarchically. Clicking a facet next to a subject will unfold the subdisciplines within that subject area. Selecting a subject area will return all of the preprints that have that subject area as a discpline. Taxonomy that is custom to a community preprint server is not listed in this sidebar on the OSF Preprints "Discover" page. The user would need to go to the community preprint server's "Discover" page to search by their custom taxonomy. The preprints tagged with custom taxonomy are still aggregated in OSF Preprints. The tag does not appear on the preprint in search results, but, when clicked, the tag is listed on the preprint's "Details" page.

Selected search facets are defined in the URL, so that a user can share/navigate to that URL and see that search facet and its parent expanded on the "Discover" page.

Preprint search results display the preprint title first, followed by the author(s), discipline(s), abstract, and preprint provider. To access the rest of the metadata, there is a down arrow that the user can click to unfold the search result on the "Discover" page. Clicking the down arrow shows external links, such as a link to a preprint's journal publication, etc., an OAI (if any), tags (if any), and the date and time on which the preprint was added. A "Share" icon is located in the top right of each preprint result so that viewers can quickly share a preprint of interest. Clicking the **Share** icon opens a pop-over with social media sharing options: Twitter, LinkedIn, Email. Selecting a social media platform from the pop-over pulls the preprint information into a modal from which the user can share or email the preprint directly from the "Discover" page.

Annotating a preprint
---------------------
**Purpose**: Enables users to comment on and annotate preprints.

Hypothes.is is integrated as an annotation tool on the "Preprint Detail" pages for preprint services who have this tool enabled. The annotation tool can only be used for users who have signed up for an account on the Hypothes.is site. After creating an account and logging in, the user can view public annotations made on the preprint, as well as highlight and annotate the preprint themselves.

Users who are not logged in to Hypothes.is can view public annotertions made on the preprint.

Hypothes.is is integrated directly on the preprint in the MFR, and can be accessed as an interactive panel that can be expanded or closed.

Opening Hypothesis
^^^^^^^^^^^^^^^^^^
To open the annotation tool, the user must click the **<** icon in the top right of the MFR. The annotation panel will expand part way across the MFR. There are two tabs that the user can toggle between: Annotations | Page Notes. The "Annotations" tab is open by default. 

If no public annotations have been made on the preprint, the following message appears in the "Annotations" tab::
  
  There are no annotations in this group. 
  Create one by selecting some text and clicking the <quotation icon> button.

The quotation icon is not visible to a logged-out user. If public annotations have been made on the preprint, the user can view and share but cannot reply to annotations or flag annotations as spam without being logged in to Hypothesis. If the user clicks the **Reply** button below the annotation without being logged in, they will see the following message::
  
    You must be logged in to create annotations.
    
If the user clicks the **flag** icon below the annotation, a temporary error message will appear::
  
    Login to flag annotations
    You must be logged in to report an annotation to the moderators.

Clicking the **Page notes** tab opens page notes made by the user. If no public page notes have been made, the following message appears in the "Page Notes" tab::
  
  There are no page notes in this group. 
  Create one by clicking the <paper icon> button.

The paper icon *is* visible to a logged-out user, but, when the user clicks this button, they are prompted to log in or create an account in order to add a page note::
  
    You must be logged in to create annotations.

If public page notes have been made on the preprint, the user can view and share them but cannot reply to page notes or flag page notes as spam without being logged in to Hypothesis. If the user clicks the **Reply** icon below the page note without being logged in, they will see the following message::
  
    You must be logged in to create annotations.
    
If the user clicks the **flag** icon below the annotation, a temporary error message will appear::
      
    Login to flag annotations
    You must be logged in to report an annotation to the moderators.


Annotating, adding page notes, and highlighting
-----------------------------------------------
Once logged in, the user can annotate, add pages notes, and  highlight the preprint. 

Annotating
^^^^^^^^^^
**Purpose**: Annotations are comments that respond and link to excerpts of text in a document, and allow users to leave feedback on a preprint.

To add an annotation, the user must first higlight the text with their cursor, after which two buttons will appear in a popover::
  
    Annotate | Highlight

After clicking **Annotate**, the annotation panel will expand, and an editable textbox will appear in which the user can write their annotation. The highlighted text is previewed above the textbox in grayed-out italics. A statement about using the CC0 lisence appears at the bottom of the annotation when in edit mode::
  
    CC0 Annotations can be freely reused by anyone for any purpose.

The user can format their annotation using the following toolbox features:

* Embolden text
* Italicize text
* Quote text
* Insert link
* Insert image
* Insert mathematical notation (LaTex is supported)
* Insert numbered list
* Insert list
* Markdown
* Preview

The user can add tags to the annotation to make it easily discoverable by others.

The user can cancel the annotation by clicking the **Cancel** link at the bottom of the annotation. 

After writing an annotation, the user can post it. Next to the "Post" button is a drop-down menu where the user can choose to either make the annotation public or private::
  
    Public
    Only Me

An annotation is public by default. If the annotation is public, the "Post" button will read "Post to Public;" if the annotation is private, the "Post" button will read "Post to Only Me." A private message is only visible to the user writing the annotation, and is distinguished from public annotations by a "lock" symbol at the top. Once posted, the annotation will link to the excerpt of text that the user highlighted. The annotation will have a tick mark next to the excerpt. In the panel, annotations appear next to the text to which they correspond.

The user's annotations can be edited at any time. Below the user's annotation is a "pencil" icon. Clicking this icon opens the annotation in editing mode. 

Clicking the **Cancel** link returns the annotation to the regular viewing mode.

The user can delete their annotations at any time but cannot delete annotations made by others. Clicking the **trashcan** icon opens a confirmation modal::
  
    Are you sure you want to delete this annotation?
    [Cancel][OK]
    
Clicking **Cancel** closes the modal and cancels the action. Clicking **OK** removes the annotation from the panel, and scrolls the preprint back to the top.

The user can reply to their own annotations by clicking the **Reply** icon, which will open a new annotation box below the original annotation.

 The user can share their annotation by clicking the **Share** icon, which will open a drop-down containing the share link, a copy-to-clipboard button,  and social media options: Twitter, Facebook, Google Plus, and email. If the annotation is private, helper text appears below the share link::
   
    Only me. No one else will be able to view this annotation.
    
If not the owner of the annotation or if the owner is logged out of Hypothesis, pasting the link into the browser will take the user to the Hypothesis site, where they will be prompted to log in::
  
    This annotation is not available. You may need to log in to see it.
    
The owner will be able to log in to Hypothesis to view the annotation.

The user cannot flag their own annotations as spam. In this way, the "Spam" icon is not available on the user's annotations from their end. The user can flag annotations written by other users as spam. Hovering over the **Flag** icon shows a tooltip::
  
    Report this annotation to the moderators

Clicking the **Flag** icon turns the flag red, and flags the page note as spam. Hovering over the red flag shows a new tooltip::
  
    Annotation has been reported to the moderators
    

Adding Page notes
^^^^^^^^^^^^^^^^^
**Purpose**: Page notes allow users to give feedback on the preprint as a whole.

Page notes are comments made in response to the preprint as a whole, and do not link to excerpts of text.

To add a page note, the user must click the **Paper** icon along the side of the panel, after which the panel will expand, and an editable textbox will appear in which the user can write their page note. A statement about using the CC0 lisence appears at the bottom of the annotation when in edit mode::
  
    CC0 Annotations can be freely reused by anyone for any purpose.

The user can format their page note using the following toolbox features:

* Embolden text
* Italicize text
* Quote text
* Insert link
* Insert image
* Insert mathematical notation (LaTex is supported)
* Insert numbered list
* Insert list
* Markdown
* Preview

The user can add tags to the page note to make it easily discoverable by others.

The user can cancel the page note by clicking the **Cancel** link at the bottom of the annotation. 

After writing a page note, the user can post it. Next to the "Post" button is a drop-down menu where the user can choose to either make the page note public or private::
  
    Public
    Only Me

A page note is public by default. If the page note is public, the "Post" button will read "Post to Public;" if the page note is private, the "Post" button will read "Post to Only Me." A private page note is only visible to the user who wrote the page note, and is distinguished from public page notes by a "lock" symbol at the top. In the panel, page notes appear in chronological order, starting at the earliest date posted to the latest.

The user's page notes can be edited at any time. Below the user's page notes is a "pencil" icon. Clicking this icon opens the page note in editing mode.

Clicking the **Cancel** link returns the page note to the regular viewing mode.

The user can delete their page notes at any time but cannot delete page notes made by others. Clicking the **trashcan** icon opens a confirmation modal::
  
    Are you sure you want to delete this annotation?
    [Cancel][OK]
    
Clicking **Cancel** closes the modal and cancels the action. Clicking **OK** removes the page note from the panel.

The user can reply to their own page notes by clicking the **Reply** icon, which will open a new page note text box below the original page note.

The user can share their page note by clicking the **Share** icon, which will open a drop-down containing the share link, a copy-to-clipboard button, and social media options: Twitter, Facebook, Google Plus, and email. If the page note is private, helper text appears below the share link::
   
    Only me. No one else will be able to view this annotation.
    
If not the owner of the page note or if the owner is logged out of Hypothesis, pasting the link into the browser will take the user to the Hypothesis site, where they will be prompted to log in::
  
    This annotation is not available. You may need to log in to see it.
    
The owner will be able to log in to Hypothesis to view the annotation.

The user cannot flag their own page notes as spam. In this way, the "Spam" icon is not available on the user's page notes from their end. The user can flag annotations written by other users as spam. Hovering over the **Flag** icon shows a tooltip::
  
    Report this annotation to the moderators

Clicking the **Flag** icon turns the flag red, and flags the page note as spam. Hovering over the red flag shows a new tooltip::
  
    Annotation has been reported to the moderators

Highlighting
^^^^^^^^^^^^
**Purpose**: The highlighting tool allows users to highlight text in the preprint as they read.

To highlight text, the user must first select the text they want to higlight using their cursor, after which two buttons will appear in a pop-over::
  
    Annotate | Highlight

Clicking **Highlight** will highlight the selected text in yellow.

The highlighted text is only visible to the user highlighting the text. To view the preprint without the highlighted text, the user can click the **eye** icon along the side of the panel. Clicking this icon will show a strikethrough through the icon. The user can still highlight text with the highlighting tool disabled. If the user highlightes text while the highlighting tool is disabled, all the highlights the user made will be visible on the document again, but the icon will still show a strikethrough. The user can click the **eye** icon to show the highlighted text again. 

Orphaned Annotations
^^^^^^^^^^^^^^^^^^^^
**Purpose**: Orphaned annotations allow previous annotations to persist even when a new version of the document has replaced the originally annotated text.

Orphaned annotations occur when a new version of the preprint has been uploaded, and an annotation does not map to the new version's text. Since annotations link to specific text in the preprint, only annotations can be orphaned - page notes cannot be orphaned as they do not link to text. 

If a new version of the preprint has been uploaded and has orphaned any of the annotations, a tab called "Orphans" will appear in the panel next to "Annotations" and "Page Notes." Clicking the **Orphans** tab will list all orphaned annotations. An orphaned annotation looks the same as an unorphaned annotation, except the preview of the text at the top of the annotation has a strikethrough. Orphaned annotations retain the same functionality as unorphaned annotations - if the user wrote an orphaned annotation, they will still be able to edit, add tags, share, and delete the annotation. Orphaned annotations do not link to or otherwise indicate which version of the preprint they map to; the text preview above the annotation is the only way to trace the annotation back to its mapped version.


