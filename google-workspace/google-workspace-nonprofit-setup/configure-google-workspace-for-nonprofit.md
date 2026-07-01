---
icon: google
---

# Configure Google Workspace for Nonprofit

Each section of this guide will walk you through configuring Google Workspace for your organization, ensuring security and access to critical features.

## :checkered\_flag: Prerequisites

**Once your nonprofit has been approved for nonprofit licensing, you can continue through this process.** You can verify your organization's nonprofit status with Google [using this guide](how-to-apply-for-free-nonprofit-google-workspace-services.md)[.](../../microsoft/microsoft-365-nonprofit-setup/how-to-apply-for-free-nonprofit-microsoft-365-services.md)

{% hint style="info" %}
Almost all of the settings mentioned in this guide are located in the Google Workspace admin portal, located at [https://admin.google.com](https://admin.google.com/ac/domains/manage). An administrator account is required to change these settings.
{% endhint %}

## License setup

You want to confirm your nonprofit plan is active. You also want to add the free device-management subscriptions.

1. Go to **Billing → Subscriptions**: https://admin.google.com/u/1/ac/billing/subscriptions
2. Verify **Google Workspace for Nonprofits** shows a **Free** price.
3. Click **Buy or upgrade**.
4. Add **Chrome Enterprise Core**:
   1. Go to **Devices → Chrome → Chrome Enterprise Core**.
   2. Confirm the **free** subscription.
5. Repeat **Buy or upgrade** for **Android Enterprise** and confirm it is **free**.

{% hint style="warning" %}
If you see a price, stop. Your nonprofit licensing may not be active yet, or you may be in the wrong admin account.
{% endhint %}

When you’re done, your **Subscriptions** page should include all three free subscriptions:

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

## :globe\_with\_meridians: DNS Setup

### Verify the domain and enable email

* Navigate to _Account_ > _Domains_ > _Manage Do&#x6D;_&#x61;ins > _Add a domain_ - [https://admin.google.com/ac/domains/manage](https://admin.google.com/ac/domains/manage)
* Enter the domain name and continue through the guided steps. They will add you to add a TXT record to your DNS host that looks something like this:

```
google-site-verification=mzch0RoooBunchOfLettersAndNumbersjJKmd4e4
```

* Add the record to your DNS host and continue through the wizard. When prompted, add the MX records to your DNS
* Add the MX record in the public DNS to complete the setup:
  * Name: _@_
  * Mail Server: _smtp.google.com_
  * TTL: _Auto_
  * Priority: _1_

Your domain is now email-enabled! In the next sections, we'll make sure it's secure.

### Enable SPF for email security

* To enable SPF, all you need to do is add TXT record in you DNS host. [Craft the SPF record using this article.](https://apps.google.com/supportwidget/articlehome?hl=en\&article_url=https%3A%2F%2Fsupport.google.com%2Fa%2Fanswer%2F10684623%3Fhl%3Den\&assistant_id=generic-unu\&product_context=10684623\&product_name=UnuFlow\&trigger_context=a)
* If you don't have any other services that send email on your domain, you SPF record will look like this:

```
v=spf1 include:_spf.google.com ~all
```

* After you publish the SPF record, no further action is required.

### Enable DKIM for email security

* Enable DKIM on all email domains using this linked process. Make sure to add the correct DKIM record to the public DNS: [https://support.google.com/a/answer/180504?hl=en](https://support.google.com/a/answer/180504?hl=en)
  * **You must wait 24 to 72 hours after enabling Gmail with a registered domain before you can create a DKIM record. Google does this to prevent its platform from being used for spam.**
  * **Changes to DNS take time, be sure to enable DKIM at the end of business hours to avoid disruption of email flow.**

## :e-mail: Email Setup

1. Set up any shared mailboxes ([collaborative inbox from Google Groups](https://support.google.com/a/users/answer/10375787?hl=en)) that will be needed and delegate them to the appropriate users.
2. Migrate any email from other platforms or personal accounts into Google Workspace. If needed, use [Google's guide to assist with moving data](https://support.google.com/a/answer/6003169?hl=en\&ref_topic=6245191) from other platforms.
3.  Enable **Mail Delegation** from Gmail's [User Settings section](https://admin.google.com/ac/apps/gmail/usersettings), which is very helpful for accessing shared mailboxes. \*

    ```
    <figure><img src="/files/EBNsaZwxfYZNt6t4PcKe" alt=""><figcaption></figcaption></figure>
    ```

{% include "../../.gitbook/includes/email-protection-setup.md" %}

## :floppy\_disk: Setup Storage (Google Drive) <a href="#setup-storage0" id="setup-storage0"></a>

#### Setup Shared Drives and Access

* **Enable Shared Drives**_**:**_ Go to _Apps_ < _Google Workspace < Drive and Docs < Manage Shared Drives > Enable shared drives for all users_
* [_**Setup any Shared drives**_ ](https://support.google.com/a/answer/7662202?hl=en)that will be needed within your organization and delegate them to users.
* **Remove storage limits for users**: Go to _Storage_ < _Manage_ < _User Storage Limit_ < Turn _OFF_. This allows user drives and email mailboxes to expand as needed.

#### Migrate Data to Google Drive

Migrate any email from other platforms or personal accounts into Google Workspace. If needed, use [Google's guide to assist with moving data](https://support.google.com/a/answer/6003169?hl=en\&ref_topic=6245191) from other platforms.

## :key: Security Settings

* Ensure that [**multifactor authentication is enforced** ](https://support.google.com/a/answer/9176657?hl=en)across the entire org using this guide:

{% content-ref url="enabling-multi-factor-authentication-mfa-enforcement-in-google-workspace.md" %}
[enabling-multi-factor-authentication-mfa-enforcement-in-google-workspace.md](enabling-multi-factor-authentication-mfa-enforcement-in-google-workspace.md)
{% endcontent-ref %}

* **Password settings** should be adjusted under [_Security_ < _Authentication < Password Management_](https://admin.google.com/ac/security/passwordmanagement?journey=62)
  * Check the box called **Enforce strong password,** and set the **minimum length** to **14 characters.**
  * Set password expiration to **Never expires**
* **Enable Login Challenges** should be enabled under [_Security_ < _Authentication < Login Challenges._](https://admin.google.com/ac/managedsettings/352555445522/loginchallenge) Under _Post-SSO Verification_, select both radio buttons that say **Ask users for additional verifications.**
* **Change third-party app settings** by navigating to [_Security < Access and data control < API Controls < Settings_](https://admin.google.com/ac/owl/settings) _< **Unconfigured third-party apps.**_ We recommend the choice called "**Allow users to access third-party apps that only request basic info needed for Sign in with Google.**" We recommend **not** leaving it on the default setting, which leaves your organization vulnerable to phishing and OAuth attacks using third-party apps.
* [Navigate to this data protection page](https://admin.google.com/ac/dp), which will automatically start provisioning the Security reports for your Google Workspace data for future reference. **Enable all options in the Data protection section at the bottom of this page.**

## Account Settings

All these settings are located under [Account < Account Settings.](https://admin.google.com/ac/accountsettings)

* **Enable Google Cloud Data Sharing**: Navigate to [_Account settings < Legal & Compliance_](https://admin.google.com/ac/companyprofile/legal)_,_ and mark Google Cloud Platform Sharing Options as **Enabled**.
* **Accept Cloud Data Processing Agreement**: Navigate to [_Account settings < Legal & Compliance_](https://admin.google.com/ac/companyprofile/legal)_,_ and under _Cloud Data Processing Addendum (CDPA)_, click **Review & Accept**.
* **Enable Conflicting Accounts Management**: Navigate to [_Account settings < Conflicting accounts management_](https://admin.google.com/ac/accountsettings/conflictaccountmanagement), then select '_Automatically invite users to transfer conflicting unmanaged accounts to managed ones_' and set the '_Send daily follow-up emails for_' to **2 weeks.** Select the sub option for **Replace their conflicting account with a managed one**
* Review and apply security settings in the Security < [Security Advisor](https://admin.google.com/u/1/ac/security/home). Apply as many of the recommendations as possible for your organization.
* **Disable Google Communications:** Under [Account Settings < Preferences < Email](https://admin.google.com/ac/accountsettings/preferences), disable all communications that would be sent from Google to end users.
* Enable _all_ **Smart Features** [from this page](https://admin.google.com/ac/accountsettings/smartfeatures).
* :art: Personalize your Google Workspace organization by uploading **y**our organization's logo: [_**Account**_ < _**Account settings**_ < _**Personalization**_](https://admin.google.com/ac/companyprofile/personalization) and upload the logo.

## :book: Directory Settings

We recommend the following settings Directory settings for Google Workspace:

| Setting Location with Link                                                                                                                         | Instructions                                                                                                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Directory < Directory Settings](https://admin.google.com/ac/managedsettings/986128716205/sharing) < Sharing Settings < Contact Sharing            | <p>Choose:<br>- <em><strong>Show all email addresses</strong></em><br>AND<br><strong>- </strong><em><strong>Show both domain profiles and domain shared contacts</strong></em></p> |
| [Directory < Directory Settings](https://admin.google.com/ac/managedsettings/986128716205/sharing) < Sharing Settings < External Directory sharing | Choose _**Authenticated user basic profile fields**_                                                                                                                               |
| [Directory < Directory Settings < **Visibility settings**](https://admin.google.com/u/1/ac/settings/directory/visibility)                          | Choose _**All users**_                                                                                                                                                             |
