.. _preprints:

Preprints
*********

**Purpose:** Sharing a preprint helps the user quickly disseminate their work and receive feedback from peers without having to wait for journal peer review. 

Anyone with an OSF account can create a preprint and upload it to OSF Preprints or a community preprint service. The user can upload a new preprint or turn an existing OSF project or component into a preprint. 

When the user uploads a new preprint (and does not use an existing project or component), an OSF project is automatically created to connect to it. The connected OSF project allows the user to upload supplemental files to their preprint. When the user turns an existing OSF project or component into a preprint, the user can add supplemental files to that project and access the files that they previously added to that project.

The user can access their preprint through their OSF project or component. On the project or component’s Overview page, there will be an alert saying “This [project] [component] represents a preprint. Learn more (this links to preprints help guides] about how to work with preprints.” The user can also access their preprint through the “My Projects” tab and  clicking “All my preprints” from the left sidebar and then clicking the preprint they want to view. 

The user can edit their preprint and upload new versions. Once a preprint is shared, it should be assumed that it will always be public and available.

OSF Preprints
-------------
**Purpose:** To search for preprints, upload a preprint, and access the preprint community services.

To navigate to the OSF Preprints landing page, the user must click the **OSF Home** button in the navigation bar and then click **OSF Preprints** from the drop-down menu.

On the OSF Preprints landing page, there is a search field to search for preprints, a green **Add a preprint** button below the search field, and a section titled "Browse by subject" that shows the 10 top-level subject areas provided by Bepress (see the `Search Preprints`_ section).

For all preprint services, the navigation bar is laid out as follows:

* **My Preprints** takes the user to their preprints list on the :ref:`My Projects page <organizer>`.
* **Add a preprint** takes the user to the "Submission" page.
* **Search** takes the user to the "Discover" page.
* **Support** takes the user to the preprints help guides.
* **Donate** takes the user to the COS "Donate" page.

If the service uses moderation, the "Add a preprint" button reads "Submit a <submission_type>".

The following tabs appear in the navigation bar when the user is *logged out of* OSF Preprints:

* **OSF Preprints** Clicking this tab prompts a drop-down menu with the OSF Products: OSFHome, OSFPreprints, OSFRegistries, OSFMeetings, OSFInstitutions.
* **Add a preprint**: Clicking this link takes the user to the :ref:`sign-in page <login>`.
* **Search**: Clicking this link takes the user to the corresponding preprints "Discover" page.
* **Support**: Clicking this link takes the user to the preprints help guides.
* **Sign Up**: Clicking this button takes the user to the :ref:`Create a free account page <sign-up>`.
* **Sign In**: Clicking this button takes the user to the :ref:`OSF sign-in page <login>`. After logging in, the user is taken to the OSF Preprints landing page.

The community preprint services are listed with their logos below the search field. Clicking on a community preprint service logo takes the user to that preprint service's landing page.

When logged in, the navigation bar is the same except that the "Sign up" and "Sign in" buttons are replaced with the user drop-down menu.

community preprint services
--------------------------
**Purpose:** To search for preprints within and upload preprints to a given preprint service.

When the user navigates to a community preprint service, the landing page is the same as OSF Preprints, except for different color schemes and different actions in the :ref:`navigation bar <navigation-bar>`. The top-level subject areas highlighted on a community preprint service's landing page vary in subject and number by each service. If the preprint service has chosen their own custom taxonomy as well as highlighted subjects, the "Browse by subjects" section is instead titled "Browse by featured subjects." When the section is "Browse by featured subjects," a link is included below the title to "See all subjects available," that, when clicked, takes the user to the "Discover" page to view all subjects available.

The following tabs appear in the navigation bar when the user is logged out:

* **Add a preprint**:  Clicking this tab takes the user to the :ref:`OSF sign-in page <login>`.
* **Search**: Clicking this tab takes the user to the preprint service's Discover page https://osf.io/preprints/preprintservice/discover.
* **Donate** takes the user to the COS "Donate" page.
* **Sign Up**: Clicking this tab takes the user to the :ref:`Create a free account page <sign-up>` where the user needs to fill out a form to create an OSF account in order to be able to upload a preprint to the community preprint service. 
* **Sign In**: Clicking this tab takes the user to the :ref:`OSF sign-in page <login>`. After logging in, the user is taken to their OSF dashboard.

