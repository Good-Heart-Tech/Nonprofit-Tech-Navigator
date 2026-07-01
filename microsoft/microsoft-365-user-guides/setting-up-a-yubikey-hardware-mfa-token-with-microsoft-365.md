---
icon: key
---

# Setting up a YubiKey (Hardware/MFA Token) with Microsoft 365

{% include "../../.gitbook/includes/multi-factor-authentication....md" %}

## :checkered\_flag:Prerequisites

Before you begin, ensure you have the following:

* A Microsoft 365 account with MFA enabled.
* A FIDO2-compliant security key (e.g., YubiKey, Feitian, or SoloKey).
* A compatible browser (Microsoft Edge, Google Chrome, or Firefox).

## :white\_check\_mark: Step-by-Step Guide

#### Step 1: Sign in to Your Microsoft 365 Security Settings

1. Open your browser and go to the Microsoft Security settings page: [https://mysignins.microsoft.com/security-info](https://mysignins.microsoft.com/security-info).
2. Sign in with your Microsoft 365 credentials.
3. If prompted, verify your identity using an existing MFA method (such as a mobile app or SMS code).

#### Step 2: Add a Security Key

1. Under the **Security info** section, click on _**+**_ _**Add sign-in method**._
2. From the drop-down list, select **Security key**, then click **Add**.
3. Choose your security key type:
   * **USB**: Insert your USB security key into your computer.
   * **NFC**: If using an NFC key, ensure your device supports NFC and hold the key near the NFC reader.
4. Click **Next** and follow the on-screen instructions.

#### Step 3: Register the Security Key

1. When prompted, insert your security key and tap it (if required).
2. Set up a PIN for your security key if you haven't already.
3. Follow the browser prompts to complete the security key registration.
4. Once successfully registered, give your security key a recognizable name (e.g., "_Work YubiK&#x65;_&#x79;").
5. Click **Done** to finalize the setup.

#### Step 4: Test Your Security Key

1. Sign out of your Microsoft 365 account.
2. Navigate to [https://login.microsoftonline.com](https://login.microsoftonline.com)&#x20;
3. Enter your username and choose **Sign in with a security key**.
4. Insert or scan your security key and enter your PIN if prompted.
5. If authentication is successful, you're now signed in using your security key!

### :construction\_worker: Managing Security Keys

To manage or remove your security key:

1. Go to [https://mysignins.microsoft.com/security-info](https://mysignins.microsoft.com/security-info).
2. Locate your registered security key under **Security info**.
3. Click **Remove** if you wish to delete it or add additional security keys, following the steps above.

### :wrench: Troubleshooting

* **Security key not detected?** Ensure your browser supports FIDO2 authentication and that your key is properly connected.
* **Error during setup?** Try using a different browser or clearing cache and cookies.
* **Lost or stolen security key?** Remove it from your security settings immediately and register a new one.

### Conclusion

Using a security key for MFA in Microsoft 365 enhances your account’s protection against phishing and unauthorized access. Once set up, signing in becomes faster and more secure. If your organization enforces MFA, consider using a security key as your primary authentication method for a seamless experience.

For additional security best practices, check out Microsoft’s official MFA documentation: [https://learn.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-methods](https://learn.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-methods).
