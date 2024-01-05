# How to Configure a RHEL 8 Workstation

## Evolution

Requires:

```bash
dnf install evolution evolution-ews
```

Get your organization's [Azure Tenant ID](https://portal.azure.com/#view/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/~/Properties)

Get your organization's [Azure Application ID for Evolution](https://portal.azure.com/#view/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/~/AppAppsPreview/menuId~/null)

Procedure to add your account to Evolution:

1. Start the account editor.
2. Add account.
3. For "Identity" enter:
  - Full Name
  - Email Address (typically First.Last@Colorado.EDU)
  - Uncheck "Look up mail server details based on the entered e-mail address."
4. For "Receiving Email" enter:
  - Server Type: choose "Exchange Web Services"
  - Username: <identikey>@colorado.edu
  - Host URL: use "https://outlook.office.com/mail/" at this time (we will change this later)
  - Under Authentication, choose "Oauth2 (Office 365)"
  - Check "Override Office365 OAuth2 settings"
  - Enter your Tenant ID
  - Enter your org's Evolution Application ID
5. Click "Finish"
  - At this point you will need to enter your password into the authentication dialog.
  - Accept the requested access permissions.
6. Once you have successfully authenticated, return to the account editor.
  - Click the subcontent triangle to show the "Mail Accounts" for your account.
  - Then click the "Mail Accounts" subcontent triangle to see the account name.
  - Then click on "Edit"
7. Select "Receiving Email"
8. Click on "Fetch URL" (to the right of "Host URL")
  - This should refresh both the "Host URL" and the "OAB URL"
9. If you want to use your "Archive" folder, go to the "Defaults" in "Account Editor" and select the folder you want to use under "Archive Folder"

You are done. You can follow the procedure above for each account you want to monitor. You can limit the configuration to email only (choose during setup).