When logged in, the navigation bar is the same except that it contains a "My OSF Projects" tab which, when clicked, takes the user to https://osf.io/myprojects/ and the "Sign up" and "Sign in" buttons are replaced by the user drop-down menu.

.. _adding-preprint: 

Adding a Preprint
-----------------
**Purpose**: To submit a preprint, the user must upload their file and fill out required information related to their preprint in the following form.
  
Clicking the green **Add a preprint** button takes the user to the "Create Preprint" page where the user must complete the five sections (in order) to sharing their preprint:

* Select a service: Only available on OSF Preprints. The user must select the preprint service on which they want to post their preprint.
* File: The user must upload their preprint file and enter a preprint title.
* Basics: The user must provide metadata about the preprint.
* Discipline: The user must select disciplines to add to their preprint.
* Authors: The user can choose to add coauthors, but can also choose to be the only author.
* Supplemental materials: The user can choose to connect supplemental materials project to their preprint.
* Submit: The user uploads their preprint to the preprint service.

After the user clicks **Save and continue** in each section, a confirmation message appears in to top right corner of the section::
  
    Changes Saved!

The user must complete the required steps within each section before they can upload their preprint. If the user starts the submission form, and then attempts to navigate away from the form, a browser alert will appear to confirm that the user intends to leave the page. On OSF Preprints, this alert gets triggered when the user starts the "File" section.
    
File
^^^^^^
**Purpose**: Prompts the user to upload their preprint file.

There is an additional section at the start of the preprint form for OSF Preprints: "Select a preprint service." This section is not available on community preprint services. This section gives users the choice to upload their preprint to OSF Preprints or a community preprint service. This section consists of a carousel showing the preprint service logos that the user must select to choose a preprint service. The "OSF Preprints" logo is selected by default. Hovering over a logo shows the name of the preprint service in a tooltip. The user can click the navigational arrows to navigate through the carousel. When selecting a preprint service, an inline description of the service appears below the carousel.

If the user clicks inside another section before saving their changes, a temporary, red error message appears in the top right of the page::
  
    Please select a preprint service before continuing

At the bottom of the section are "Discard changes" and "Save and continue" buttons. The "Discard changes" button is disabled. It becomes enabled if the user clicks **Save and continue**, reopens the section, and selects a different preprint service. Clicking **Discard changes** re-selects the first preprint service from the list, and disables the "Discard changes" button. Clicking **Save and continue** closes the "Select a preprint service" section, where a temporary, green confirmation message appears in the top right::
  
    Changes Saved!
    
The "Select a preprint service" section shows the service that was selected::
  
    Preprint service: <preprint service name>

Once the "Select a preprint service" section closes, the "File" section opens (this section is auto-expanded for community preprint services).

If the user leaves the "File" section incomplete and clicks inside another section, an alert will appear in the top right of the submission page::

    Please complete upload section before continuing
    
The alert has an animated reverse progress bar that functions as a timer. When the animation completes, the alert disappears, and the "File" section remains open.

