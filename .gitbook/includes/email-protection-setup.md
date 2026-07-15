---
title: Email Protection Setup
---

## The following settings should be applied and can be adjusted based on your organization's needs.

# Gmail Safety Settings

These settings can be found in the [**Google Admin portal**](https://admin.google.com) under [**Apps** > **Google Workspace** > **Gmail** > **Safety**.](https://admin.google.com/ac/apps/gmail/safety)

* Attachments
  * Protect against encrypted attachments from untrusted senders = **OFF** (ON by default)
  * Protect against attachments with scripts from untrusted senders = ON
  * Protect against anomalous attachment types in emails = **ON** (OFF by default)
  * Apply future recommended settings automatically = ON
* IMAP view time protections
  * Enable IMAP link protection = **ON** (OFF by default)
* Links and external images
  * Identify links behind shortened URLS = ON
  * Scan linked images = ON
  * Show warning prompt for any click on links to untrusted domains = ON
  * Apply future recommended settings automatically = ON
* Spoofing and authentication
  * Protect against domain spoofing based on similar domain names = ON
  * Protect against spoofing of employee names = ON
  * Protect against inbound emails spoofing your domain = ON
  * Protect against any unauthenticated emails = **ON** (OFF by default)
  * Protect your Groups from inbound emails spoofing your domain = **ON** (OFF by default)
  * Apply future recommended settings automatically = ON

# End User Access Settings

These settings can be found in the [**Google Admin portal**](https://admin.google.com) under [**Apps** > **Google Workspace** > **Gmail** > **End User Access**.](https://admin.google.com/ac/managedsettings/740348119625)

* **Disable POP**: Under **POP and IMAP Access**, _uncheck_ **Enable POP access for all users** to disable it.
* _**(Optional**_**) Disable IMAP**: If you want to increase security, you can force people to use the Gmail web app and prevent people from using apps like Microsoft Outlook to manage thier email. This greatly increases security. Under **POP and IMAP Access**, _uncheck_ **Enable IMAP access for all users** to disable it.
* **Google Workspace Sync**: On
* (_**Optional**_**) Disable External Recipients Warning:** At the bottom of the page, uncheck **Warn for external recipients** to disable it.
* **Emoji Reactions**: On

# Spam, phishing, and malware settings

These settings can be found in the [**Google Admin portal**](https://admin.google.com) under [**Apps** > **Google Workspace** > **Gmail** > **Spam, phishing, and malware.**](https://admin.google.com/ac/apps/gmail/spam?setting=86)

* Enable _Enhanced malware & phishing protection_
* Enable _Security sandbox_
