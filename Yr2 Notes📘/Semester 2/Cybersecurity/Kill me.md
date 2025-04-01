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




Qs
1) 50% - Sites communicate w in the transaction? List of each site and its apparent purpose. The list should be numbered. b. 21..50 sites. 

2) 20% - To which site, or sites, does the complete PAN get communicated. State the line(s) in the HAR that evidence this. How is the PAN protected in transit? Was it obvious, from the transaction as you observed it as a purchaser (i.e. not using the logs) that your data would go there? 

3) 20% - How dependent is the correct functioning of the process you saw on the correct functioning of the DNS? In particular, could a subverted DNS result in any of a. Leakage of the PAN (with or without the CVV)? b. Failure of the transaction (no money taken and no goods delivered/service rendered)? c. Subversion of the transaction (money is taken, but the goods/services are delivered elsewhere)? d. Other malfunction? 
   
4) 10% - Looking at the HTML etc. you have saved, do you feel confident you know what it is doing with your data? In particular, what did you learn from the logs/HTML that you could not have reasonably deduced as a purchaser with no access to these?