The section contains two options for adding a preprint file::

    [Upload from your computer [Select from an existing OSF project]

Clicking the **Upload from your computer** button opens an upload zone with helper text::
      
    Drop preprint file here to upload

There are two buttons to the bottom right of the file box::
  
    [Back][Save and continue]

The "Save and continue" button is disabled until the user meets the requirements of uploading a file and entering a title.

The user can add their preprint file by either dragging and dropping it into the upload zone or uploading it from dialog box.

When the user uploads their preprint file, there filename along with the file size, and a progress bar appear to signify the file upload. The user can upload another file at this time to replace the file just added. The helper text changes to::
    
    Click or drag another preprint file to replace

After uploading the preprint file, the preprint title field appears below the upload zone, with the following helper text::
    
    Enter preprint title

If the user clicks inside the title field without entering a title, and then clicks elsewhere within the section, a growlbox appears below the title field that reads::
  
      Title can't be blank

After entering a title, the user can click **Save and continue** or press the **enter** to continue to the next section.

A temporary alert confirming the upload will appear in the top right of the page::
  
    Preprint file uploaded!

This alert has an animated reverse progress bar that functions as a timer. When the animation completes, the alert disappears.

Clicking the **Select from an existing OSF project** allows the user to select a file that is already stored in one of their OSF projects. With this workflow, the preprint title takes the title of the selected project or component. After clicking **Select from an existing OSF project**, the user is presented with the "Choose project" section where the user can select a project from a drop-down menu with helper text::
  
    Click to select
    
After clicking inside the menu, a drop-down menu appears with the following helper text::
  
    Type to search

Typing into the field shows the following helper text::
  
    Loading options...
    
A maximum of 7 projects are shown at a time. If there are more than 7 projects, the user can scroll through the menu to view more matching results.
    
After the user selects a project or component from the drop-down menu, the "Choose Project" section closes, and the "Choose File" section appears below it.

In the "Choose File" section, the OSF Storage for the project is displayed with "Back" and "Save and continue" buttons. "Save and continue" remains disabled until the user selects a file from the list. If no files are stored in the project, the following message appears below OSF Storage::
  
    No files found

If no files are stored, the user can either click the **Back** button and re-click the **Select from an existing OSF project** to choose a file from a different project, or click **Back** to click the **Upload from your computer** option.  

If files *are* stored in the project, the user can select a file from the list, after which the "Save and continue" button will become enabled. After clicking **Save and continue**, the user is taken to the next section.

Basics
^^^^^^
**Purpose:** Prompts the user to select a license, provide an abstract, and add other metadata.

In the bottom right of the "Basics" section, there are two buttons::
  
    [Discard changes][Save and continue]

These buttons are disabled until the user has filled the required fields. The required sections and fields for this section are:

* Choose a license
* Abstract

If the user chooses the **No license** option from the license drop-down menu, the two fields that appear below the menu are also required:
* Year
* Copyright Holders

**License**

In the license section, the user has the following options::
    
    **Choose a license:** (required)
    [Drop-down selections]
    `License FAQ <http://help.osf.io/m/preprints/l/726873-preprint-faqs#how_should_i_license_my_preprint>`_. 
    Show full text (clicking this shows an explanation of the license selected)
    Hide full text (this appears in place of Show full text when the user clicks to view the text)

The licenses available vary by preprint service. OSF Preprints offers No license, CC0 1.0 Universal, and CC-By Attribution 4.0 International. If the user selects "No license" from the drop-down menu, the "Year" and "Copyright Holders" fields appear below the menu.

These two fields are required. In the "Year" field, the current year is listed automatically. If the user deletes the current year - e.g. "2017"- from the field, the year will reappear automatically in the field. To enter a different year, the user can delete the last 1-3 numbers and type in the correct year from there. If the user deletes the first number- e.g. "2"- the year will reappear automatically in the field.

There is an option to "Apply this preprint license to my OSF project." The user can select "Yes" or "No" to either extend or not extend the preprint license to their OSF project. "Yes" is selected automatically. Note that if the user selects "No license" option from the drop-down menu, they can choose to extend this license to their OSF project, as well.

**The DOI section**
A DOI is automatically generated for a preprint upon submission, and is minted through Crossref. Each preprint service has a unique DOI prefix. If the  preprint has been published in a journal, the user can enter the peer-reviewed DOI into the "Peer-reviewed publication DOI (optional)" field.
    
If the user enters an invalid DOI, a red error message appears below the field::
  
    Please use a valid DOI
    
The error message disappears when the user removes the invalid DOI.

**Original Publication Date**

If their preprint has been previously published, the user can include the publication year, month, and day into this field. Clicking inside this field opens a calendar picker from which the user can select and apply the publication date.

This publication date will appear in the preprint's metadata, as well as in the preprint citations.

**The Keywords section**
    
In the Keywords section, the user can add tags to their preprint in the text box that has the instructions::
  
    Add a tag

**The Abstract section**

In the Abstract section, the text box has instructions that read::
  
    Add a brief summary of your preprint

If the user starts typing into the Abstract text box and deletes what they have written, a growlbox will appear below the text box that reads::
  
    Abstract can't be blank

When the user starts typing their abstract and the content is--so far--less than 20 characters long, a growlbox will appear below the text box that reads::
  
    Abstract is too short (minimum is 20 characters)

The growlbox disappears once the user has typed 20 characters. When the abstract is less than 20 characters, the text box is outlined in blue, but when the abstract reaches 20 characters and more, the textbox is outlined in green.

When the user has filled out all of the required sections and fields, they can either click [Discard changes][Save and continue]

Clicking "Discard changes" will cause a growlbox to appear below the Abstract text box that reads::
  
    Abstract can't be blank

**Finishing the Basics section**
 
In the event that the user chooses "No license" from the drop-down menu and fills out the "Year" and "Copyright Holders" fields as their last steps before they finish the Basics section, the user can press the **return** key (Mac) or the **Enter** key (Windows) on their computer to close the Basics section and open the Authors section.

The user can also click [Save and continue] to close the Basics section and open the Authors section.

This is how the section appears when closed::
  
    Basics (this is a link that the user can use to click to open the section; the user can click anywhere inside the section to open it)
    License: [license type]
    DOI: [DOI] (or) None (if no DOI is provided)
    Abstract:
    [abstact content]
    Click to Edit
    
The user can click inside the Basics section to open it and make changes at any point throughout the preprint upload process. When the user reopens the Basics section, they cannot click "Discard changes" unless they have made changes to the information they previously provided in the section. Once the user has made changes to the information, the user can click "Discard changes."
    
Discipline
^^^^^^^^^^
**Purpose:** Prompts the user to select disciplines to be added to their preprint.

The taxonomy for the disciplines comes from BePress.

At the top of the Discipline section, there is a message that reads::
  
    Select a discipline and sub-discipline, if relevant. Add more by clicking on a new discipline or sub-discipline.

There are three columns that sort the hierarchies of the disciplines and sub-disciplines.

There are two buttons in the bottom right of the section::
  
    [Discard changes][Save and continue]

In the left column, all of the disciplines available in OSF Preprints are listed::

    Architecture
    Arts and Humanities
    Business
    Education
    Engineering
    Law
    Life Sciences
    Medicine and Health Sciences
    Physical Sciences and Mathematics
    Social and Behavioral Sciences
    
When selecting a discipline, the user must click on a top-level discipline from the left column, and it will be added to their preprint. Their disciplines will appear above the discipline chooser.

To select a sub-discipline, the user must click on a top-level discipline to view sub-disciplines rendered in the middle column. The user can select a sub-discipline from the middle column to render third-level disciplines in the right column.

To remove disciplines from their preprint, the user can click the white "x" to the right of their added disciplines.

The user can click inside any other section prior to adding disciplines; however, the user must add at least one discipline to their preprint before they can upload it.

Until the user adds a discipline, they will not be able to click "Discard changes" or "Save and continue."

When the user clicks "Save and continue," the Discipline section will close, and the Basics section will open.

The user can return to the Discipline section to make changes at any point throughout the preprint upload process. 

Authors
^^^^^^^
**Purpose:** Prompts the user to add authors.

This section is optional. 

At the top of the Authors section, there are instructions that read::
  
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

When the user clicks the green "Add" button, the author will be added to the Authors section on the right side of the section below the user's name.
  
If the author who the user searches for has an OSF account, a Results section will appear below the gray box, and the author's name will be listed in the Results section with a green "Add" button to the right of their name.

When the user clicks the green "Add" button, the author will be added to the Authors section on the right side of the section below the user's name.

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

When the user is finished filling out the Authors section, they can click the blue **Continue** button in the bottom right of the section.

After the user clicks the **Continue**, the section will close and the next section open. 

Supplemental materials (Optional)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
**Purpose**: Enables the user to add or connect a supplemental node to store supplemental materials for their preprint.

This section is optional.

At the top of the section, helper text reads::
  
    Connect an OSF project to share data, code, protocols, or other supplemental materials.

The user is presented with two options::
  
    [Connect an existing OSF project][Create a new OSF project]

Clicking **Connect an existing OSF project** presents the user with a drop-down menu from which they can search and select a project. Helper text inside the drop-down menu reads::
  
    Click to select

Helper text below the drop-down menu reads::
  
  The list of projects appearing in the selector are projects and components for which you have admin access.
  This will make your project public, if it is not already.

After clicking inside the menu, a drop-down menu appears with the following helper text::
    
      Type to search

Typing into the field shows the following helper text::
    
      Loading options...
      
A maximum of 7 projects are shown at a time. If there are more than 7 projects, the user can scroll through the menu to view more matching results.

Below the drop-down menu are "Back" and "Save and continue" buttons. The user can click **Back** to return to the options to connect a supplemental node. The "Save and continue" button remains disabled until the user selects a project from the drop-down menu.

Clicking **Save and continue** takes the user to the final section.

Selecting **Create a new OSF project** presents the user with a "Project title" field, where the OSF generates a default title for the project to be created::
  
    Supplemental materials for preprint: <preprint title>

Below the field are "Back" and "Save and continue" buttons. Since a title is provided by default, the "Save and continue" button is enabled. The user can modify the title in the field. If the user deletes the entire title, leaving the field blank, the "Save and continue" button becomes disabled, and a red inline error appears below the field::
  
    Title can't be blank

Helper text in the field reads::
  
    Enter supplemental project title

At least 1 character must be entered into the field in order for the "title" requirements to be met.

After providing a title, the "Save and continue" button becomes enabled again. After clicking **Save and continue**, the "Supplemental materials" section closes.

Finalize submission
^^^^^^^^^^^^^^^^^^^
Once the user has filled out the required fields and reaches the bottom of the page, they can submit their preprint. Instructions walk the user through what will happen after submission.

For services who do not use moderation, the "Add a preprint" button in the navigation bar reads "Add a <submission_type>" and the submission language is as follows::
  
  By creating this <submission_type>, you confirm that all contributors agree with sharing it and that you have the right to share this <submission_type>.
  
  When you create this <submission_type>, it will be assigned a DOI and become publicly accessible via OSF. The <submissions_type> file cannot be deleted, but it can be updated or modified.
  [Cancel][Create <submission_type>]

For services that use post-moderation, the "Add a preprint" button in the navigation bar reads "Submit a <submission_type>" and the submission language is as follows::
  
  By submitting this <submission_type>, you confirm that all contributors agree with sharing it and that you have the right to share this <submission_type>.
  [Cancel][Submit <submission_type>]
  
  <service> uses post-moderation. When you submit this <submission_type>, it will be assigned a DOI and become publicly accessible via <service>. Your <submission_type> will only become private if rejected by a moderator. The <submission_type> file cannot be deleted, but it can be updated or modified. 
  [Cancel][Submit <submission_type>]

For services that use pre-moderation, the "Add a preprint" button in the navigation bar reads "Submit a <submission_type>", and the submission language is as follows::
  
    By submitting this <submission_type>, you confirm that all contributors agree with sharing it and that you have the right to share this <submission_type>.
    [Cancel][Submit <submission_type>]
    
    <service> uses pre-moderation. If your <submission_type> is accepted, it will be assigned a DOI and become publicly accessible via <service>. The <submission_type> file cannot be deleted, but it can be updated or modified. 
    [Cancel][Submit a <submission_type]

If the user has not finished all required sections, and they click the **Create** button, a message will appear below the instructions that reads with a list of the unfinished sections::
  
    The following section(s) must be completed before submitting this <submission_type>.
    <section titles>

After clicking the **Create preprint** button, a confirmation modal appears::

    Create Preprint
    Once this preprint is made public, you should assume that it will always be public. Even if you delete it, search engines or others may access the files before you do so.
    [Cancel][Create]
    
For services using moderation, the modal reads::
  
    Submit <submission_type>
    Once this <submission_type> is made public, you should assume that it will always be public. Even if you delete it, search engines or others may access the files before you do so.
    [Cancel][Submit]
    
Clicking **Cancel** returns the user to the submission page form.

Clicking the **Create** button submits the preprint and directs the user to the "Preprint Detail" page.   

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

Submitting to a moderated service
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
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
  
    Pending: <preprint service> uses pre-moderation. this preprint is not publicly available or searchable until approved by a moderator.

If the user submitted to a preprint service that uses post-moderation, the user will receive a confirmation email upon submission titled "Confirmation of your submission to <preprint service>"::
  
  Hello <user name>,

  Your preprint <preprint title> has been successfully submitted to <preprint service>.

  <preprint service> has chosen to moderate their submissions using a post-moderation workflow, which means your submission is public and discoverable, while still pending acceptance by a moderator. You will receive a separate notification informing you of any status changes.

  Learn more about <preprint service> or OSF.

  Sincerely,
  Your <preprint service> and OSF teams

In the last line of the email, the "preprint service" and "OSF" link to the preprint service landing page and OSF dashboard, respectively.
  
The preprint will be public upon submission. Until a moderator accepts or rejects the preprint, a blue banner will appear at the top of the page::

    Pending: OSF uses post-moderation. This preprint is publicly available and searchable but is subject to removal by a moderator.

If the moderator accepts the preprint, a green banner will appear at the top of the preprint page::
  
    Accepted: <preprint service> uses [pre][post]-moderation. This preprint has been accepted by a moderator and is publicly available and searchable.

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

    Rejected: <preprint service> uses [pre][post]-moderation. This preprint has been rejected by a moderator and is not publicly available or searchable.

Upon rejection, the preprint will be made private.

If the moderator provides feedback with their decision, there will be a **Moderator feedback** button on the right side of the banner. Clicking this button opens a drop-down. If accepted, the drop-down will read::
  
    Moderator feedback
    Accepted
    This preprint has been accepted by a moderator and is publicly available and searchable.

The moderator's feedback will follow, along with their name (or not, if anonymized).

If rejected, the drop-down will read::
  
    Moderator Feedback
    Rejected
    This preprint has been rejected by a moderator and is not publicly available or searchable.

The moderator's feedback will follow, along with their name (or not, if anonymized).

Preprint Detail Page
--------------------
 **Purpose:** renders the preprint file and provides a consistent URL to host the preprint.

The preprint title appears at the top of the "Preprint Detail" page. Below the title is a list of the preprint authors. If a co-author is a registered contributor, their name will be linked to their OSF profile page. The date when the preprint was shared and the date when the preprint was last edited are listed below the preprint's title. If supplemental materials have been connected, a link titled "Supplemental materials" and the URL of the OSF project will be listed here, as well. Clicking the URL will open the OSF project in a new tab. The project will remain empty until the user has navigated to it and added materials.
 
On the left half of the page, the preprint is displayed in the MFR. Below the MFR is the preprint filename, the current version number, and links to previous versions (if available). If only one version has been uploaded, the current version number appears as::
  
    Version: 1

If more than one version has been uploaded, the version number increases accordingly. The most recent version is rendered in the MFR. To access previous versions, a drop-down menu appears next to the version number. The drop-down button has the call-to-action: "Download previous versions." Clicking the button pulls all previous versions with their upload dates and times, and displays the versions from newest to oldest. For example::

  Version 3, 01/18/2019 10:33:79
  Version 2, 11/14/2018 8:45:15
  Version 1, 09/01/2018 4:29:33

Selecting any version from the menu (even the most recent) will download the file to your browser.

On the right half of the page, the preprint's abstract, license, disciplines, Preprint DOI (when clicked takes the user to the "Preprint Detail" page), Peer-Review Publication DOI (optional - appears if the user's preprint has been previously published and the user has provided the DOI), Original Publication Date, tags, and citation styles (MLA, APA, and Chicago) are listed. 

