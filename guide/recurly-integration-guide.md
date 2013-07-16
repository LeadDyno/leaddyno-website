---
layout: guide
title: "Affiliate Tracking Software & Online Marketing System: LeadDyno"
nav: guide > recurly-integration-guide
---

## Recurly Integration Guide

### Introduction

This guide explains how to integrate Recurly purchases and subscription into LeadDyno. The integration
between Recurly and LeadDyno allows automated tracking of lead conversion, cancellation and affiliate compensation for purchases
made via [Recurly Hosted Payment](http://docs.recurly.com/hosted-payment-pages) pages.


### Recurly Hosted Payment Page Settings

The first step to enable the integration is to make sure Recurly Hosted Payment Pages are enabled. Login to your recurly
account, select **Hosted Payment Pages** from the left menu, and make sure **Enable Hosted Payment Pages** is checked.
Review the other settings and adjust is necessary.

See the following image for reference:


![Recurly Hosted Payment Pages Settings](/img/recurly_guide_hosted_payment_settings.png)


#### Recurly Plan Settings

To obtain the Hosted Payment Page URL within Recurly, click on **Subscription Plans** in the left menu and then click
on the plan you wish to use. The **Plan Code** must match the Commission Plan configured in the Commissions section of
the [LeadDyno Dashboard](https://app.leaddyno.com/plans).

On this page you will see the **Hosted Page URL**. This is the URL your website will link to when customers are ready
to make a purchase.

See the following image for reference:

![Recurly Plan Settings](/img/recurly_guide_plan_info.png)


#### Recurly Push Notifications

In order for LeadDyno to receive events about purchases made by your customers, you must configure a Recurly Push Notification
to be sent to LeadDyno. This is done in Recurly by selecting **Push Notifications** in the left menu (located near the bottom-left
in the **Developer** section).

You will be presented with the following screen:

![Recurly Push Notifications](/img/recurly_guide_push_notifications.png)

Click on the **Configure** button, and then in the Push Notification URL text field, put in the following:

<pre>
 https://collector.leaddyno.com/recurly_push_notification?key=YOUR_PRIVATE_KEY
</pre>

Replace **YOUR_PRIVATE_KEY** with your private API key found on the [LeadDyno Dashboard](https://app.leaddyno.com/settings/account).

Leave **HTTP Auth Username** and **HTTP Auth Password** fields blank.

You should see something like the following:

![Recurly Push Notifications Settings](/img/recurly_guide_push_settings.png)

Click **Update Configuration** and you are done configuring Recurly.


### Enable Recurly Integration with LeadDyno

This section assumes the regular LeadDyno visitor tracking is already installed on your website. If not, see our
[Installation Guide](/guide/installation.html) for details, and return here after it is installed.

The integration with Recurly is very simple. All that needs to be done is to add a special parameter to any link to
the Recurly hosted payment page at the end of the URL.

Before the modification, the link to the Recurly Hosted Payment page might look like this on your page:

{% highlight html %}
<a href="https://example.recurly.com/subscribe/myplan">Subscribe!</a>
{% endhighlight %}

To enable the integration add **/\{\{leaddyno.visit.id\}\}** at the end of the link URL. For example, the above would become:

{% highlight html %}
<a href="https://example.recurly.com/subscribe/myplan/{{ "{{leaddyno.visit.id"}}}}">Subscribe!</a>
{% endhighlight %}

The variable **\{\{leaddyno.visit.id\}\}** will be replaced by the LeadDyno visitor ID and when the Recurly Push Notificaiton
is sent to LeadDyno (configured in the previous section), we will match up the visitor with the purchase and perform
the appropriate action.


### Conclusion

LeadDyno is able to seamlessly integrate with Recurly for transactions that occur on your Hosted Payment Pages. All
Recurly transactions are automatically sent to LeadDyno to track conversions, cancellations and affiliate compensation.
