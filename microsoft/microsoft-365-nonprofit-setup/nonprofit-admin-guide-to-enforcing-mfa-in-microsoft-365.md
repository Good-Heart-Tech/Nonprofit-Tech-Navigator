---
description: >-
  MFA is a critical component of cloud services that helps keep your org safe.
  Admins can enable it for Microsoft 365 with ease using this guide.
icon: lock-keyhole
---

# Nonprofit Admin Guide to Enforcing MFA in Microsoft 365

To enable MFA, admins have two choices: [**Security Defaults**](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/security-defaults) vs. [**Conditional Access Policies**](https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/overview)**.**&#x20;

**For Nonprofits:** Choose [**Security Defaults**](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/security-defaults) for simplicity and basic protection, ideal for smaller nonprofits. Opt for [**Conditional Access Policies** ](https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/overview)for tailored security and precise control, suited for larger nonprofits with IT support.

### **Security Defaults**

[Security Defaults](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/security-defaults) are enabled by default for all new organizations as of 2022. This automatically enforces multi-factor authentication for all users and ensures baseline security measures are in place. It's an efficient option for nonprofits seeking a simple and quick way to enhance their security posture.

* **Pros:** Quick setup, basic protection, simplicity.
* **Cons:** Limited customization, minimal controls, not for larger nonprofits.
* **How to enable Security Defaults:**
  * In the [Entra ID portal,](https://entra.microsoft.com/) navigate **Identity in the sidebar**, then to the **Properties** tab.
  * From there, scroll to the bottom and select **Manage Security Defaults.**
  * Finally, choose **Enabled** and save. &#x20;

### **Conditional Access Policies**

[Conditional Access Policies](https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/overview) enable nonprofits to customize access controls based on factors like user location, device type, and sign-in risk. This advanced feature lets organizations require multi-factor authentication, restrict access, or enforce security measures selectively, providing tailored protection for different scenarios and user groups.

* **Pros:** Customized protection, detailed control, flexibility.
* **Cons:** Configuration effort, complexity, learning curve.
* **How to enable:**
  * Review the requirements you want to put in place.&#x20;
  * [Use this guide to deploy your own ](https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/overview)custom conditional access policies.&#x20;