Below the default citation styles is a citation picker with a header "Get more citations." The user can click inside the citation picker to type in another citation style. Helper text reads::
    
    Please enter a few characters

Typing into the search fields changes the helper text to::
    
    Searching...

A drop-down list of citation styles will appear. After selecting a citation style from the menu, the preprint citation will be generated below the citation picker in the selected style. Meanwhile, the default citation styles are still listed in the metadata. Upon refreshing the page, the generated citation disappears.

It can take up to 24 hours for a preprint to be minted, in which case the DOI is listed, but not linked, and the following message appears below the Preprint DOI::
  
    DOIs are minted by a third party, and may take up to 24 hours to be registered

If the user has entered a peer-reviewed DOI and an original publication date, these metadata will appear in the citations (not all citation styles use DOIs). If the user has not entered a peer-reviewed DOI, the preprint DOI is used in the citations.

If an abstract is long, there will be a **See more** button below the abstract that the user can click to expand the remaining text. When the abstract is expanded, the button changes to **See less**. When the user clicks the **See less** button, the abstract shrinks back to its shorter length, and the **See more** button returns.

In the top right of the Preprint Detail page, there is a gray box that includes a series of actions for downloading and sharing a preprint::

   [Download preprint], the number of downloads [Downloads: x], and social media sharing options

