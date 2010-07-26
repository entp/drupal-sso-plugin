Installation
------------
Copy the multipass folder to your module directory and then enable it on the admin modules page.

Description
-----------
What is Tender Support SSO?

When you build a website with Drupal, it already comes with a user registration system. Tender Support compliments your application, product or marketing site by being able to share this registration systems information.

With Tender Support SSO you don't need users to re-register with Tender Support, who wants to do that? Terrible people. That's whom. We can pass all the user information as securely as possible over a simple hyperlink. 

This plugin goes one step further and makes sure you don't have to do any of the weird encryption and crazy programming to secure the info. All you need to know are three simple things:

1. Your Tender url (e.g. http://help.tender.com)
2. Your SSO Key
3. Your Tender Key

How fantastic is that? This plugin will automatically generate that anchor element for you. It looks something like this:

<a href="(the generated url)">Support</a>

Enabling Tender Support SSO
---------------------------
In order to use this plugin you need to enable Tender Support SSO on your Tender application. Here's how:

1. Login to your Tender Support application dashboard
2. Click on the Site Settings navigation item
3. Scroll down to the bottom of the page
4. Where it says "MultiPass Single Sign On" click on "Enabled".
5. Copy and paste your SSO API key and your site key, make sure you keep them separate and you know which is which. 

You can then use those to generate your Tender Support SSO link.

Usage
-----
Place <?php theme('multipass', 'yourtenderlink', 'your_sso_key', 'your_tender_site_key'); ?> in your theme template.

This will generate an anchor element (link omitted due to size): 

<a href="(Tender Support SSO link)">Support</a>.

Optionally, you may use a fifth parameter and give the link a different text:

e.g. <?php theme('multipass', 'yourtenderlink', 'your_sso_key', 'your_tender_site_key', 'Help'); ?>

This will generate <a href="(Tender Support SSO link)">Help</a>

Thanks for using Tender Support!