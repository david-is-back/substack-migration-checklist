# Move Your Custom Domain from Substack

If your publication runs on a custom domain (like `news.yourdomain.com` or `yourdomain.com`), moving that domain is the moment your migration becomes visible to the world. Done in the right order, it involves a few minutes of downtime at most and all your old links keep working. Done in the wrong order, readers hit dead pages and old links break.

The golden rule: **set everything up on the new platform first, and change DNS last.**

## Before you touch anything

- [ ] Confirm your current setup: which domain or subdomain points to Substack, and what DNS records make that happen. Log in to your DNS provider (Cloudflare, Namecheap, GoDaddy, your registrar) and screenshot the current records.
- [ ] Confirm who controls the DNS. If someone else set it up years ago, find the login now, not on migration day.
- [ ] Lower the DNS **TTL** (time to live) on the relevant records to something short — 300–600 seconds — a day or two before the switch, if your provider allows it. Low TTL means the change propagates fast, and means you can roll *back* fast if something is wrong.

## Set up the domain on the new platform

- [ ] Add your custom domain in the new platform's settings **before** changing any DNS.
- [ ] Note the DNS records the platform asks for — usually a CNAME pointing at the platform, sometimes A records for a root domain.
- [ ] If you are changing subdomains (e.g. moving from `yourdomain.com` on Substack to `news.yourdomain.com`), plan redirects between them.
- [ ] Do **not** delete the existing Substack records yet. Add or prepare the new ones; the old ones stay until the new setup is verified.

## Make the switch

- [ ] Pick a low-traffic time (not right before a scheduled send).
- [ ] Update the CNAME (or A records) to point at the new platform.
- [ ] Wait for the platform to detect the domain and issue an SSL certificate. This usually takes minutes; occasionally longer.
- [ ] Verify SSL: the padlock shows and `https://` loads without warnings.

## Verify everything

- [ ] Homepage loads on the custom domain.
- [ ] Signup page loads and the form works.
- [ ] Old post URLs resolve — test several, including your most-linked posts.
- [ ] Redirects work if your URL structure changed (see [Migrate Your Substack Archive](migrate-your-archive.md)).
- [ ] Test from a different network or with your phone on cellular — your home network may cache old DNS.
- [ ] Monitor propagation for 24–48 hours; a tool like a public DNS checker shows when the change has reached resolvers worldwide.

Only after everything above checks out should you remove the old Substack-specific DNS records — and even then, there is rarely urgency.

## Update links everywhere else

The domain now points at your new platform, but plenty of links live outside your control of DNS:

- [ ] Social media bios (X/Twitter, LinkedIn, Instagram, Bluesky, YouTube)
- [ ] Link-in-bio pages
- [ ] Email signature
- [ ] Your personal or company website
- [ ] Podcast show notes, speaker bios, directories
- [ ] Google Search Console — verify the property still works and submit the new sitemap if the URL structure changed

## If you didn't have a custom domain

If your newsletter lived at `yourname.substack.com`, you cannot move or redirect that domain — Substack owns it. Your options: set up a custom domain on the new platform (a good moment to start owning your URLs), keep the Substack publication alive with a pinned post pointing to your new home, and update every external link you control.

## Quick-reference template

A condensed version of this guide for migration day: [domain-switch-checklist.md](../templates/domain-switch-checklist.md).

## Next steps

- [Deliverability Checklist After Migrating from Substack](deliverability-checklist.md)
- Back to the full [Substack Migration Checklist](../checklist.md)

---

## Need help migrating?

This guide is maintained by [LetterBucket](https://letterbucket.com). If you want help pointing your domain at your new newsletter home, [contact us](https://letterbucket.com/contact).
