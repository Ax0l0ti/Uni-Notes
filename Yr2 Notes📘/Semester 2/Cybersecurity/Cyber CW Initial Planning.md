### Cyber CW Initial Planning 

---

Results of Code - 
[[Kill me]]

Webnovel directed to - 
[Cloudary Holdings Limited](https://checkout.stripe.com/c/pay/cs_live_a1TQSQf7AvN7hiobgasm5U93WIT5ZHW6sKJJXTL59UEdKXCZy95awLDWfg#fidkdWxOYHwnPyd1blppbHNgWlJuPDFMMzBfV2Bgb2xVYWpDY1B3S0x8UzU1dn9ANn8zc1UnKSdobGF2Jz9%2BJ2hwbGEnPydLRCcpJ3ZsYSc%2FJ0tEJyknYnBsYSc%2FJ0tEJ3gpJ2dgcWR2Jz9eWCknaWR8anBxUXx1YCc%2FJ3Zsa2JpYFpscWBoJyknd2BjYHd3YHdKd2xibGsnPydtcXF1dj8qKnVkfCtyYGdranNgaStmamgneCUl)


![[HAR_screenshot.png]]


> [!tldr]+ Images of tTansaction 
> ![[Pasted image 20250310143801.png|200]] Purchasing coins immediately redirected through to Stripe checkout for Cloudary Holdings Limited which after research is a Hong Kong private company involved in shares 
> ![[Pasted image 20250310143436.png|400]]
> 




---


## Analysis of HAR

Immediately upon hitting purchase, first activity was re-direction to stripe checkout page for Cloudary Holdings Limited

The second HAR file contains **181 HTTP requests**. I’ll now analyse:

Let’s start by extracting the domains and request metadata. ​​

### **Most Frequently Accessed Domains (HAR2):**

1. **Stripe-related:**
    
    - `js.stripe.com` (53 requests)
        
    - `r.stripe.com` (39 requests)
        
    - `b.stripecdn.com` (20 requests)
        
    - `api.stripe.com` (7 requests)
        
    - `m.stripe.com` (4 requests)
        
2. **hCaptcha:**
    
    - `api.hcaptcha.com` (13 requests)
        
    - `newassets.hcaptcha.com` (12 requests)
        
3. **Google-related:**
    
    - `play.google.com` (10 requests)
        
    - `www.gstatic.com` (8 requests)
        
    - `pay.google.com` (5 requests)

---

​

Detailed Sensitive Requests (HAR2)

| URL                                                                                                             | Method | Status |
| --------------------------------------------------------------------------------------------------------------- | ------ | ------ |
| https://js.stripe.com/v3/fingerprinted/js/shared-b3fa357b5466571fdd145011ca89702c.js                            | GET    | 200    |
| https://js.stripe.com/v3/fingerprinted/js/elements-inner-express-checkout-0705f382c3bd353ab319c39aa1eddc29.js   | GET    | 200    |
| https://js.stripe.com/v3/fingerprinted/css/elements-inner-express-checkout-a898a29787883a4bb38206a38b604243.css | GET    | 200    |
|                                                                                                                 |        |        |

Security Risk Assessment (HAR2)

|URL|Exposed Data|Security Risks|
|---|---|---|
|https://r.stripe.com/b|746|⚠️ CVV or Card Number should only be used in a single secure transaction.|
|https://api.stripe.com/v1/payment_methods|4928261366639168|⚠️ CVV or Card Number should only be used in a single secure transaction.|
|https://api.stripe.com/v1/payment_methods|746|⚠️ CVV or Card Number should only be used in a single secure transaction.|

#### **Sensitive Request Details:**

From the second HAR file, your personal and card information was transferred to the following URLs:

1. **`https://r.stripe.com/b`**
    
    - Exposed Data: **CVV (746)**
        
2. **`https://api.stripe.com/v1/payment_methods`**
    
    - Exposed Data:
        
        - **Full card number** (4928261366639168)
            
        - **CVV** (746)
 

These endpoints belong to **Stripe**, which is a known and secure payment processor. However, the presence of full card details and CVV across multiple requests is something to watch closely.


49348
54093
54101
54105
Name & email on 54264 
Name & email on 55895 

Name, email and account ID on 57916


balance in value field for 1392, 1667, 4182

many minified and obfuscated JavaScript module loader or bundler. Let's break down the main components: