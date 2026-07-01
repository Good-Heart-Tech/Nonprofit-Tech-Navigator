---
icon: envelope-circle-check
---

# Email Sender Validation Using DNS (SPF, DKIM, & DMARC)

Several DNS-reliant technologies can be used to help validate the authenticity of email. This article will describe how to configure each of these technologies to ensure security for your organization.   **We recommend enabling these services for all your domains wherever possible.** When configured correctly, these services all work together and help ensure emails sent from a client's environment are delivered successfully to recipients without getting caught in spam filters.&#x20;

{% hint style="info" %}
DNS changes can take time to take effect. To avoid disruption, we recommend making DNS changes at the end of working hours.
{% endhint %}

## Testing Your Current Configuration

To test which of these technologies is currently in place for your organization, type in your domain using [our Domain & DNS Health Check tool](https://dns.nonprofittools.org/).  Then, come back here to the sections that need attention.&#x20;

## **SPF (Sender Policy Framework)**

SPF records tell spam filters what mail services a particular domain name typically sends emails from. It's **essential** to have a correctly configured SPF record that lists any mail-sending servers. This includes any hosted mail server environments (Microsoft 365, Google Workspace, etc.), third-party mailing list services (website, MailChimp, HubSpot, Constant Contact, etc.), and external IP addresses of any sites with on-premise devices or servers sending mail (local Exchange servers, scanners, etc.). These services must be identified before an accurate record can be generated. Each third-party service should provide details on what to include in an SPF record for their particular environment. These must be combined into a single correctly formatted TXT record in the DNS zone of each domain used to send mail.

### Google Workspace SPF Setup

*   When using **Google Workspace,** [always use the '_soft fail_'](https://support.google.com/a/answer/10684623?hl=en) parameter (the "\~" character) near the end of the SPF record.   For example, your SPF record for Google Workspace should look like this:

    ```
    v=spf1 include:_spf.google.com ~all
    ```

### Microsoft 365 SPF Setup

When using **Microsoft 365**, use the '_hard fail_' parameter at the end of the SPF record: **-all**

*   For example, the SPF record should look like this:&#x20;

    ```
    v=spf1 include:spf.protection.outlook.com -all
    ```
* And NOT these:
  * v=spf1 include:spf.protection.outlook.com **?**&#x61;ll
  * v=spf1 include:spf.protection.outlook.com all _(this typo allows email from everywhere!)_
  * v=spf1 include:spf.protection.outlook.com

{% hint style="info" %}
Microsoft [recommends the '_hard fail_' parameter](https://learn.microsoft.com/en-us/defender-office-365/email-authentication-spf-configure), but '_soft fail_' parameter (the "\~" character instead of "-") also works and [may be more helpful](https://www.mailhardener.com/blog/why-mailhardener-recommends-spf-softfail-over-fail) for some organizations in allowing third parties to send emails on your behalf.&#x20;
{% endhint %}

{% embed url="https://mxtoolbox.com/dmarc/spf/setup/how-to-setup-or-modify-spf" %}

{% embed url="http://www.open-spf.org/SPF_Record_Syntax/" %}

## **DKIM (DomainKeys Identified Mail)**

[DKIM ](https://dmarcian.com/what-is-dkim/)signs each message that leaves the mail server so the destination server knows that the message came from the sender's organization.  Luckily, DKIM is easy to configure with Microsoft 365 and Google Workspace.&#x20;

### Microsoft 365 DKIM Setup

Enable DKIM on all your domains using [the DKIM wizard in the Microsoft admin security center.](https://security.microsoft.com/dkimv2) Follow the instructions for adding DNS records to your DNS host.&#x20;

{% hint style="info" %}
Microsoft's default domains (_onmicrosoft.com_ domains) have DKIM set up by default.
{% endhint %}

### Google Workspace DKIM Setup

Enable DKIM on all email domains by following this[ article from Google Support.](https://support.google.com/a/answer/180504?hl=en) &#x20;

{% hint style="info" %}
After enabling Gmail with a registered domain, you must wait 24 to 72 hours before you can create a DKIM record.  Google does this to prevent its platform from being used for spam. &#x20;
{% endhint %}

## DMARC (Domain-based Message Authentication, Reporting, and Conformance)

DMARC is the technology that allows for message traversal reporting and builds upon both SPF and DKIM.  DMARC is important to implement, especially for email reputation.&#x20;

### DMARC Using Cloudflare

**We recommend configuring** [**DMARC through Cloudflare**](https://developers.cloudflare.com/dmarc-management/)**.**   Cloudflare will automatically create the correct DMARC record for you. &#x20;

* [Sign in to your Cloudflare account](https://dash.cloudflare.com/) where your domain already exists, and DNS is being managed.&#x20;
* In the Cloudflare dashboard sidebar, navigate to **Email >** **DMARC Management**
* **Click Enable DMARC Management:** ![](<../../.gitbook/assets/image (39).png>)
* Click **Add**.
* By default, the policy is deployed in 'none' mode (report-only).  We recommend increasing this security by simply replacing '_**none**_' with '_**quarantine**_' in the TXT DMARC record that was just created under **DNS** > **Records**.&#x20;

### Setup DMARC Manually

* When creating a DMARC DNS record manually, you specify a policy. We recommend deploying the DMARC TXT record with the "quarantine" policy,
  * Create a TXT (text) record with '**\_dmarc**' as the name/target.&#x20;
  * The content of the TXT record should be as follows:
    * _v=DMARC1; p=_**quarantine**_; rua=mailto:your\_reporting\_email\_address@here.com_
  * The policy can optionally be increased to '**reject**' if higher security is needed.&#x20;

{% embed url="https://support.valimail.com/support/solutions/articles/48001147676-dmarc-strict-vs-relaxed-alignment" %}

## DNSSEC (Domain Name System Security Extensions)

{% hint style="info" %}
We only recommend using DNSSEC if your domain is registered with Cloudflare. Avoid enabling DNSSEC at other providers unless you are willing to manually rotate DNSSEC keys and have in-depth IT knowledge.
{% endhint %}

### Enabling DNSSEC in Cloudflare

To enable DNSSEC for domains registered with Cloudflare:

1. **Log into your Cloudflare account** and navigate to the domain you wish to secure.
2. In the **DNS** section, locate and click on **DNSSEC**.
3. Click **Enable DNSSEC.**

## _Optional_ - MTA-STS (SMTP MTA Strict Transport Security)

SMTP MTA Strict Transport Security (MTA-STS) helps ensure that email communications are encrypted during transmission, significantly reducing the risk of interception or tampering. This is particularly important for nonprofits using Google Workspace or Microsoft 365 to protect sensitive information and maintain trust with their collaborators. These instructions require the use of our [preferred DNS host, Cloudflare](../../tech-recommendations/it-management-and-security-solutions/website-and-dns-services-for-nonprofits.md).  Follow these steps to deploy MTA-STS:

* Download this file to your computer and extract the contents: &#x20;
  * [Click here for **Microsoft 365** ](https://drive.google.com/file/d/1i7ZX_IrxUVXfN59AT7TXh__NFiSHyWwF/view?usp=sharing)
  * [Click here for **Google Workspace**](https://drive.google.com/file/d/1gmo9WD7RKsRzEN3uumJqxQfZSamnWDne/view?usp=sharing)
* Login to Cloudflare and navigate to the R2 storage service.&#x20;
* Create a new bucket in Cloudflare R2 and name it: _**mta-sts**_
  * Upload the FOLDER called "_.well-known_" that you extracted in step 1 to the new bucket.&#x20;
  * Under the bucket's **Settings** tab, click _Connect Domain_. &#x20;
  * Specify the subdomain **mta-sts**. Cloudflare will initialize the domain, which can take 5-10 minutes. Then the file will be available at [https://mta-sts._**yourdomain.org**_/.well-known/mta-sts.txt](https://mta-sts.yourdomain.org/.well-known/mta-sts.txt)
  * In the bucket **Settings** tab, find **CORS Policy**.  Click **Add CORS Policy** and replace the content with the text below.  This ensures that all viewers, including bots, can read the policy file.&#x20;

```
[{"AllowedOrigins":["*"],"AllowedMethods":["GET"],"AllowedHeaders":["*"],"MaxAgeSeconds":3600}]
```

* Finally add **both** of the following TXT records to your DNS configuration in Cloudflare:
  * **Create TXT record for MTA-STS**
    * Name: `_mta-sts`
    * Value: `v=STSv1; id=20220101000000Z;`
  * **Create TXT record for TLSRPT**
    * Name: `_smtp._tls`
    * Value: `v=TLSRPTv1;`

## Vanity or Parked Domains

Vanity or parked domains are extra domains acquired to safeguard an organization's brand and likeness but not actively utilized for any services, including email. Best practice involves prohibiting email sending on vanity or parked domains. Use **all** of the following DNS records to prohibit email sending on a domain:

| **Protocol or Standard** | **Record Type** | **Name**       | **Value**           | **Priority** |
| ------------------------ | --------------- | -------------- | ------------------- | ------------ |
| **SPF**                  | TXT             | @              | v=spf1 -all         |              |
| **DMARC**                | TXT             | \_dmarc        | v=DMARC1; p=reject; |              |
| **DKIM**                 | TXT             | \*.\_domainkey | v=DKIM1; p=         |              |
| **MX**                   | MX              | @              | **.**               | 0            |

{% hint style="info" %}
_Not all DNS hosts support wildcards in public DNS records, so the DKIM restriction may not always be possible._
{% endhint %}

