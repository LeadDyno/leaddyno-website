---
layout: post
title:  "Setting up LeadDyno’s Integration with Infusionsoft"
date:   2013-03-21
categories: blog
author: brett@leaddyno.com
---

We are big fans of [Infusionsoft](http://www.infusionsoft.com) at LeadDyno.  We use it extensively as our CRM and email 
marketing solution for our sister company, Chrometa (purveyors of automatic [time tracking software](http://www.chrometa.com)).

When you capture a new lead with LeadDyno, you can have the lead automatically ported over to Infusionsoft, where you 
can then take advantage of its extensive follow up marekting capabilities.  Here's how:

### Set Up the Infusionsoft Integration

From LeadDyno, click the **Settings** button, then select the **Integrations** tab.

![Infustionsoft LeadDyno Integration](/img/Integrations-tab-Infusionsoft1.png)

Enter your **Infusionsoft URL** and **API key**, and click **Test Connection**.
* Your **Infusionsoft URL** is the base URL that appears in your web browser when you access Infusionsoft
* Your **API key** can be found within Infusionsoft under **Admin > Settings > Application > Encrypted Key**

After you verify the connection is good, click **Save Integration Info**.

### Trigger the Infusionsoft Action Set

You can trigger an [Action Set](http://ug.infusionsoft.com/article/AA-00861/0/What-is-an-action-set-Legacy.html)
within Infusionsoft for each registration, conversion, and cancellation that occurs in LeadDyno.

From [Infusionsof's Help Center](http://ug.infusionsoft.com/article/AA-00861/0/What-is-an-action-set-Legacy.html):

> An action set is a series of actions that are used together. Most of the time  action sets are created automatically
> when you assign them to a trigger (e.g.  web form).

To create a new Action Set in Infusionsoft, go to **Marketing > Settings > Action Sets > Add an Action Set**.

Enter the **ID** of your Action Set that you wish to trigger for each registration, conversion, and/or cancellation.

### Action Set Example: New Registration

Here's the Action Set we assign to the Register trigger for a new trial user at Chrometa:

* We create the contact in Infusionsoft (via the LeadDyno integration), and add them to our Free Trial Follow-Up
  Sequence.  This is a series of 6 emails that is automatically delivered to our prospect during their 14-day free trial
  period.

* We also apply two tags - the first indicates where they came from, and the second classifies them as a new lead.

![Register Action Set Example](/img/Register-Action-Set-Example.png)

And there you have it - your affiliate / online ad tracking tool is synced up with your automated marketing CRM.
An Online Marketing Dream Team for small business owners!
