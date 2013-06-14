---
layout: guides
---

# Paypal Integration Guide #


## Introduction ##

This guide explains how to integrate PayPal one-time purchase and subscription buttons into LeadDyno. The integration
between PayPal and LeadDyno allows automated tracking of lead conversion, cancellation and affiliate compensation for purchases
made via PayPal buttons.


## Paypal Buttons ##

PayPal buttons are elements you put on your website that allow consumers to purchase your products or services. To
create the buttons, from the PayPal interface, put your mouse over **Profile** and select **My Selling Tools** from the drop down list.
From there, select the **Update** link next to **PayPal Buttons** as seen in the image below.

![PayPal Selling Tools](/img/pp_guide_create_buttons.png)


From here, you will see the **My Buttons** page. To create a new button integrated with LeadDyno, select **Create New Button**
from the right *Related Items* menu. Select either **Buy Now** or **Subscriptions**.


### Subscription Button ###

Subscription buttons allow your customers to subscribe to a recurring service and they are automatically charged based
on the *Billing Cycle* you choose. In the image below, the button would charge the customer $50 every month forever until
they login and cancel their subscription.

![PayPal Subscription Button](/img/pp_guide_subscription_button.png)

After selecting **Subscriptions** from the *Choose a button type* list, it will ask for an *Item name* and
*Subscription ID*. In the Item name field, put the name of the service, and in Subscription ID, put in the LeadDyno
commission plan code. Below is an example LeadDyno commission plan. The **Code** (in this case *gold*) must match the
**Subscription ID** defined for the PayPal button. If you do not supply a Subscription ID in the button, it will use
the Default commission plan defined in LeadDyno.


![LeadDyno Commission Plan](/img/pp_guide_leaddyno_commission_plan.png)


In the example above, affiliates would be compensated $10 starting after the first month for any customers they bring
to the site that sign up for the $50/month *Gold Plan* forever until the customer cancels their subscription.

After setting all the button parameters needed for your service, click *Create Button*. You will be presented with the
HTML to place on your website.


### One Time Purchase Button ###

From a LeadDyno integration perspective, one time buttons are very similar to subscription buttons. One time payment
buttons are used if you want to sell individual items or a service that does not automatically renew on a specific interval.

On the Create PayPal payment button page, supply an *Item name* for the button that represents the item being purchased
and an *Item ID* that matches a LeadDyno commission plan code. In the image below, this button would be used to purchase
an item named **My Widget** and associated to the LeadDyno commission plan **widget** that would give the referring affiliate
either a fixed amount or some percentage of the sale.

![PayPal Buy Now Button](/img/pp_guide_buynow_button.png)


## Enable PayPal Integration with LeadDyno ##

To enable PayPal integration with LeadDyno, call the function
{% highlight javascript %}
  LeadDyno.initPaypal();
{% endhighlight %}

in addition to the other LeadDyno visit tracking code

A typical complete installation of LeadDyno with PayPal integration enabled would be to have the following in the header section on
every page of your site:

{% highlight html %}
<script type="text/javascript" src="https://static.leaddyno.com/js"></script>
<script>
  LeadDyno.key = "YOUR_PUBLIC_KEY";
  LeadDyno.recordVisit();
  LeadDyno.initPaypal();
 </script>
{% endhighlight %}

Replace **YOUR_PUBLIC_KEY** with your public API key found on the [LeadDyno Dashboard](https://app.leaddyno.com/settings/account).



## Conclusion ##

LeadDyno is able to seemlessly integrate with both one time and subscription PayPal buttons with no changes to the html
of the button. The only coordination between the button and LeadDyno is the Item ID (for one time buttons) or the
Subscription ID (for subscription buttons) in the PayPal button editor which needs to match a LeadDyno compensation plan.
If the default LeadDyno compensation plan is the desired plan to be used with the transaction, then even this coordination is not required.

A single line of javascript, enabling the PayPal integration, is enough for LeadDyno to be in the loop on PayPal transactions
to track conversions, cancellations and affiliate compensation.



