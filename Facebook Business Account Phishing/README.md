## Facebook Business Account Phishing ##

This is a collection of IOCs and TTPs associated with Facebook Business Account phishing. These are primarily originating from Vietnamese online crime gangs who use the stolen Facebook business accounts to advertise websites that spread malware or engage in dropshipping.

These are small samples of a very large cluster of phishing landing pages targeting Facebook and Calendly users. The motivation is to obtain all credentials and data required to take over Business Facebook accounts. The victim is prompted with a Captcha, and once this is completed they are prompted to enter Facebook login credentials and/or personal details necessary for full account takeover. The themes of the landing pages suggest social engineering is used on victims with hooks about facebook account recovery, rule infringments, and scheduled meetings with Calendly to get them to visit them.

Some landing pages after the captcha are themed to look like Facebook business account recovery steps, others are made to look like a Calendly scheduled call that can only be accessed by logging into Facebook. Some of these landing pages even prompt the user for 2FA codes. The adversary makes use of a mix of typosquat domains and legitimate hosting such as Vercel and ApplifyApp. These along with the Captcha are a low effort attempt to avoid automated detection for at least a few days. There are thousands of these domains generated daily, I offer a small sample to showcase a snapshot in time and the TTPs in play.

## Calendly Example ##

Initial page with Captcha:

<img width="614" alt="image" src="https://github.com/user-attachments/assets/86b6ea86-c6c3-4467-b10a-ded2a1e9bdd9" />

Calendly landing page:

<img width="1341" alt="image" src="https://github.com/user-attachments/assets/f91f5514-9d48-4ee9-af41-5c9adcbc1875" />

Calendly Landing page with fake browswer popup to harvest facebook credentials:

![image](https://github.com/user-attachments/assets/fef9c52d-a4cd-4835-a91e-cc4324546f17)




