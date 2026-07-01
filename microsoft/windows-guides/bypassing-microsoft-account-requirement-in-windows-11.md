# Bypassing Microsoft Account Requirement in Windows 11

### When to Use This

Use this procedure if:

* The device is at the “_Let’s add your Microsoft account_” screen
* There is no option to create or use a local account
* The device was previously configured with a local login, but can no longer sign in after updates
* A Windows feature update completed, and now the user is blocked at account setup
* The device is not intended to be signed into Microsoft Entra ID

Do **not** use this if the device is intentionally joined to Microsoft 365 or managed via Entra.

### Steps to Bypass Microsoft Account Requirement

#### 1. Open Command Prompt During Setup

While on the Microsoft account sign-in screen, press:

```
Shift + F10
```

This opens a Command Prompt window. If prompted for elevated access, approve the administrator request.

#### 2. Run the Bypass Command

In the Command Prompt window, type:

```
oobe\bypassNRO
```

Press **Enter**.

#### 3. Allow the Device to Reboot

The system will automatically reboot. Do not interrupt this process.

### Access Your Local Windows Account

After the device reboots, you will now see one of the following paths.&#x20;

* If you previously had an account on this device, the local account will appear, and the device should return to the desktop exactly as it was before the update.
* If this is a new PC:
  * Select **I don’t have internet**
  * Choose **Continue with limited setup**
  * Set a secure password and security information.
