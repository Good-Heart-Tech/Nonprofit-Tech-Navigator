---
icon: cloudflare
---

# Cloudflare Zero Trust Setup

## :closed\_lock\_with\_key: What is  Zero Trust?

[Cloudflare Zero Trust](https://www.cloudflare.com/zero-trust/) is a security approach that ensures trust verification for every user and device, wherever they are. It boosts security by confirming identities and **reducing risks in remote work**. It's also cost-effective, offering free access for up to 50 users and easy integration with identity providers like Microsoft or Google.

## :pen\_ballpoint: Sign Up For Cloudflare Zero Trust

* Log in with your [Cloudflare account](https://dash.cloudflare.com/).
* Ensure you have a credit on file. You can't proceed without this, even though Zero Trust is free for 50 users. To add a credit card, navigate to **Billing** > **Payment Info**
  * ![](<../../.gitbook/assets/image (28).png>)
* Navigate back to the [main dashboard](https://dash.cloudflare.com/).&#x20;
* Click on **Zero Trust** on the left sidebar.
* A wizard will launch for you to set up a Cloudflare Team name. Use the name of your organization without spaces. For example, [Good Heart Tech](https://goodhearttech.org/) could be goodhearttech.&#x20;
* Select the **FREE** Plan.&#x20;

## &#x20;:hammer: Setup Zero Trust

Once in the Zero trust portal, setup the rest of the Team and portal and configure the following settings:&#x20;

* Settings < Custom Pages < make a note of the **Team domain**. This is what users will use to log in to Cloudflare Zero Trust using the [WARP client ](https://developers.cloudflare.com/warp-client/)or URL. &#x20;
* Settings < Custom Pages < Login Page < Customize.    &#x20;
  * Set the message to:  _If you are not authorized, close this page immediately._&#x20;
  * (Optional branding) Update the background color and logo URL.
* Settings < Authentication < **Configure Azure AD SSO** according to the Cloudflare Documentation  [https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/azuread/](https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/azuread/)
* If you'd like to integrate Azure AD or another identity provider for signing into Cloudflare Zero Trust, you can use these docs: [Azure AD](https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/azuread/) / [Others](https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/)

## :construction\_site: Setup Access Group, Tunnels, & Applications

### Access Group

Access groups allow organizations to create specific access policies based on user roles, devices, and locations. This enhances security by ensuring that only authorized individuals can access sensitive data, applications, and services.

In the Zero Trust Portal, navigate to: **Access** < **Access Groups** < Create an Access group for each group needed, usually just one.  Add in the company email domains. &#x20;

### Tunnels

Cloudflare Tunnels provide a secure and efficient way to connect your infrastructure to Cloudflare's global network. They enable organizations to route traffic through Cloudflare for enhanced performance and security. This ensures that web applications and services remain highly available and protected from online threats.

* In the Zero Trust Portal, navigate to **Network** < **Tunnels** <  + **Create a Tunnel.** Name the tunnel.&#x20;
* Use the code displayed on the screen to install the Tunnel ([cloudflared](https://github.com/cloudflare/cloudflared)) on the server hosting the services.&#x20;
* If configuring APPLICATION access (specific port on a server), do the following:
  * On the first screen, select self-hosted.&#x20;
  * In the **Public hostname** tab of the Tunnel, create an entry for each web-based resource you want to publish to the Zero-Trust portal.  Add a public hostname using a subdomain, and point the application to the correct local host and port.  Creating a public hostname entry creates a public DNS CNAME record.&#x20;
  * For services running without valid SSL certs, check the Do Not Verify TLS option. &#x20;
* If configuring NETWORK access, do the following:&#x20;
  * In the **private network** tab of the Tunnel, specify the IPs that Zero Trust will have access to, typically the whole network.  Example: _192.168.1.0/24_
  * Go to _Settings < WARP Client < Default profile < **Split Tunnels** < Manage_ < and delete the class of IP Addresses that represent the primary corporate network and tunneled resources.&#x20;
  * If you have a local Active Directory domain, you should add the domain to **Local Domain Fallback** setting under _Settings < WARP Client < Default profile._  This ensures that connected agents will use the on-premise DNS options provided by Active Directory but bypasses Cloudflare's logging.&#x20;

## :man\_technologist: Applications

We'll create an application for all applications that are required on the portal (typically all web-based applications). Each application must relate to an existing DNS entry or tunnel public hostname. &#x20;

* Go to Access < Applications < Add an application
* Select Self-Hosted
* Enter the application name, subdomain, domain, and path if applicable.&#x20;
* Enable App in App Launcher
* By default, enable all ID providers unless the client has other requirements. Click **Next**.
* For the Policy, give it a name, then select the **Access Group** you made previously. Hit **Next**.&#x20;
* The last tab, Setup, can be left as-is.&#x20;

## :computer: WARP Client Deployment & Setup

The [Cloudflare WARP client ](https://1.1.1.1/)should be deployed to all PCs that need to connect to the Cloudflare Network and access the internet securely. &#x20;

* Deploy [Cloudflare WARP](https://1.1.1.1/) using your preferred method for software deployment (we like [Chocolatey](https://community.chocolatey.org/packages/warp))
* Have users follow the following steps to configure Zero Trust on endpoints:
  * In the WARP Client, right-click the tray icon and go to **Preferences**.  Then go to **Account** < Login with Cloudflare Zero Trust.
  * Instruct users to log in with their Cloudflare team name, which should be similar to their company name.