At the bottom right of the page, there is a gray box that reads::
     
    The project for this paper is available on the OSF
   [Visit project] (links to the OSF project connected to a preprint)

Admins can see a green "Edit preprint" button in the top right of the Preprint Detail page. Contributors with read access or read+write access and visitors to a Preprint Detail page cannot see this button.

Edit a Preprint
---------------
**Purpose:** To modify and update preprints.

Only authors with admin permissions on the preprint can edit the preprint. The "Edit preprint" button is located in the top right of the page. If an author does not have admin permissions, the button is not visible.

Clicking the **Edit preprint** button directs the user to the "Edit Preprint" page. 

The user can edit the sections in any order, but the user cannot leave any of the required information blank, just as they could not during the :ref:`preprint upload process <adding-preprint>`.

The user can upload a new version of the preprint in the "File" section. Versioning requires that new versions must have the same filename and file extension as the original preprint. Helper text above the upload zone reads::
  
    Update preprint file version. File must have the same name as the original.

If the user uploads a file with a different filename, a growlbox appears in the top right of the page::
    
    This is not a version of the current preprint file.
    
If the user uploads a new version of their preprint using the same filename, the version number will update accordingly in the "File" section::
        
    [filename](Version: x)
    
The user can connect or change a supplemental materials node at any time. If the user has not connected a node prior, the same workflow as during the submission process will appear. At the top of the section is a link to the current supplemental node::
  
    Connected OSF project: <osf_project>

