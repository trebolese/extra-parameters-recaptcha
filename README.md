# extra-parameters-recaptcha
Identify pageAction, reCaptcha Enterprise, anchor, reload, the type of the reCaptcha, data-s parameter and more!


![](https://assets.capsolver.com/prod/images/post/2024-06-04/9c9c82ff-64e5-4ca9-b7e7-664ef1d994f0.jpeg)

# Understanding Additional Parameters
**reCaptcha v2:**
- **reCaptcha versions**: These can vary and include:
  - **reCaptcha v2 Normal**: The standard version where users solve a puzzle to verify they're not a bot.
  - **reCaptcha v2 Enterprise**: An advanced, paid version with more features and customization options, designed for businesses requiring higher security.
  - **reCaptcha v2 Invisible**: A version that operates in the background, typically requiring no user interaction. It uses a risk analysis engine to differentiate between users and bots.

- **pageAction**: This is a parameter found in some site anchor endpoints. It represents the 'action' value and is used in reCaptcha v3 for risk analysis.

- **enterprise payload**: This refers to the 's-data' in reCaptcha, which is a set of data sent to reCaptcha Enterprise for analysis. The exact contents depend on the specific requirements of reCaptcha Enterprise.

- **Anchor**: This is additional data obtained from the Capsolver extension. In the context of reCaptcha, it could refer to the part of the page where the reCaptcha widget is anchored.

- **Reload**: This is also additional data obtained from the Capsolver extension. It could refer to the action of reloading the reCaptcha widget, for instance, if the user wants a new challenge.

- **ApiDomain**: This is the domain address from which to load reCAPTCHA Enterprise. Examples include 'http://www.google.com/' and 'http://www.recaptcha.net/'. This parameter should only be used if its purpose is understood.
Don't use a parameter if you don't know why it's needed.
   ![](https://assets.capsolver.com/prod/images/post/2024-06-04/9309601c-3b34-4db3-a594-7ca073928a38.png)

These parameters are not always present and their presence depends on the site key.

# Identifying Additional Parameters
The Capsolver extension can detect if a site key requires these additional parameters.

### Steps to Detect reCAPTCHA Parameters:

1. **Installation**:

   - For Chrome users, install the [Captcha Solver Auto Solve](https://chrome.google.com/webstore/detail/captcha-solver-auto-bypas/pgojnojmmhpofjgdmaebadhbocahppod) extension.
   - For Firefox users, install the [Captcha Solver Auto Solve](https://addons.mozilla.org/en-US/firefox/addon/capsolver-captcha-solver/) extension.

2. **Capsolver Setup**:

   - Go to [CapSolver](https://www.capsolver.com/).
   - Press "F12" on your keyboard to open the developer tools.
   - Go to the **Capsolver Captcha Detector** tab.
     ![](https://assets.capsolver.com/prod/images/post/2023-10-31/2115f05d-a7eb-40b6-9693-53baa45d39a9.png)

3. **Detection**:
   - Keep the Capsolver panel open and visit the website where you want to trigger the CAPTCHA.
   - Trigger the captcha.
   - Note: **Do not close** the Capsolver panel before triggering the CAPTCHA.

### CAPTCHA Parameter Detection:

#### Parameters for reCAPTCHA that can be identified:

- Website URL
- Site Key
- isInvisible
- pageAction
- isEnterprise
- isSRequired
- isReCaptchaV3
- Api Domain
- Anchor
- Reload

After the CAPTCHA parameters have been detected, CapSolver will provide a JSON detailing how to submit the captcha parameters to their service.

The extension panel will display the information like this:
![](https://assets.capsolver.com/prod/images/post/2024-06-04/22c56797-bbde-4ba5-9a2a-115fb4715449.png)
