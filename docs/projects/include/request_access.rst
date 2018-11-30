Request Access
**************
The request access feature gives non-contributors the opportunity to collaborate on and access both public and private projects. This feature must be enabled on the project for non-contributors to request access. Admins on the project can enable or disable request access via their :ref:`project Settings page <project-settings>`.


Request access on private projects
----------------------------------
**Purpose**: To allow users who have the URL of a private project to request access to it.

To request access on a private project, the user must navigate to the project's URL. They will be taken to a restricted page that reads::
  
    You Need permission
    Ask for access, or switch to an account with permission.
    [Request access][Switch account]
    If this should not have occurred, please contact support@osf.io.

Clicking the **Request access** button disables the button and updates the button text to read "Access requested," indicating to the user that their request has been submitted. Above the button, the helper text updates to::
  
    Your request for access has been sent. You will receive an email if and when your request is approved.
    
Clicking the **Switch account** button takes the user to the :ref:`OSF login page <login>` where they can switch to their correct account. If the user is already a contributor on the project, but they are logged into the wrong account, this button makes it easy for them to switch accounts.


Request access on public projects
---------------------------------
**Purpose**: Gives the opportunity for users to collaborate on research they find on OSF.

To request access on a public project, the user must click the **ellipsis** button in the top right of the project "Overview" page. After clicking the button, a drop-down menu will unfold, from which the user can click the **Request access** button. Upon clicking the **Request Access** button, the button becomes disabled and updates to read **Access requested**, indicating to the user that their request has been submitted.


Grant or reject access
----------------------
**Purpose**: To allow admins to choose who can contribute to their project.

When a user requests access to a project, the admins will receive an email notification titled "An OSF user has requested access to your project"::
  
    Hello <admin name>,

    <user name> has requested access to your project <"project name">.

    To review the request, click here <https://.osf.io/GUID/contributors/> to allow or deny access and configure permissions.

    This request is being sent to you because your project has the 'Request Access' feature enabled. This allows potential collaborators to request to be added to your project. To disable this feature, click here <https://osf.io/GUID/settings/>.

    Sincerely,

    The OSF Team

    Want more information? Visit https://osf.io/ to learn about OSF, or https://cos.io/ for information about its supporting organization, the Center for Open Science.

To grant or reject access to the project, the admin must navigate to the "Contributors" page of their project, where a "Requests for access" section will appear at the bottom of the Contributors list. The following helper text appears below the section header::
    
    The following users have requested access to this project.

The list of requests are formatted in the same table structure as regular contributors, where the admin can assign permissions and bibliographic status. At the end of the table row is a green **+Add** button and a black **X** to reject the user. 

Clicking the **+Add** button adds the user to the Contributors list where their permissions can continue to be modified like regular contributors. Their name will be removed from the "Requests for access" section. If the added user was the only request in the list, the "Requests for access" section will disappear from the page. The recently added user will receive an email titled "Your access request to an OSF project has been approved" notifying the user that they were added to the project::
  
  Hello <user name>,

  <admin name> has approved your access request and added you as a contributor to the project <"project name"> on OSF.

  You will be automatically subscribed to notification emails for this project. To change your email notification preferences, visit your project or your user settings.

  Sincerely,

  The OSF Team

  Want more information? Visit https://osf.io/ to learn about OSF, or https://cos.io/ for information about its supporting organization, the Center for Open Science.

  Questions? Email contact@osf.io

If a user is added to a project after requesting access, and is later removed by the admin as a regular contributor, the user can request access again.
  
Clicking the **X** button removes the user from the "Requests for access" section. If the removed user was the only request in the list, the "Requests for access" section will disappear from the page. The user will receive an email titled "Your access request to an OSF project has been declined" notifying the user that their request was rejected::
  
  Hello <user name>,

  This email is to inform you that your request for access to the project at https://osf.io/GUID/ has been declined.

  Sincerely,

  The OSF Team

  Want more information? Visit https://osf.io/ to learn about OSF, or https://cos.io/ for information about its supporting organization, the Center for Open Science.

  Questions? Email contact@osf.io
  
If the user navigates back to the public project and attempts to request access again, the button will still be disabled and read "Access Requested," and a tooltip will read::
  
    Request declined

If the project is private, and the user navigates to the URL, the button will still be disabled and read "Access requested," and a tooltop will read::
  
    Request declined