If the user has connected a node, the options to modify this section are as follows::
  
    [Change the connected project][Disconnect the project]
    
Clicking **Change the connected project** presents the user with the same workflow as during submission::
  
    [Connect an existing OSF project][Create a new OSF project]

Clicking **Disconnect the project** disconnects the node. A temporary confirmation message appears in the top right of the page::
  
    Supplemental project disconnected.

After disconnecting the node, the original options appear again in this section::
  
    [Connect an existing OSF project][Create a new OSF project]
    
The preprint editing process is otherwise the same as the preprint uploading process. When the user is finished editing the preprint, or chooses not to make any changes, the user can click the **Return to preprint** button at the bottom of the page to return to the "Preprint Detail" page. If no changes have been made, a confirmation modal appears after clicking this button::
  
    Are you sure you want to abandon changes to this preprint?
    [Cancel][OK]

Clicking **Cancel** keeps the user on the "Edit preprint" page. Clicking **OK** directs the user to the "Preprint Detail" page.

Search Preprints
----------------
**Purpose**: To search for and browse preprints in OSF Preprints and other preprint services.

OSF Preprints is an aggregator of several preprint services and is powered by SHARE. On the OSF Preprints and community preprint services' landing pages, the user can enter a query to search for preprints. The search results will appear on the respective "Discover" page. 

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

