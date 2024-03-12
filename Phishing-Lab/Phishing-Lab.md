# Phishing Lab

I am going to analyze a phishing email that I found on GitHub and determine if the email is malicious or not.

![PhishingEmail](Screenshots/PhishingEmail.png)

Rendered image of email.

## Phishing Email Report

The email styling looks well put together and appears to be an email from Lowe's at first glance. The email is trying to get a user to click on a link, if clicked it would send them to an X post. I don’t have access to the X post that has been deleted. The X post probably had another link to a malicious site.  

## Email Artifacts

    Date and Time: Mon, 13 Nov 2023 10:47:11 +0000
    Sending Address: l7o03@fvreazgkx4[.]com
    Subject: Win a Club Car Golf Cart - Enter Now 
    Recipient address: “Redacted”
    Sending IP address: 89.144.10.70
    Reverse DNS: AS197549 DE-TopColo GHOSTnet GmbH, DE (registered Jan 28, 2011)

## Web Artifacts

    hxxps://t[.]co/ZXcw3ridSn

## Defensive Measures

I would block the sending email address, subject, web artifact, and domain of the email address. This email is malicious and needs to be deleted from any inbox that has received this email to limit the damage it could cause.
