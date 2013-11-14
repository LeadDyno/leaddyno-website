---
layout: guide
title: "Affiliate Tracking Software & Online Marketing System: LeadDyno"
nav: guide > content
---

## Managing Marketing Content

LeadDyno allows you to create and manage marketing content that can be used by your affiliates, as well as linked to
directly from your own website.  You can manage your content by selecting the **Content Library** menu item under the
**Affiliate Content** section:

![content_list](/img/content_list.png)

Here you will see a list of content that you have created.  Each piece of content will have an icon indicating which
channel the content is designed for:

* Email
* Facebook
* LinkedIn
* Twitter
* Banner/Blog

### Adding/Editing Content

You can add content by selecting the content type from the "Add Content" button:

![content_list](/img/content_add.png)

which will take you to the content editor, where you can compose your content.

#### The Content Editor

The content editor lets you all aspects of the content:

![content_list](/img/content_editor.png)

#### Content Title

This is the internal title of the content within LeadDyno, and should describe the content, but it will **not** be
part of the content that is actually shared.

#### Primary Content

Check this to make this content the **primary** content for its channel.  This will be be the content that is used when
an affiliate clicks their quick share links (see below for more info.)

#### On Marketing Tab

Determines if this content should be available on the Marketing Content tab on your Affiliate's dashboard (see below for
more info.)

#### Subject

For some channels, a subject is available.  This will be the subject of the content that the affiliate shares.

#### Body

For all channels, a body is available.  The body will either be HTML (email and banner/html content) or plain text.  Within
the body of your content you can freely use links to your sites and these links will be automatically transformed into
affiliate links by LeadDyno when we show the content to your affiliate.

So, for example, if you have the following tweet:

    Wow, this is amazing!  http://yourproduct.com

When an affiliate shared the content, it will be modified to:

    Wow, this is amazing!  http://yourproduct.com#_a_l1

Where the affiliates tracking code is appended to the URL.

##### Note On Affiliate Discount Codes

If you are running an affiliate program that uses discount codes rather than tracking links, you can use the `$CODE` variable
in your content body to represent the affiliates discount code:

    Check it out!  http://yourproduct.com  Get 10% off using discount code '$CODE$'

will become

    Check it out!  http://yourproduct.com  Get 10% off using discount code 'l1'

### Content Details

After content is created you will be taken to a detail page, which will show information about the content:

![content_list](/img/content_show.png)

In particular, the content will be given a content URL, highlighted in the image above.  This URL can be used to
link to the content from anywhere, including your own website, newsletters, etc.

### Creating Banners

To create a banner for your affiliates, select **Add Banner/HTML Content** from the **Add Content** menu.  You will
be taken to the editor:

![content_list](/img/content_banner_1.png)

Click on the **Insert Image** button in the editor, highlighted above.  This will bring up the image picker dialog:

![content_list](/img/content_banner_2.png)

Where you can pick an image from your local machine to upload, or point to an existing image on the internet:

![content_list](/img/content_banner_3.png)

Now you can click on the image, then click **Edit** and set a link for it:

![content_list](/img/content_banner_4.png)

Set the link to point to your website and click **Save**.  You are done creating your banner, now click **Save Content**.

When an affiliate looks at this banner, they will see the content specialized for their affiliate content:

![content_list](/img/content_banner_5.png)

### Primary Content

Primary Content is the content that will be used when an affiliate clicks on the quick share buttons on their dashboard:

![content_list](/img/content_primary.png)

Content that you mark as "Primary" will be the content used for these links.  Only one piece of content per channel
can be the primary content.

Primary content also has a special set of URLs that you can link to.  If your LeadDyno affiliate site is
at `https://yourproduct.leaddyno.com` then the following URLs are linked to your primary content:

* https://yourproduct.leaddyno.com/share/email - Your primary email
* https://yourproduct.leaddyno.com/share/tweet - Your primary tweet
* https://yourproduct.leaddyno.com/share/facebook - Your primary Facebook post
* https://yourproduct.leaddyno.com/share/linkedin - Your primary LinkedIn post
* https://yourproduct.leaddyno.com/share/gplus - A Google Plush Share

###  Marketing Material

You may have additional content such as banners, other tweets or facebook posts, etc. that you want your affiliates to
have access to, you can mark them as "On Marketing Tab" and they will then appear on the marketing tab:

![content_list](/img/content_marketing_tab.png)

You can reorder the items on your marketing tab by clicking the **Marketing Tab Content** button in the Content Library:

![content_list](/img/content_marketing_tab_btn.png)

And then reordering the rows by dragging them and then clicking **Save Order**:

![content_list](/img/content_marketing_tab_reorder.png)
