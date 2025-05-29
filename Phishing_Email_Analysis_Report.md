# Task2 
Analyze a Phishing Email Sample

*Objective*  To identify phishing characteristics in a suspicious email sample and generate a report detailing all observed phishing indicators.

*Tools Used*  # Email Client or Saved Email File (.eml / .txt)
              #Free Online Email Header Analyzer:
                https://mxtoolbox.com/EmailHeaders.aspx

 *Step-by-Step Analysis* 
 
  1. Obtaining the Sample Email
    A publicly available phishing sample was sourced from a threat-sharing platform for educational purposes. The email pretends to be from PayPal.

  2. Analyzing Sender's Address
     From: support@paypa1.com
     The domain is misleading — "paypa1.com" (with the number 1) instead of the legitimate "paypal.com". This is a clear spoofing attempt.
     
  3. Checking Email Headers (Using MXToolbox)
    Return Path: mailer@scamdomain.com
    Received From: An unknown mail server, not associated with PayPal.
    SPF: Fail
    DKIM: Missing
    DMARC: None
    These failed authentication mechanisms indicate the sender is spoofed and not verified by PayPal.

  4. Identifying Suspicious Links
   The body of the email includes a call-to-action:

   “Click here to verify your account”

  Actual link (hovered): http://verify-paypal-login.secure-mfa.io/paypal/login
  The domain is not related to PayPal and contains misleading terms like “secure” and “login” to appear legitimate.

 5. Urgent and Threatening Language
    The email uses psychological urgency to manipulate the recipient:

    “Failure to verify will result in suspension of your account.”
     This type of message is a common phishing tactic.
    
 6. Mismatched URLs
The hyperlink text shows “www.paypal.com” but redirects to a suspicious domain.

7. Spelling & Grammar Errors
Phrases like “We urgey you to act immdediately” reflect poor grammar and spelling — a typical indicator of phishing.

 EXAMPLE:-
 
 From: PayPal Support <support@paypa1.com>
 To: victim@example.com
 Subject: Action Required: Verify Your Account
 Date: Wed, 12 May 2025 09:47:00 -0400

 Dear User,

 We have detected unusual activity in your PayPal account. As a security precaution, your account access has been temporarily limited.

 To restore full access, please click the link below and verify your identity:

 http://verify-paypal-login.secure-mfa.io/paypal/login

 Failure to verify will result in permanent suspension of your PayPal account.

 Thank you,
 PayPal Security Team


