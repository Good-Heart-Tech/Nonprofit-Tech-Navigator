# 🔓 Security Recommendations for Nonprofits

Strong security doesn’t have to be complicated or expensive. Nonprofits can make a significant impact by focusing on a few proven practices that block the majority of attacks. The recommendations below highlight practical tools and configurations—like multi-factor authentication, DNS protections, and free assessments—that any nonprofit team can implement to reduce risks and safeguard their mission.

## Multi-factor Authentication (MFA) <a href="#multi-factor-authentication0" id="multi-factor-authentication0"></a>

{% hint style="info" %}
Interested in FREE hardware MFA tokens for your nonprofit?  Check out: [mfa-security-token.md](../hardware/mfa-security-token.md "mention")
{% endhint %}

Multi-factor authentication (MFA/2FA) should be enforced in as many systems as possible. Forcing users to use this ensures attackers can't log in using only a stolen password. For many years, this has remained the most critical security recommendation any IT provider makes, and for good reason. For example, [99.9% of compromised accounts in Microsoft did not use multi-factor authentication.](https://www.zdnet.com/article/microsoft-99-9-of-compromised-accounts-did-not-use-multi-factor-authentication/) The need for this cannot be overstated.&#x20;

## DNS Security <a href="#dns-security2" id="dns-security2"></a>

[**DNS Email security**](https://support.google.com/a/topic/9061731?hl=en\&ref_topic=9202) is an essential part of email services that are often neglected by smaller nonprofits. [SPF](https://support.google.com/a/topic/10685331?hl=en\&ref_topic=9061731), [DMARC](https://support.google.com/a/topic/2759254?hl=en\&ref_topic=9061731), and [DKIM](https://support.google.com/a/topic/2752442?hl=en\&ref_topic=9061731) work together to provide secure and reputable email delivery for a domain. All three enable helps your brand reputation and ensure other people get your emails. Feel free to reach out to us to [get help setting these up](https://goodhearttech.org/contact). SPF and DKIM technologies can be easily configured for Google and Microsoft email services, and we recommend [Cloudflare](https://blog.cloudflare.com/dmarc-management/) for free DMARC services. &#x20;

{% content-ref url="../../tech-guides/domain-and-dns/email-sender-validation-using-dns-spf-dkim-and-dmarc.md" %}
[email-sender-validation-using-dns-spf-dkim-and-dmarc.md](../../tech-guides/domain-and-dns/email-sender-validation-using-dns-spf-dkim-and-dmarc.md)
{% endcontent-ref %}

### DNSSEC

DNSSEC (Domain Name System Security Extensions) enhances the security of the Internet's Domain Name System (DNS). By digitally signing DNS data, it safeguards against DNS hijacking and ensures that users are directed to legitimate websites. This boosts online trust, safeguards data integrity, and reduces the risk of cyberattacks.  If you purchased your domain through Cloudflare, you can easily enable it [using this guide](https://developers.cloudflare.com/dns/dnssec/#enable-dnssec).

## Free Microsoft Cybersecurity Self-Service Assessment

Microsoft offers a free [Cybersecurity Self-Service Assessment tool](https://portal.selfserviceassessment.com/) for IT admins with full administrator privileges. This tool provides a comprehensive evaluation of an organization's cybersecurity posture, offering valuable insights and actionable recommendations. For nonprofits, this tool is particularly beneficial as it can help identify vulnerabilities and prioritize security measures, ensuring the protection of sensitive data and resources. The user-friendly interface and clear, well-structured report make it easy to understand the assessment results and implement recommended improvements.

## **Improving Security Awareness and Readiness with Backdoors & Breaches**

[Backdoors & Breaches](https://www.blackhillsinfosec.com/tools/backdoorsandbreaches/) is a tabletop exercise tool that enhances security awareness and incident response preparedness for organizations. It simulates real-world cyberattacks, allowing teams to practice identifying, mitigating, and recovering from security incidents. The tool helps evaluate security policies, test communication workflows, and identify gaps in defenses, improving response strategies. By engaging in realistic scenarios, organizations can foster a proactive security culture and strengthen their incident response readiness without complex or costly simulations. [Click here to play for free.](https://play.backdoorsandbreaches.com/)
