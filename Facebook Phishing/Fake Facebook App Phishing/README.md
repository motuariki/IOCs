These domains are phishing for users to grant thier custom facebook app access to thier Facebook Auth token.

Adveraries are using bunch of com domains eg. calendy.com-51235999318515976594[.]com.

User goes to the page, it directs them to login to calendly via Facebook. Click this link and it opens a legit login page for Facebook and asks them to connect the Calendly app to Facebook.

Sometimes there’s an error on this page for ‘JSSDK unknown host domain The domain you are hosting the Facebook Javascript SDK is not in your app’s Javascript SDK host domain list. Please specify your host domain in the App Dashboard login settings.’

This indicates that there is a mismatch between the calendly app on Facebook and the (fake) domain that is claiming to be authorised for accessing it. (only pre-approved domains can use their SDK for a specific app).
I suspect they have made an app on Facebook and are connecting it to that, but in some cases forgot to whitelist their domain. I have extracted appIDs however Facebook doesn’t return any info if those apps are set to private which is possibly whats going on there.
Eg. https://apps.facebook.com/application[.]php?id=256281040558

Likely goal:
Control OAuth redirect URIs, SDK behaviour, and permissions.
Receive the access tokens directly if the flow succeeds.
Avoids needing access to a real company’s Facebook App (like Calendly’s), which would be harder to exploit.