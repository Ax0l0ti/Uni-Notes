# Kill me
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  01-04-2025
> > *Module :* [[Cybersecurity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]
> [[#]]
> [[#]]
> [[#]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  
> $b)$ - 
> $c)$ - 

---

#TODO 

=== Personal Details Occurrences ===  

BRAND: Found in lines 87, 111, 3001, 3031, 3034, 3157, 3714, 3744, 4121, 4145, 4201, 4635, 4659, 11332, 11803, 12093] 

CVV/CVC: Found in lines 87, 111, 191, 1170, 3001, 3031, 3034, 3133, 3157, 3714, 3769, 3793, 3841, 4097, 4121, 4145, 4234, 4332, 4368, 4380, 4437, 4635, 4659, 8142, 8181, 8257, 8296, 10739, 10760, 14658, 14697, 14736, 14775, 15313, 15334, 16177, 16506, 16851

COUNTRY: Found in lines 3034 

PIN: Found in lines 3157, 4097, 8008, 8142, 8181, 8257, 8296, 10739, 10760, 14554, 14658, 14697, 14736, 14775, 15313, 15334

EMAIL: Found in lines 16085, 16506

NUMBER: Found in lines 16506

NAME: Found in lines 16506, 16546, 16722, 17214
  
=== Grouped Website Occurrences by Domain ===  
A total of 23 unique base domains were contacted/referenced  
378 | stripe.com  
└─ 140 js.stripe.com  
└─ 133 checkout.stripe.com  
└─ 41 r.stripe.com  
└─ 28 q.stripe.com  
└─ 14 api.stripe.com  
└─ 7 stripe.com  
└─ 4 m.stripe.com  
└─ 3 pm-hooks.stripe.com  
└─ 3 merchant-ui-api.stripe.com  
└─ 2 errors.stripe.com  
└─ 1 checkout-cookies.stripe.com  
└─ 1 payments.stripe.com  
└─ 1 dashboard.stripe.com  
92 | hcaptcha.com  
└─ 55 newassets.hcaptcha.com  
└─ 16 hcaptcha.com  
└─ 13 api.hcaptcha.com  
└─ 8 sentry.hcaptcha.com  
85 | google.com  
└─ 49 pay.google.com  
└─ 16 play.google.com  
└─ 7 apis.google.com  
└─ 4 google.com  
└─ 3 pay.sandbox.google.com  
└─ 2 uberproxy-pen-redirect.corp.google.com  
└─ 1 ibfe-canary.corp.google.com  
└─ 1 www.google.com  
└─ 1 admob.google.com  
└─ 1 accounts.google.com  
61 | stripecdn.com  
20 | gstatic.com  
17 | withgoogle.com  
17 | stripe.network  
15 | w3.org  
11 | webnovel.com  
└─ 9 pay.webnovel.com  
└─ 2 www.webnovel.com  
11 | github.com  
10 | bit.ly  
7 | apache.org  
6 | affirm.ca  
3 | reactjs.org  
3 | cloud.google  
2 | link.com  
└─ 1 link.com  
└─ 1 checkout.link.com  
2 | cdn-apple.com  
2 | angular.dev  
1 | git.io  
1 | link.co  
1 | ibfe-canary.corp  
1 | broofa.com  
1 | example.com




---

Abstract 
Transaction
Overview
In depth 
DNS related
what no user could deduce
- Tested as a robot 
	- Probably to stop DOS from purchase requests
	- Or hinder automated piracy of unreleased chapters



└─
Qs
1) 50% - Sites communicate w in the transaction? List of each site and its apparent purpose. The list should be numbered. b. 21..50 sites. 

2) 20% - To which site, or sites, does the complete PAN get communicated. State the line(s) in the HAR that evidence this. How is the PAN protected in transit? Was it obvious, from the transaction as you observed it as a purchaser (i.e. not using the logs) that your data would go there? 

3) 20% - How dependent is the correct functioning of the process you saw on the correct functioning of the DNS? In particular, could a subverted DNS result in any of a. Leakage of the PAN (with or without the CVV)? b. Failure of the transaction (no money taken and no goods delivered/service rendered)? c. Subversion of the transaction (money is taken, but the goods/services are delivered elsewhere)? d. Other malfunction? 
   
4) 10% - Looking at the HTML etc. you have saved, do you feel confident you know what it is doing with your data? In particular, what did you learn from the logs/HTML that you could not have reasonably deduced as a purchaser with no access to these?