To browse by subject area, there is a list of subject areas on the OSF Preprints and community preprint services' landing pages. Clicking a subject area will yield preprints within that subject on the "Discover" page.

On the "Discover" page, there is a "Providers" sidebar that shows all of the preprint services aggregated in that particular preprint service. The user can select a preprint service to search for preprints uploaded to that service. If searching by subject area from the landing page, that subject will be expanded in its hierarchy in the sidebar when the user gets to the "Discover" page. Some community preprint services will have the top-level subjects expanded by default in the sidebar.

Below the "Providers" sidebar, there is a Subject sidebar that is sorted hierarchically. Clicking a facet next to a subject will unfold the sub-disciplines within that subject area. Selecting a subject area will return all of the preprints that have that subject area as a dicscpline. Taxonomy that is custom to a community preprint service is not listed in this sidebar on the OSF Preprints "Discover" page. The user would need to go to the community preprint service's "Discover" page to search by their custom taxonomy. The preprints tagged with custom taxonomy are still aggregated in OSF Preprints. The tag does not appear on the preprint in search results, but, when clicked, the tag is listed on the preprint's "Details" page.

Selected search facets are defined in the URL, so that the user can share/navigate to that URL and see that search facet and its parent expanded on the "Discover" page.

Preprint search results display the preprint title first, followed by the author(s), discipline(s), abstract, and preprint service. To access the rest of the metadata, there is a down arrow that the user can click to unfold the search result on the "Discover" page. Clicking the down arrow shows external links, such as a link to a preprint's journal publication, etc., an OAI (if any), tags (if any), and the date and time on which the preprint was added.

