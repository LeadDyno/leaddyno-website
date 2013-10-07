---
layout: guide
title: "Affiliate Tracking Software & Online Marketing System: LeadDyno"
nav: guide > paypal-merchant-integration-guide
---

## Paypal Merchant Account Integration Guide

### Introduction

This guide explains how to integrate the PayPal merchant service with LeadDyno. The integration
between PayPal and LeadDyno allows automated tracking of lead conversion, cancellation and affiliate compensation for purchases
made when PayPal acts as your merchant service.

<p class="alert alert-info">
  <strong>Note:</strong> If you are using PayPal "Buy Now" buttons on your site, there is a simpler integration mechanism
  available.  Please <a href="/guide/paypal-integration-guide.html">Click Here</a> for instructions.
</p>

#### Configuring the Paypal IPN callback

To integrate Paypal's Merchant Account functionality with LeadDyno, you must set up a global
[IPN](https://cms.paypal.com/uk/cgi-bin/?cmd=_render-content&content_ID=developer/e_howto_admin_IPNIntro) callback
to LeadDyno.  This involves three steps, outlined below:

![/img/paypal-merchant-config.png](/img/paypal-merchant-config.png)

##### Step 1

Select the **Profile** section of your PayPal account

##### Step 2

Select the **My Selling Tools** sub-section of your PayPal profile

##### Step 3

Click The **Update** link to the right of the the **Integrate PayPal payment notifications with my website** text.

and then click **Choose IPN Settings**:

![/img/paypal-choose-ipn.png](/img/paypal-choose-ipn.png)

You will be taken to your IPN settings page

![/img/paypal-update-ipn.png](/img/paypal-update-ipn.png)

Set the **Notification URL** to:

`https://collector.leaddyno.com/paypal_ipn?key=YOUR_PUBLIC_KEY`

where **YOUR_PUBLIC_KEY** is your LeadDyno Public API Key from your
[LeadDyno settings page](https://app.leaddyno.com/settings/account).

Ensure that **Receive IPN messages (Enabled)** is selected, and then click **Save**

### Conclusion

Paypal notifications will now be sent to LeadDyno when purchases and cancellations occur.  After ensuring that LeadDyno's
lead tracking Javascript is properly installed on your site, you are done with the integration.