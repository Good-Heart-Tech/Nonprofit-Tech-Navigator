---
description: >-
  Good Heart Tech's recommended IT checklist when staff or volunteers join or
  leave—accounts, email, devices, and access.
icon: user-check
---

# Employee Onboarding & Offboarding (IT Checklist)

Staff, contractors, interns, and **volunteers** who use your email, files, or apps need predictable **join** and **leave** steps. Good Heart Tech recommends treating onboarding and offboarding as a short, repeatable checklist—not ad hoc inbox fixes after someone has already left.

{% hint style="info" %}
**Your organization decides what applies.** Board policy, HR, legal, grants, and HIPAA or other rules may require **more** or **fewer** steps than this list—and different **timing** (for example, immediate account suspension vs. a two-week mail forward). Use this page as a starting template and document your own standard in your employee handbook or IT runbook.
{% endhint %}

{% hint style="warning" %}
**Good Heart Tech partners:** We can help with many of these tasks, but we do **not** guarantee complete offboarding or compliance. **Your organization** owns HR decisions and final account actions in your admin consoles. [Submit a support ticket](../../other-nonprofit-resources/nonprofit-partner-resources/how-to-submit-a-support-ticket-to-good-heart-tech.md) when you need hands-on help.
{% endhint %}

**Related:** [User naming conventions](user-naming-conventions-for-email-and-identity-systems.md) · [Why MFA is crucial](../../tech-guides/security-guides/why-mfa-is-crucial-for-nonprofits.md) · Google: [Groups & shared email](../../google-workspace/google-workspace-nonprofit-user-guides/google-groups-and-shared-email-options.md) · Microsoft: [Managing licenses](../../microsoft/microsoft-365-nonprofit-setup/managing-nonprofit-licenses-in-the-microsoft-365-admin-center.md)

---

## Onboarding (joining the organization)

Goal: the person can work **safely** on day one—without excess access they do not need yet.

| Area | Recommended actions |
| --- | --- |
| **Identity & email** | Create a Google Workspace or Microsoft 365 user using your [naming convention](user-naming-conventions-for-email-and-identity-systems.md). Assign the right **license**. Set a strong temporary password or send an invite; require **password change** on first sign-in. |
| **Sign-in security** | Enforce **MFA** before they access email or sensitive data. See [Google MFA enforcement](../../google-workspace/google-workspace-nonprofit-setup/enabling-multi-factor-authentication-mfa-enforcement-in-google-workspace.md) or [Microsoft MFA enforcement](../../microsoft/microsoft-365-nonprofit-setup/nonprofit-admin-guide-to-enforcing-mfa-in-microsoft-365.md). |
| **Groups & access** | Add them only to **mailing lists, Google Groups, Teams, and Shared drives** they need. Default to **least privilege**; expand access when their role requires it. |
| **Shared mailboxes & delegation** | If they will handle **info@** or a queue, add them as a **Gmail delegate** or grant **Shared mailbox / Full Access** in Microsoft 365—not a shared password. |
| **Devices** | Issue or record an org-owned PC. Install OS updates, endpoint protection, and (for GHT partners) [support tools](../../other-nonprofit-resources/nonprofit-partner-resources/install-good-heart-techs-support-tools-on-your-computer.md) if applicable. |
| **Passwords & SaaS** | Invite them to your org **password manager** (if you use one). Create accounts in donor CRM, accounting, website CMS, etc., **per role**—avoid “everyone is admin.” |
| **Training & policy** | Share acceptable-use, phishing awareness, and [separate work/personal browser profiles](../../tech-guides/software-guides/how-to-use-separate-chrome-and-edge-profiles-for-work-and-personal.md) if they use a personal computer for any org work. |

**Examples (onboarding)**

* New program manager: **M365 license**, **Marketing** group, **SharePoint** site member, **no** finance folder until payroll approves.
* Volunteer coordinator (part-time): **Google account**, **volunteers@** collaborative inbox member, **MFA** on first login, **no** admin role.

---

## Offboarding (leaving the organization)