Annotating a preprint
---------------------
**Purpose**: Enables users to comment on and annotate preprints.

Hypothes.is is integrated as an annotation tool on the "Preprint Detail" pages for preprint services who have this tool enabled. The annotation tool can only be used for users who have signed up for an account on the Hypothes.is site. After creating an account and logging in, the user can view public annotations made on the preprint, as well as highlight and annotate the preprint themselves.

Users who are not logged in to Hypothes.is can view public annotations made on the preprint.

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

To add an annotation, the user must first highlight the text with their cursor, after which two buttons will appear in a popover::
  
    Annotate | Highlight

After clicking **Annotate**, the annotation panel will expand, and an editable text box will appear in which the user can write their annotation. The highlighted text is previewed above the textbox in grayed-out italics. A statement about using the CC0 license appears at the bottom of the annotation when in edit mode::
  
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

To add a page note, the user must click the **Paper** icon along the side of the panel, after which the panel will expand, and an editable text box will appear in which the user can write their page note. A statement about using the CC0 lisence appears at the bottom of the annotation when in edit mode::
  
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

To highlight text, the user must first select the text they want to highlight using their cursor, after which two buttons will appear in a pop-over::
  
    Annotate | Highlight

Clicking **Highlight** will highlight the selected text in yellow.

The highlighted text is only visible to the user highlighting the text. To view the preprint without the highlighted text, the user can click the **eye** icon along the side of the panel. Clicking this icon will show a strikethrough through the icon. The user can still highlight text with the highlighting tool disabled. If the user highlights text while the highlighting tool is disabled, all the highlights the user made will be visible on the document again, but the icon will still show a strikethrough. The user can click the **eye** icon to show the highlighted text again. 

Orphaned Annotations
^^^^^^^^^^^^^^^^^^^^
**Purpose**: Orphaned annotations allow previous annotations to persist even when a new version of the document has replaced the originally annotated text.

Orphaned annotations occur when a new version of the preprint has been uploaded, and an annotation does not map to the new version's text. Since annotations link to specific text in the preprint, only annotations can be orphaned - page notes cannot be orphaned as they do not link to text. A tab called "Orphans" will appear in the panel next to "Annotations" and "Page Notes."

Clicking the **Orphans** tab will list all orphaned annotations. An orphaned annotation looks the same as an un-orphaned annotation, except the preview of the text at the top of the annotation has a strikethrough. Orphaned annotations retain the same functionality as un-orphaned annotations - if the user wrote an orphaned annotation, they will still be able to edit, add tags, share, and delete the annotation. Orphaned annotations do not link to or otherwise indicate which version of the preprint they map to; the text preview above the annotation is the only way to trace the annotation back to its mapped version.


