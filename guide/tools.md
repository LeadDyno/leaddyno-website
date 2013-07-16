---
layout: guide
title: "Affiliate Tracking Software & Online Marketing System: LeadDyno"
nav: guide > tools
---

## Affiliate Tools

<a class="docs-anchor" id='affiliate_form'> </a>
### Affiliate Sign Up Form

If you'd like to enable anyone to join your affiliate program, you can use this form:

<pre class="prettyprint">
    &lt;form action="https://app.leaddyno.com/provision" method="post">
      &lt;label>Enter Your Email:&lt;/label>
      &lt;input name="email"/>
      &lt;input type="hidden" name="key" value="<span class="pub-key-rep">YOUR_PUBLIC_KEY</span>"/>
      &lt;input type="submit" value="Join Our Affiliate Program"/>
    &lt;/form>
</pre>

Which will render like so:

<form action="https://app.leaddyno.com/provision" method="post">
  <label>Enter Your Email:</label>
  <input name="email"/>
  <input type="hidden" name="key" value="9d7969b29fee56ee8ab1d747c1b41a2cd7a5e1ce"/>
  <input type="submit" value="Join Our Affiliate Program"/>
</form>

<div class="alert alert-info">
  <strong>Note:</strong> This form is hooked up to the LeadDyno affiliate program, please join it and recommend
  us!
</div>

<a class="docs-anchor" id='affiliate_link'>&nbsp;</a>
### Affiliate Link/Button

If you have a users email (for example, if they are signed in on your site, or have just made a purchase,
you can render a link, rather than a form, to join your affiliate program:

<pre class="prettyprint">
&lt;a href="https://app.leaddyno.com/provision?email=example%40example.com&amp;key=<span class="pub-key-rep">YOUR_PUBLIC_KEY</span>">
  Click To Join Our Affiliate Program
&lt;a>
</pre>

Note that you will need to URL escape the email address of the user, and that you can style the link
however you'd like


<a class="docs-anchor" id='sharing_buttons'>&nbsp;</a>

### Share Buttons

You can create share buttons that are tracked and tied to the content managed in the 
[Social Content](https://app.leaddyno.com/content) section of LeadDyno using our 'instant share'
functionality. This will provision someone as an affiliate and then send them on to the target social medium
in a single action.

Here is example form code:

<pre class="prettyprint">
  &lt;form id="sharing_form" class="sharing_form" target="_blank" action="https://app.leaddyno.com/instant_share" method="get">
    &lt;input type="hidden" name="key" value="<span class="pub-key-rep">YOUR_PUBLIC_KEY</span>"/>
    &lt;strong>Enter Your Email:&lt;/strong> &lt;input type="text" name="email">
    &lt;br/>
    &lt;input style="background: white url('http://www.leaddyno.com/img/social/32px/Facebook.png'); margin-bottom: -10px; border: 0; height: 32px; width: 32px; line-height: 999px; overflow: hidden; font-size: 0;"
              name="type"
              value="facebook"
              type="submit"
              alt="Share on Facebook" />
    &lt;input style="background: white url('http://www.leaddyno.com/img/social/32px/Twitter.png')"
              name="type"
              value="twitter"
              type="submit"
              alt="Share on Twitter" />
  &lt;/form>
</pre>

In this form, `email` and `key` are the usual suspects, and an additional parameter, `type` is set depending on the
submit button clicked..  The values for `type` can be:

* `twitter` - Posts a tweet
* `email` - Creates an email 
* `facebook` - Posts to Facebook 
* `gplus` - Posts to Google+ 
* `linkedin` - Posts to LinkedIn

As with the affiliate signup URL https://app.leaddyno.com/instant_share accepts both `GET` and `POST`, so you can render 
these as simple links if you have the email for your user available:

<pre class="prettyprint">
&lt;a href="https://app.leadyno.com/instant_share?email=example%40example.com&amp;key=<span class="pub-key-rep">YOUR_PUBLIC_KEY</span>&amp;type=twitter">
  Share Us On Twitter
&lt;a>
</pre>

Finally, if you want to override the standard social content of a tweet or post defined on the 
[Social Content](https://app.leaddyno.com/content) page, you can use the following form variables to do so

* facebook_subject - Change the facebook subject
* facebook_message - Change the facebook message
* twitter_message - Change the twitter message
* linkedin_subject - Change the linkedin subject
* linkedin_message - Change the linkedin message
* email_subject - Change the email subject
* email_message - Change the email message

<div class="alert alert-info">
  <strong>Note:</strong> Links and URLs in these variables will be specialized for affiliates automatically.
</div>
