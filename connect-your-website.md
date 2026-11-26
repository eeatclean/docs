---
title: Connect your website
description: How EEATClean reads your website, the reader name and IP addresses to allow in a firewall, and what to do when your articles can't be read.
---

# Connect your website

EEATClean reads your public pages, like a visitor would. It works with any website that has a sitemap: WordPress, Webflow, Shopify, Wix, Squarespace, Ghost, Drupal and more.

Most websites work right away. Some security settings, however, block automated readers. This page explains how to let EEATClean in.

## Who reads your website

EEATClean reads your pages with this identity:

| What | Value |
| --- | --- |
| Name (user agent) | `Mozilla/5.0 (compatible; EEATClean/1.0; editorial content audit)` |
| IP address (IPv4) | `144.126.155.22` |
| IP address (IPv6) | `2605:a140:2321:1447::1` |

It only reads. It never posts a form, logs in or changes anything on your website.

## Your firewall blocks EEATClean

Firewalls and security plugins sometimes refuse unknown readers. In that case, EEATClean tells you which protection answered, when it can recognize it.

To fix it, add the IP addresses above to the allowed visitors of your protection:

- **Cloudflare**: create an IP Access rule that allows these addresses. [Cloudflare guide](https://developers.cloudflare.com/waf/tools/ip-access-rules/)
- **Sucuri**: add the addresses to the allowlist of your website firewall. [Sucuri docs](https://docs.sucuri.net/)
- **Wordfence**: add the addresses to the allowlisted IPs in the Wordfence options. [Wordfence help](https://www.wordfence.com/help/)
- **SiteGround**: ask SiteGround support to allow the addresses, or check their knowledge base. [SiteGround guide](https://www.siteground.com/kb/)
- **Another host or plugin**: send the table above to your webmaster or your host, and ask them to allow these addresses.

Then go back to EEATClean and check again.

## robots.txt

EEATClean reads your website because you asked for its analysis. It isn't a crawler exploring the web. For this reason, the crawling rules of your `robots.txt` don't apply to it. EEATClean still reads the `Sitemap:` lines of the file to find your articles.

Real protections, such as a firewall, a challenge page or a login, still stop it.

## Other messages and what to do

| Message | What it means | What to do |
| --- | --- | --- |
| We could not find your articles | No sitemap or WordPress listing was found. | Enter the address of your sitemap, usually `yoursite.com/sitemap.xml`. |
| Your articles require a login | Your articles are behind a login. | EEATClean analyzes public pages only. Use a website whose articles anyone can read. |
| This address leads somewhere else | The address redirects to another website, or keeps redirecting. | Enter the final address of your website. |
| This address cannot be checked | The address isn't a public HTTPS website. | Enter the public HTTPS address of your website. |
| Your website is limiting requests | Your server asked us to slow down. | Wait a few minutes, then try again. |
| We could not connect to your website | Your server didn't answer. | Check the address. If your site opens normally for you, contact us. |

If nothing here helps, email [support@eeatclean.com](mailto:support@eeatclean.com) with the address of your website. We'll look at the cause with you.
