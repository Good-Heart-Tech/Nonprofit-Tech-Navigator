---
description: >-
  This document will show you how to configure the Endpoint Protection solution
  Microsoft Defender for your nonprofit.
icon: file-shield
---

# Configure Microsoft Defender for Endpoint for Nonprofit (Antivirus)

{% hint style="info" %}
This uses the premium version of Microsoft Defender, which is included in the free licenses granted to nonprofits. More info here:[how-to-apply-for-free-nonprofit-microsoft-365-services.md](how-to-apply-for-free-nonprofit-microsoft-365-services.md "mention")
{% endhint %}

## **Microsoft 365 Defender for Endpoint Setup**

* Go to [this Onboarding page](https://security.microsoft.com/onboard) to start enabling features, and wait until it reloads and redirects you to the dashboard.  This can take 5-15 minutes. [https://security.microsoft.com/onboard](https://security.microsoft.com/onboard)
* Open this [policy management link](https://security.microsoft.com/policy-management) in a new tab and walk through the wizard (if prompted), skipping all the steps that ask you to assign roles and notifications: [https://security.microsoft.com/policy-management](https://security.microsoft.com/policy-management)
* Cache-clear refresh the page (Crtl + Shift + R) to ensure all menu options are revealed.&#x20;
* Navigate to: [**Settings** > **Endpoints** >**Advanced features**](https://security.microsoft.com/preferences2/integration).  Enable the following:
  * _**Microsoft Defender for Cloud Apps**_
  * _**Unified audit log**_
  * _**Share endpoint alerts with Microsoft Compliance Center**_
  * _**Microsoft Intune connection**_
  * Save your changes.
* Verify [in the Intune Portal](https://intune.microsoft.com/#view/Microsoft_Intune_Workflows/SecurityManagementMenu/~/atp) that the connection to the Defender portal is active.  **Endpoint Security < Microsoft Defender for Endpoint**
  * **Connection Status** _should be_ **Enabled**
  * If it does **not** say **Enabled**:&#x20;
    * Go back to the Security/Defender portal, and [**Settings** > **Endpoints** >**Advanced features**](https://security.microsoft.com/preferences2/integration). and toggle the _**Microsoft Intune connection**_ OFF, Save, then toggle it back on again and Save.&#x20;

Next, you need to configure policies for the following, in the Intune portal:&#x20;

* AV Policy
* ASR Policy
* EDR Policy

{% hint style="info" %}
The Good Heart Tech team has the automation and skillset to enable the seamless deployment of all of the above settings and policies. Contact us if you need assistance with deployment.
{% endhint %}
