---
icon: cloudflare
---

# Logging Into Cloudflare Zero Trust

## :checkered\_flag: Prerequisites

* Cloudflare Zero Trust must be configured for your organization
* You must know your organization's **Cloudflare Team Name.** If you don't, contact your IT administrator.&#x20;

{% tabs %}
{% tab title="Computer" %}
#### Step 1: Download & Install the App

* **Download** the [Cloudflare WARP (1.1.1.1) app](https://1.1.1.1/) on your device. &#x20;
*   Launch the executable file and click through the screens to complete the installation.&#x20;

    <figure><img src="../../.gitbook/assets/image (16).png" alt="" width="375"><figcaption></figcaption></figure>

#### Step 2: Open the Cloudflare WARP app and Sign In

* Launch the Cloudflare app on your computer.
* In the bottom right, click WARP's tray icon. ![](<../../.gitbook/assets/image (29).png>)
* Go to the settings icon, then **Preferences**. &#x20;

<figure><img src="../../.gitbook/assets/image (30).png" alt="" width="178"><figcaption></figcaption></figure>

* Then go to **Account** < **Login with Cloudflare Zero Trust**.

<figure><img src="../../.gitbook/assets/image (31).png" alt="" width="375"><figcaption></figcaption></figure>

* Type in the **Cloudflare team name**
* You will be prompted to log in using whatever method your IT department has configured.&#x20;

#### Step 3: Enable Protection & Verify Connection

* Click on the tray icon. Turn on the service by clicking the big button that is displayed.&#x20;
* Once enabled, you can verify your connection is secure.&#x20;

<figure><img src="../../.gitbook/assets/image (15).png" alt="" width="221"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Mobile Device" %}
#### Step 1: Download the App

* _**Android**_: Go to the Google Play Store, search for "[Cloudflare One Agent](https://play.google.com/store/apps/details?id=com.cloudflare.cloudflareoneagent)," and install.
* _**iPhone**_: Access the App Store, find "[Cloudflare One Agent,](https://apps.apple.com/th/app/cloudflare-one-agent/id6443476492)" and download.

#### Step 2: Open Cloudflare One Agent and Sign In

* Launch the app on your device after installation. &#x20;
* It will ask you for your organization's team name, which your IT administrator can provide.&#x20;
* Enter your Cloudflare credentials or use SSO through Google or Microsoft (depending on your organization) to log in.

#### Step 3: Enable Protection & Verify Connection

* Turn on the service as directed by the app. This typically involves enabling a VPN profile to route your traffic through Cloudflare's secure network, as well as enabling notifications.
* Make sure you’re connected by checking the app's status. You should see an indication that you are protected.
{% endtab %}
{% endtabs %}









