---
icon: sign-posts-wrench
---

# How to Uninstall Good Heart Tech's Support Tools

Sometimes, a **personal computer** (not owned by your organization) gets added to Good Heart Tech’s management by mistake. When that happens, uninstalling our support tools removes our ability to access and monitor that device.

### Before you start (important)

{% hint style="warning" %}
You must be signed in with a **Windows administrator account** to uninstall apps.
{% endhint %}

{% hint style="danger" %}
If this PC is still managed by your organization (often through **Microsoft Entra ID**), the tools may reinstall. If you’re not sure, check with your organization’s IT contact first.
{% endhint %}

### Uninstall the support tools (Windows)

{% stepper %}
{% step %}
### Open the installed programs list

1. Open the **Start** menu.
2. Type `appwiz.cpl`.
3. Press **Enter**.

This opens **Programs and Features** (the classic Windows uninstall list).
{% endstep %}

{% step %}
### Uninstall all Good Heart Tech support tools

In the program list, uninstall **each** of the following if you see it:

* **Level**
* **Liongard Agent**
* **Senteon Agent**
* **Tier2Tickets**

Uninstalling **Level** is especially important. If it stays installed, it can reinstall the other tools over time.

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

### Restart and confirm

1. Restart the computer.
2. Re-open `appwiz.cpl`.
3. Confirm that the items above are no longer listed.
{% endstep %}
{% endstepper %}

### If the tools come back after uninstalling

That usually means the device is still under an organization's management.

Try this quick check:

1. Open **Settings**.
2. Go to **Accounts** → **Access work or school**.
3. If you see a work/school account connected, you may need to select it and choose **Disconnect**.

{% hint style="warning" %}
Disconnecting a work/school account can remove access to organizational apps, email, and files on this PC. If this is a work device, stop and talk to your organization’s IT team first.
{% endhint %}

### Need help?

If you’re not sure whether you should remove these tools, or if uninstall fails, contact Good Heart Tech support. Tell us whether the device is **personal** or **organization-owned**, and whether it’s connected to a **work/school account** in Windows.

{% content-ref url="how-to-submit-a-support-ticket-to-good-heart-tech.md" %}
[how-to-submit-a-support-ticket-to-good-heart-tech.md](how-to-submit-a-support-ticket-to-good-heart-tech.md)
{% endcontent-ref %}
