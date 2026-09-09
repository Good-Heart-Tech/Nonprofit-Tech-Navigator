---
description: >-
  These instructions will review how to add an unlicensed admin account in
  Google Workspace (Super Admin role) to allow IT admins to see and manage the
  systems without having to pay for an extra user.
icon: user-group-crown
---

# Adding an Unlicensed Admin Account in Google Workspace

{% hint style="info" %}
This guide requires access to a Google Workspace administrator account and **Business Standard** licenses or higher.  The required license settings are not available with **Business Starter.**&#x20;
{% endhint %}

1. **Access Google Admin Console -** Log in to your Google Workspace admin account at [admin.google.com](https://admin.google.com/) using your administrator credentials.
2. **If your organization is already using Nonprofit licensing, skip this step.  To Disable license Auto-Assign:**&#x20;
   * Before adding the new user, you can optionally disable auto-assign for licenses to prevent the automatic assignment (and purchase) of licenses to newly created users. This step ensures that the new user will remain unlicensed until you manually assign a license to them.
   * Navigate to the Admin console and go to _Billing_ > _Subscriptions_ > _License Settings_ > _Manage licensing settings_.
   * Here, you'll find the option to disable auto-assign for licenses. Uncheck the setting to turn off auto-assign. **Save** your changes before proceeding to add the new user.
3. **Add a New User:** &#x20;
   * On the left sidebar, navigate to _Directory_ < _Users._ This will take you to the section where you can manage user accounts.&#x20;
   * At the top, click "_**Add new user**_".  Fill in the required information for the new user. This includes their first name, last name, and the email address you want to assign to them.&#x20;
   * Make sure to record the username and password so you can give that to the new admin.&#x20;
4. **Make the new user a 'Super Admin'** &#x20;
   * In the left sidebar to _Account_ < _Admin Roles_, _Super Admin_.  Click the _Admins_ pane, and then "Assign users".   Search for and find the user you created and click "_ASSIGN ROLE._"&#x20;

Be sure to provide the login information to the new admin, and recommend that they configure multifactor authentication as soon as possible. For more on that topic, see this article:&#x20;

{% content-ref url="enabling-multi-factor-authentication-mfa-enforcement-in-google-workspace.md" %}
[enabling-multi-factor-authentication-mfa-enforcement-in-google-workspace.md](enabling-multi-factor-authentication-mfa-enforcement-in-google-workspace.md)
{% endcontent-ref %}
