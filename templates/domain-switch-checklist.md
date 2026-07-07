# Domain Switch Checklist

A condensed, fill-in checklist for the day you point your custom domain away from Substack. For the full walkthrough and the reasoning behind the order of operations, see [Move Your Custom Domain from Substack](../guides/move-your-custom-domain.md).

## Record your current setup

| Item | Value |
|---|---|
| Current DNS provider | |
| Current Substack domain (e.g. `news.yourdomain.com`) | |
| New platform | |
| DNS records required by new platform | |
| Current TTL value | |
| Screenshot of current DNS records saved? | |

## Before the switch

- [ ] Domain added to the new platform (before any DNS changes)
- [ ] Required DNS records from the new platform written down
- [ ] TTL lowered to 300–600 seconds at least 24 hours in advance
- [ ] Old Substack DNS records documented but **not** deleted
- [ ] Switch scheduled at a low-traffic time, not before a scheduled send

## The switch

- [ ] CNAME / A records updated to point at the new platform
- [ ] New platform shows the domain as verified
- [ ] SSL certificate issued — `https://` loads with no warnings

## Verify

- [ ] Homepage tested on the custom domain
- [ ] Signup page tested (submit a real test signup)
- [ ] Old post URLs tested — including your most-linked posts
- [ ] Redirects tested, if the URL structure changed
- [ ] Analytics receiving traffic from the custom domain
- [ ] Tested from a second network (phone on cellular) to rule out DNS caching

## Afterwards

- [ ] DNS propagation monitored for 24–48 hours
- [ ] Google Search Console verified / sitemap resubmitted if needed
- [ ] Social bios, link-in-bio pages, email signature, and website links updated
- [ ] Old Substack-specific DNS records removed (only after everything is verified)
- [ ] TTL raised back to a normal value (e.g. 3600+)

---

Part of the [Substack Migration Checklist](../checklist.md), maintained by [LetterBucket](https://letterbucket.com/migrate-from-substack).
