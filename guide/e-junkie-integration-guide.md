---
layout: guide
title: "Affiliate Tracking Software & Online Marketing System: LeadDyno"
nav: guide > e-junkie-integration-guide
---

## E-Junkie Integration Guide

### Introduction

This guide explains how to integrate E-Junkie purchases into LeadDyno. The integration
between E-Junkie and LeadDyno allows automated tracking of lead conversion, cancellation and affiliate compensation for
purchases made via Paypal purchases configured with E-Junkie.


### Configuring An E-Junkie Product

In order to track your affiliate sales, you must configure each E-Junkie product to pass PayPal purchase
information through to LeadDyno.

#### Step 1 - Set Up Your Product

First you need to configure your new product or edit your existing product through E-Junkie:

You will initially see a screen like this:

![Recurly Hosted Payment Pages Settings](/img/E-Junkie-Step-1.png)

When you configure your product options, you must check the **Send Transaction Data to a URL** checkbox.

When you are done configuring your product click **More Options** (if the product is new) or **Next** if you are editing
an existing product.

#### Step 2 - Integrate Your Product With LeadDyno

In the second step you will need to fill out the field labeled **Payment Variable Information URL**

![Recurly Hosted Payment Pages Settings](/img/E-Junkie-Step-2.png)

This should be set to

    https://collector.leaddyno.com/paypal_ipn?key=YOUR_PRIVATE_KEY

where **YOUR_PRIVATE_KEY** is replaced with your LeadDyno Private Key, available here:

[https://app.leaddyno.com/settings/account](https://app.leaddyno.com/settings/account)

When you are done, click the **Next** button, then the **Submit** button.

#### Step 3 - Include LeadDyno Tracking Info In Your Product Link

The final step is to pass LeadDyno's tracking information through to E-Junkie.

To do so, add the following code to the E-Junkie web link your users use to purchase your product:

**&custom=\{\{leaddyno.visit.id}}**

So the following E-Junkie link:

**https://www.e-junkie.com/ecom/gb.php?i=P1&c=cart&cl=123**

Would need to be modified to

**https://www.e-junkie.com/ecom/gb.php?i=P1&c=cart&cl=123&custom=\{\{leaddyno.visit.id}}**

With this change, your product offering will now be integrated with LeadDyno.

### Conclusion

LeadDyno is able to seamlessly integrate with E-Junkie for transactions that occur on your E-Junkie site. All
E-Junkie transactions are automatically sent to LeadDyno to track conversions, cancellations and affiliate compensation.
