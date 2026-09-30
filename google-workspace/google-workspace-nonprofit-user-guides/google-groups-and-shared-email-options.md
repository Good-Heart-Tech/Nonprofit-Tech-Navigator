---
icon: users
description: >-
  Choose the right Google Group or shared Gmail setup for team inboxes, lists,
  and public addresses like info@ or support@.
---

# Google Groups & Shared Email Options

Your nonprofit often needs addresses like **info@**, **support@**, or **board@** that more than one person can use. Google Workspace offers three main approaches. Pick the one that matches how your team actually works—not every option behaves like a normal inbox.

{% hint style="info" %}
**Who this guide is for:** Office managers and staff who need to understand the choices. Creating groups and shared inboxes usually requires a **Google Workspace administrator**. Staff can use collaborative inboxes and delegated Gmail once an admin sets them up.
{% endhint %}

## Choose the right option

| What you need | Best option | What it feels like for staff |
| --- | --- | --- |
| Everyone on the team should **get their own copy** of each message in their personal Gmail | **Email list group** | Mail to **group@yourorg.org** shows up in each member’s inbox |
| A **shared queue**—assign messages, mark done, work as a team | **Collaborative inbox** (a type of Google Group) | Staff work from the group’s shared list in [Google Groups](https://groups.google.com) |
| One **real Gmail mailbox** (info@) that several people open and send from | **Shared Gmail user** with **delegates** | Staff switch to **info@** inside Gmail and read/send as that address |
| Only **people inside your org** should email the address | Any option, with **Who can post** set to your org (not “Anyone on the web”) | Outside senders get blocked or moderated |
| **Anyone in the public** should email you (donors, clients, volunteers) | Group or shared user with **outside posting allowed** | See [Allow email from outside your organization](#allow-email-from-outside-your-organization) |

{% hint style="success" %}
**Simple rule:** Use an **email list** when everyone needs their own copy. Use a **collaborative inbox** when one team shares responsibility for answering. Use a **delegated Gmail account** when you want a single mailbox in Gmail with a shared Sent folder and contacts.
{% endhint %}

---

## Option 1: Email list group (distribution list)

An **email list** is the classic “mailing list.” When someone emails **newsletter@yourorg.org**, **each member receives the message in their own Gmail inbox**.

**Good for:**

* **board@** — every board member gets board mail in their personal inbox
* **staff@** or **all-staff@** — announcements to the whole team
* **committee@** — a small team that all needs to see every message

**Not ideal for:**

* A front desk or support queue where only one person should reply and others should see what’s already handled
* A single shared **Sent** folder everyone sends from

**How members experience it:** Messages appear like normal email in Gmail. Members can change how often they get mail (every message vs. a daily summary) in their [group membership settings](https://support.google.com/groups/answer/9666590).

Google’s overview: [What you get with Groups for Business](https://support.google.com/a/answer/10308022).

---

## Option 2: Collaborative inbox (Google Group)

A **collaborative inbox** is still a Google Group, but it is set up for **team workflow**, not for blasting copies to everyone’s personal inbox.

**Good for:**

* **support@**, **help@**, **intake@**, **volunteers@** — one team answers incoming mail
* Any address where you want to **assign** a message to someone and **mark it complete**

**How staff work:** Open the group in [Google Groups](https://groups.google.com). From the conversation list, team members can assign topics, mark conversations complete, and use labels. Google’s walkthrough: [Use a group as a Collaborative Inbox](https://support.google.com/a/users/answer/167430) and [Make a group a Collaborative Inbox](https://support.google.com/a/users/answer/10375787).

**Important:** Collaborative inbox features must be turned on for that group, and **conversation history** must be on. An owner or manager sets this in the group’s settings.

**Compared to an email list:** Members are **not** meant to get every message duplicated into personal inboxes. The “inbox” is the group.

---

## Option 3: Shared Gmail user with delegates

Here you create (or reuse) a **real Google account**, such as **info@yourorg.org**. You then add **delegates**—people allowed to open that mailbox inside Gmail, read mail, and send as **info@**.

**Good for:**

* A main **info@** or **contact@** address with a familiar Gmail experience
* When several people need to send from the **same address** and see the same inbox and contacts
* Larger teams (Google supports many delegates on one account; see limits in Google’s docs)

**How staff work:** In Gmail, click your profile picture and choose the **delegated** account (for example, **info@yourorg.org**). Google’s steps: [Delegate & collaborate on email](https://support.google.com/mail/answer/138350).

**Admin setup:** Turn on mail delegation in the Admin console, then create a [shared inbox](https://support.google.com/a/answer/16343077) or add delegates to an existing user. Admin guide: [Delegate a user’s email address](https://support.google.com/a/answer/11946994) and [Let users delegate access to a Gmail account](https://support.google.com/a/answer/7223765).

**License note:** A separate user account like **info@** uses a **Google Workspace user license**. A Google Group does **not** use an extra user license.

**Not the same as an alias:** You cannot add delegates to a simple **email alias** on someone’s account. The address needs to be its own user (or a group).

---

## Allow email from outside your organization

Many nonprofits need **donors, clients, or the public** to email **info@** or **support@**. That requires two layers of settings—**organization** and **group**.

### 1. Organization setting (admin)

An administrator must allow groups to accept mail from outside:

1. Sign in to [admin.google.com](https://admin.google.com).
2. Go to **Apps** → **Google Workspace** → **Groups for Business**.
3. Open **Sharing settings**.
4. Turn on **Group owners can allow incoming email from outside the organization**.
5. Save.

Google’s reference: [Set organization-wide policies for using groups](https://support.google.com/a/answer/167097).

### 2. Group setting (owner, manager, or admin)

For the specific group:

1. Open the group at [groups.google.com](https://groups.google.com).
2. **Group settings** → **Posting policies** (or **General**, depending on the UI).
3. Under **Who can post**, choose **Anyone on the web** if anyone should be able to email the group address.

If outside senders still cannot reach the group, see Google’s troubleshooting: [People outside my organization can’t email my group](https://support.google.com/a/answer/167085) (also covered in [Fix common issues with group settings](https://knowledge.workspace.google.com/admin/support/troubleshooting/fix-common-issues-with-group-settings)).

{% hint style="warning" %}
**Spam risk:** When **Anyone on the web** can post, turn on **moderation** for messages from non-members so junk mail does not flood the group. Google recommends moderating non-member posts when allowing public posting. Details: [Set who can view, post & moderate](https://support.google.com/groups/answer/2464975).
{% endhint %}

For a **shared Gmail user** (delegated account), outside senders simply email that address like any normal mailbox—no “who can post” group setting. You still protect it with your org’s [email protection settings](../google-workspace-nonprofit-setup/configure-email-protection-settings-in-google-workspace.md).

---

## Other settings worth knowing

These appear when creating or editing a group. Names in Google’s UI may vary slightly.

| Setting | Plain English | Typical nonprofit use |
| --- | --- | --- |
| **Who can post** | Who is allowed to send email **to** the group | **Anyone on the web** for public **info@**-style groups; **All organization users** or **Only members** for internal lists |
| **Who can view conversations** | Who can read messages in Google Groups | Often **All group members**; stricter for sensitive groups |
| **Who can join** | Open, invite-only, or request to join | **Invite only** for board@ and staff lists |
| **Allow external members** | Whether people **outside your org** can be added as members | Usually **off** unless you need a partner on a list |
| **Message moderation** | Hold messages for approval before delivery | Use when the address is public on your website |
| **Include in global address list** | Show the group in your org’s email directory | **On** for addresses staff should find when composing mail |
| **Conversation history** | Keep a searchable archive in the group | **On** (required for collaborative inbox) |

Permission reference: [Set who can view, post & moderate](https://support.google.com/groups/answer/2464975).

---

## Create a group (admin or allowed users)

Admins can create groups in the [Admin console](https://admin.google.com/ac/groups) under **Directory** → **Groups**, or users may create them at [groups.google.com](https://groups.google.com) if your org allows it.

When you create the group:

1. Pick the **group email address** (for example, **support@yourorg.org**).
2. Add **owners** (usually at least one admin) and **members** or **managers**.
3. Choose **email list** vs **collaborative inbox** (enable collaborative inbox in group settings if needed).
4. Set **Who can post** and moderation to match public vs internal use.

Admin FAQ: [Groups administrator FAQ](https://support.google.com/a/answer/167085).

---

## Google’s official guides (bookmark these)

* [Collaborate with colleagues (Gmail)](https://support.google.com/mail/answer/9259857) — compares delegation vs collaborative inbox
* [Make a group a Collaborative Inbox](https://support.google.com/a/users/answer/10375787)
* [Use a group as a Collaborative Inbox](https://support.google.com/a/users/answer/167430)
* [Delegate & collaborate on email](https://support.google.com/mail/answer/138350)
* [Create a shared inbox (admin)](https://support.google.com/a/answer/16343077)
* [Set organization-wide policies for groups (admin)](https://support.google.com/a/answer/167097)
* [What you get with Groups for Business](https://support.google.com/a/answer/10308022)

After groups are planned, continue nonprofit email setup in [Configure Google Workspace for Nonprofit](../google-workspace-nonprofit-setup/configure-google-workspace-for-nonprofit.md).

*Last reviewed: 2026-09.*
