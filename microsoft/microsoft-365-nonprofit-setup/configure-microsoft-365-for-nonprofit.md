---
description: >-
  This page will outline the first steps and best settings for configuring
  Microsoft 365 for your nonprofit.
icon: screwdriver-wrench
---

# Configure Microsoft 365 for Nonprofit

## :checkered\_flag: Prerequisites

**Once your nonprofit has been approved for Microsoft 365 nonprofit licensing, you can continue through this process.** You can verify your organization's nonprofit status with Microsoft [using this guide.](how-to-apply-for-free-nonprofit-microsoft-365-services.md)

## :white\_check\_mark: Get Free Microsoft 365 Nonprofit Licenses

Follow these step-by-step instructions to provision licenses for your organization. This will provide you with access to a variety of Microsoft 365 services and tools.

* Go to the Microsoft 365 admin portal by visiting [**admin.microsoft.com**](https://admin.microsoft.com/) and sign in using your administrator account credentials.
* In the left-hand menu, click on "**Billing**." This will take you to the billing overview page.
* Within the billing overview, click on "**Purchase services**" from the top navigation menu.
* On the Purchase Services page, you'll see a list of available services and licenses for your organization. Search or scroll for the licenses that are designated for nonprofits and are FREE, which include the below licenses.&#x20;

{% include "../../.gitbook/includes/microsoft-365-licenses-free-for-nonprofits.md" %}

## :zap:**Assign Licenses to Users**

After purchasing licenses, you'll need to assign them to specific users within your nonprofit organization.&#x20;

* Go to the "[**Licenses**](https://admin.microsoft.com/#/licenses)" section in the Microsoft 365 admin portal
* Select a license
* Click "Assign licenses" to choose which users should get that license.

You can also assign licenses directly to users from the [Users screen](https://admin.microsoft.com/#/users) of the Microsoft Admin portal.&#x20;

## :earth\_americas: Add your Domain

Your domain operates a lot of the key features within Microsoft 365.  Adding your domain is the very first step to properly configuring Microsoft 365.&#x20;

Follow this guide to add your domain in Microsoft 365: [https://learn.microsoft.com/en-us/microsoft-365/admin/setup/add-domain?view=o365-worldwide](https://learn.microsoft.com/en-us/microsoft-365/admin/setup/add-domain?view=o365-worldwide)

## :e-mail: Email Protection

**Microsoft Defender for Office 365** - [Good Heart Tech](https://goodhearttech.org) strongly recommends adding this to enhance email security. This adds Anti-Phishing, Safe Attachments, and Safe Links functionality and is included in several M365 packages.  To enable these features in a few easy clicks:&#x20;

* Log in to the security portal and navigate to _Email & Collaboration < Policies & Rules < Threat Policies_ < **Preset security policies**: [https://security.microsoft.com/presetSecurityPolicies](https://security.microsoft.com/presetSecurityPolicies)
* Turn on the **Standard protection** by completing the short setup wizard.&#x20;

## :link: DNS Email Security

See this guide for more information on how to protect you Microsoft 365 environment using DNS email send validation technologies like SPF, DKIM, and DMARC:&#x20;

{% content-ref url="../../tech-guides/domain-and-dns/email-sender-validation-using-dns-spf-dkim-and-dmarc.md" %}
[email-sender-validation-using-dns-spf-dkim-and-dmarc.md](../../tech-guides/domain-and-dns/email-sender-validation-using-dns-spf-dkim-and-dmarc.md)
{% endcontent-ref %}

## :art: Organization Theme

Adding logos and personalizing your tenant is not just for a great user experience. It also increases security by letting users know they are signing into the right place.&#x20;

#### Customize the top bar/theme for 365 via the admin center

* Navigate to this link: [https://admin.microsoft.com/Adminportal/Home?#/Settings/OrganizationProfile/:/Settings/L1/CustomThemes](https://admin.microsoft.com/Adminportal/Home#/Settings/OrganizationProfile/:/Settings/L1/CustomThemes)
* Upload the logo that'll appear in the top left of the navigation menu in Microsoft.  Choose an appropriate color scheme. The settings will tell you if the colors are not contrasting enough.&#x20;

#### Add Logo To Azure AD

Add graphics and support message to the sign-in screen [via Azure from this screen](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/LoginTenantBranding):&#x20;

* For the sign-in background, create an image that is 1920x1080 pixels and place the logo in the middle. Upload that for the background.&#x20;
* For the company logo, save a small version of the logo and upload it.&#x20;

## :speech\_balloon: Set up Microsoft Teams

Add default meeting policy in teams admin center to allow sharing and joining from everyone

* [https://admin.teams.microsoft.com/policies/meetings](https://admin.teams.microsoft.com/policies/meetings)
* Edit any other settings you wish to change.&#x20;
* Then apply the policy to “All users”

## :open\_file\_folder: Setup SharePoint

* Edit the default SharePoint site to show the document library
  * [https://admin.microsoft.com/Adminportal/Home#/alladmincenters](https://admin.microsoft.com/Adminportal/Home#/alladmincenters)
* Set the default SharePoint Home site under SharePoint Admin < Settings < Home Site.&#x20;

## :key: Security Settings

The MOST critical security setting: **Enable Multi-factor authentication (MFA)**

[Security Defaults](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/security-defaults) are enabled by default for all new Microsoft tenants. Find out more here:

{% content-ref url="nonprofit-admin-guide-to-enforcing-mfa-in-microsoft-365.md" %}
[nonprofit-admin-guide-to-enforcing-mfa-in-microsoft-365.md](nonprofit-admin-guide-to-enforcing-mfa-in-microsoft-365.md)
{% endcontent-ref %}

### Other Security Settings

* Update Security Settings in these sections at your discretion:  [https://security.microsoft.com/securitysettings](https://security.microsoft.com/securitysettings)
* Disable user app registrations: [https://portal.azure.com/#blade/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/UserSettings](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/UserSettings)
* Restrict SharePoint sharing access with 'everyone' without sign-in: [https://portal.office.com/Adminportal/Home#/Settings/Services/:/Settings/L1/Sites](https://portal.office.com/Adminportal/Home#/Settings/Services/:/Settings/L1/Sites)

## :green\_book: Misc. Recommended Settings:

* Disable Microsoft End-User communication - [https://admin.microsoft.com/Adminportal/Home?#/Settings/Services/:/Settings/L1/EndUserCommunications](https://admin.microsoft.com/Adminportal/Home#/Settings/Services/:/Settings/L1/EndUserCommunications)
* Disable Skype deployment in office settings (Settings < Org < Office install options) - [https://portal.office.com/Adminportal/Home#/Settings/Services/:/Settings/L1/SoftwareDownload](https://portal.office.com/Adminportal/Home#/Settings/Services/:/Settings/L1/SoftwareDownload)
* Adjust News settings - Select industry, topic (Nonprofit corporation), and disable daily news updates:
  * [https://admin.microsoft.com/Adminportal/Home?#/Settings/Services/:/Settings/L1/BingNews](https://admin.microsoft.com/Adminportal/Home#/Settings/Services/:/Settings/L1/BingNews)
  * Select Microsoft 365 as a feed, and disable daily digest.&#x20;