Overview
This report presents an analysis of a HAR file recorded during an
online transaction. It addresses the communication endpoints, personal data exposure
(especially the Primary Account Number, PAN), DNS dependencies, and the visibility of
data handling from the HTML/JS content.

**##NEWW** 
Transaction
The transaction recorded was a purchase of in-app currency for webnovel.com which was handled by stripe.com. 

1 Communication with Websites (50%)
Based on the captured HAR, the browser communicated with more than 50 unique sites.
These are grouped below by top-level domain.
Grouped Website Occurrences
A total of 23 unique base domains were contacted. Below is a summary:
Domain Subdomains and Counts
stripe.com js (140), checkout (133), r (41), q (28), api (14), m (4), others (18)
hcaptcha.com newassets (55), api (13), sentry (8), hcaptcha (16)
google.com pay (49), play (16), apis (7), sandbox (3), others (10)
stripecdn.com 61 requests total
gstatic.com 20
withgoogle.com 17
stripe.network 17
w3.org 15
webnovel.com pay (9), www (2)
github.com 11
bit.ly 10
apache.org 7
affirm.ca 6
reactjs.org 3
cloud.google 3
link.com link (1), checkout.link (1)
cdn-apple.com 2
angular.dev 2
git.io 1
link.co 1
1

webnovel is the website of purchase, it is only referenced 
Stripe is the handler of transaction activity


Concerning or Unclear Domains
• bit.ly - URL shortener, purpose unclear.
• b.stripecdn.com - Serves third-party scripts, could embed trackers.
• q.stripe.com - Analytics; not visible to user.
• pay.webnovel.com - If not familiar with the merchant, could be misleading.
2 Transmission of PAN (20%)
The full PAN (4928261366639168) was detected in:
• URL: https://api.stripe.com/v1/payment_methods
• HAR Line: 47953
• Protection: HTTPS (TLS encryption)
• Visibility to Purchaser: Not obvious unless inspecting network traffic
Listing 1: Excerpt from HAR Line 47953
" postData ": {
" text ": " card [ number ]=4928261366639168& card [ exp_month ]=4& card
[ exp_year ]=2027& card [ cvc ]=746"
}
3 DNS Dependency and Risks (20%)
The transaction is highly DNS-dependent. A subverted DNS could result in:
• (a) Leakage of PAN: Yes, if API domain is spoofed.
• (b) Transaction failure: Yes, due to dependencies on Stripe, Google, and hCaptcha.
• (c) Transaction subversion: Possible if DNS directs to fake merchant/payment
processor.
• (d) Other malfunctions: CAPTCHA or third-party scripts may fail to load.
4 HTML/JavaScript Observations (10%)
• Background requests to r.stripe.com, q.stripe.com, pay.google.com were not
disclosed on the UI.
• Stripe elements auto-collect user card data and send directly to Stripe.
• Full visibility of the request payload only possible through HAR inspection.
2
Purchaser View vs Developer Insight
As a regular purchaser:
• You would not know about any backend analytics or third-party data sharing.
**##NEWW** • No notice of CAPTCHA activity is given, user is analysed incase 
• The transmission endpoint (Stripe) is hidden behind frontend scripts.
• HTML and JS logs reveal far more than the visible UI suggests.
Appendix A: Personal Data Occurrences
BRAND : Lines [87 , 111 , 3001 , 3031 , ...]
CVV / CVC : Lines [87 , 111 , 191 , 1170 , ...]
COUNTRY : Lines [3034]
PIN : Lines [3157 , 4097 , 8008 , ...]
EMAIL : Lines [16085 , 16506]
NUMBER : Lines [16506]
NAME : Lines [16506 , 16546 , 16722 , 17214]
3


10.72.46.25:1643