Goal: **separation**—they cannot sign in, but the org keeps mail, files, and continuity where policy allows. Do this in coordination with HR on the person’s **last day** (or immediately if termination is for cause).

| Area | Recommended actions |
| --- | --- |
| **Stop sign-in** | **Google:** **Suspend user** (preferred over delete while you transition mail/files). **Microsoft 365:** **Block sign-in** or disable the account. [Sign the user out of all sessions](https://support.google.com/a/answer/6328716) / revoke refresh tokens where your platform allows. |
| **Passwords & MFA** | After suspension, reset the password if policy requires it. Remove **app passwords**, **hardware keys** (reassign to IT inventory), and **OAuth / third-party app** access tied to their account. |
| **Mail continuity** | **Delegate** or **forward** to a manager (time-limited). Set an **out-of-office / vacation responder** with a generic contact if appropriate. **Google:** transfer **Drive** ownership of critical files; consider **email routing** or a **collaborative inbox** instead of leaving a full license on a departed user forever. **Microsoft:** consider converting to a **shared mailbox** (no sign-in) or grant manager access; see [shared mailbox guidance](../../microsoft/microsoft-365-user-guides/accessing-a-shared-mailbox-in-microsoft-outlook.md). Remove their **delegation** on other people’s mailboxes. |
| **Groups & collaboration** | Remove from **Google Groups**, **Teams**, **Shared drives**, **distribution lists**, **calendar resources**, and **chat spaces**. Audit **group owners** and **Drive file owners**—reassign owned items. |
| **Licenses & accounts** | **Unassign licenses** when the mailbox is archived or converted. Delete or archive the identity only when HR and legal are satisfied nothing must be retained. |
| **Devices** | Collect **org-owned** hardware. Remote-wipe org data from BYOD only if your policy allows. Remove the machine from **inventory / RMM**. |
| **Line-of-business apps** | Disable logins in CRM, fundraising, payroll, website admin, social accounts, and vendor portals. Rotate any **shared secrets** they knew (Wi‑Fi psk in a doc, shared API keys, etc.). |
| **Documentation** | Note what was done and **who owns** their former duties (ticket or internal checklist). |

**Examples (offboarding)**

* Departing ED: **Suspend** account same day; **delegate** email to board chair for 90 days; **transfer Drive** “Board” folder ownership; remove from **QuickBooks** and **banking** delegate list (non-IT but often forgotten).
* Intern ending term: **Suspend** account; **remove** from all groups; **no** mail forward unless supervisors request it; **unassign license** after 30-day read-only archive if your policy allows.
* Termination for cause: **immediate suspend** + **revoke sessions**; **no** auto-forward to personal email; HR drives timing on mailbox export.

### Google vs. Microsoft (quick reference)

| Task | Google Workspace | Microsoft 365 |
| --- | --- | --- |
| Pause access | Admin → Users → **Suspend user** | Users → **Block sign-in** |
| Hand off email | **Gmail delegation**, routing, or new owner for groups | **Shared mailbox**, **forwarding**, **full access** |
| Hand off files | **Transfer Drive ownership** | **OneDrive** transfer (admin workflow) + SharePoint membership |
| Free a license | Suspend, then delete or archive per policy | **Unassign license** ([guide](../../microsoft/microsoft-365-nonprofit-setup/managing-nonprofit-licenses-in-the-microsoft-365-admin-center.md)) |

**Vendor docs:** [Offboard a user (Google)](https://support.google.com/a/answer/33314) · [Remove a former employee (Microsoft)](https://learn.microsoft.com/en-us/microsoft-365/admin/add-users/remove-former-employee)

---

## Build your own runbook

1. Pick the rows above that match your size and risk (a 5-person agency vs. a clinic with PHI will differ).
2. Assign an **owner** (office manager, ED, or IT volunteer) and a **backup**.
3. Align with HR on **when** IT steps run (before exit interview, last hour of last day, etc.).
4. Review yearly—especially **group ownership**, **shared inboxes**, and **volunteer** accounts that outlive a single event.
