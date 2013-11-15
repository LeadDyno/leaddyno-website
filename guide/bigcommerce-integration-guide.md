---
layout: guide
title: "Bigcommerce Integration Guide with LeadDyno, The Affiliate Tracking Software & Online Marketing System"
nav: guide > bigcommerce-integration-guide
---

## Bigcommerce Integration Guide

### Introduction

LeadDyno offers a One-click integration with Bigcommerce, making it incredibly easy to get an affiliate program going for
your Bigcommerce store. After completing this guide, your LeadDyno account will be setup so that you will have complete
visibility into your store's visitors, leads and purchases, including crediting affiliates for traffic in which they
send to your store.

The Bigcommerce integration also synchronizes custom **Affiliate Codes** you assign to affiliates as Bigcommerce coupons.
This allows affiliates to pass around their affiliate code via offline means and still get credit for those sales. You
have full control over the coupon settings such as the dollar or percent discount and minimum purchase required. You
also have full control to make changes to individual affiliate coupons via the Bigcommerce control panel.

This guide consists of several parts:

* Instructions on how to add the LeadDyn tracking code to your Bigcommerce store
* Configuring your Bigcommerce store so that LeadDyno can integrate with it
* Configuring your LeadDyno account to connect to your Bigcommerce store

## Enable LeadDyno tracking in your Bigcommerce store ##

The LeadDyno tracking integration makes use of the built in 'Google Analytics' tracking setting of Bigcommerce. To
enable it, select the **Analytics** menu option from within the **Apps** menu.

![Bigcommerce Analytics Setting](/img/bc_guide_analytics.png)


Next, check the **Google Analytics** option in the Providers box, and click Save.

![Bigcommerce Providers](/img/bc_guide_analytics_enable_google.png)

A new tab will appear called **Google Analytics**. Click this tab.

![Bigcommerce Google Analytics](/img/bc_guide_analytics_click_google.png)

Paste the following LeadDyno tracking javascript into the **Tracking Code** field:

{% highlight html %}
<script type="text/javascript" src="https://static.leaddyno.com/js"></script>
<script>
  LeadDyno.key = "YOUR_PUBLIC_KEY";
  LeadDyno.recordVisit();
  LeadDyno.autoWatch();
 </script>
{% endhighlight %}

Replace the word **YOUR_PUBLIC_KEY** with your **public** API key found on the [LeadDyno Dashboard](https://app.leaddyno.com/settings/account).

![Bigcommerce Tracking Code](/img/bc_guide_analytics_paste_and_save.png)

After clicking Save, your Bigcommerce store will now have the tracking code on every page.


## Configure Bigcommerce API User ##

LeadDyno requires you to create a user within the Bigcommerce system that has API access and provide the API details
to LeadDyno. This way LeadDyno can periodically watch for new sales in your Bigcommerce store and record those as
purchases in LeadDyno, crediting the affiliate with the sale, if applicable.

To create a new user in your Bigcommerce store, select the **Users** option in the top right navigation menu and click
**Create a User Account**.

![Bigcommerce Users](/img/bc_guide_create_user.png)


Fill in a Username, password and email address for the new user. We suggest using the username **apiuser**. The password
and email can be anything, LeadDyno will not need these settings, just the username. Make sure the **User Role** for the new
user is a **Store Administrator** so that the new user will have access to orders and coupons, which LeadDyno needs.

![Bigcommerce User Settings](/img/bc_guide_create_user_settings.png)

The important part is to turn on API access by checking the box next to **Enable the API** option.

![Bigcommerce User API Settings](/img/bc_guide_enable_api.png)

Take note of the **API Path** and **API Token** settings that will appear. These will need to be copied into your LeadDyno
settings, which is detailed in the next section. Make sure to click Save to save this new user.



## Configure LeadDyno to Bigcommerce Integration ##

From within your [LeadDyno Dashboard](https://app.leaddyno.com), select the **Settings** menu from the left-hand naviation
and click **Manage Integrations**, and then choose **E-Commerce Services** at the top.

![LeadDyno E-Commerce Settings](/img/bc_guide_ld_settings.png)


Copy the values from your Bigcommerce store into the Bigcommerce settings. The **Store URL** is the **API Path** value
from the last section. The **API User** is the user you created in the last section, and finally the **API Key** is the
**API Token** from the Bigcommerce user page.

Click on the **Test Connection** button and you should get a message indicating if LeadDyno is able to successfully connect
to your Bigcommerce shop. If it does not say the connection is successful, double check the settings match the ones from
your Bigcommerce user you created previously.

After the test connects successfully, click the blue Save Bigcommerce Connection Settings button, and then a new button called
Manage Bigcommerce Discount Program will appear. This is where you configure the default settings for new coupons that
LeadDyno creates for each affiliate.

![Bigcommerce Discount Settings](/img/bc_guide_ld_coupon_settings.png)

On this page you can choose if the coupon should be a percentage or fixed amount, and if a minimum purchase is required
for the coupon to work. These are just the default settings for coupons that are created when you assign a discount/affiliate
code to an affiliate. You can always change individual coupon settings from within the Bigcommerce manage coupon tool
to change many more settings about the coupon.

From this screen you can also manually run a synchronization between LeadDyno and Bigcommerce. This happens several times
a day automatically, but if you have a recent Bigcommerce sale that you need to show up immediately in LeadDyno as a
purchase, you can manually start the job on this page.

<div class="alert alert-info">
  <strong>Note:</strong> LeadDyno only considers paid, completed and shipped orders as purchases, so they will not show up
   as purchases in LeadDyno until those criteria are met.
</div>


## Conclusion

At this point your Bigcommerce shop will be fully integrated with LeadDyno. Good luck selling!