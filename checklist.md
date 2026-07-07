# Substack Migration Checklist

The complete checklist for migrating your newsletter from Substack to another platform. Work through the sections in order. Each section links to a detailed guide where one exists.

Before you start: read the [Quick warning](README.md#quick-warning). Do not touch your live Substack publication until your data is exported and your new setup is tested.

## 1. Before you migrate

- [ ] Decide why you are migrating (costs, features, ownership, design, deliverability) and write it down — it will shape your platform choice.
- [ ] Choose your new newsletter platform (LetterBucket, Ghost, Kit, Beehiiv, WordPress, or another).
- [ ] Confirm the new platform supports what you actually need: paid subscriptions, custom domain, archive import, and CSV subscriber import.
- [ ] Create your new publication on the new platform **before** touching anything on Substack.
- [ ] Make a list of all current Substack assets: subscriber list, posts, custom domain, signup embeds, recommendation links, welcome email, about page.
- [ ] Note where your Substack links live outside Substack: social bios, website, email signature, podcast show notes, link-in-bio pages.
- [ ] Pick a migration date with buffer time on both sides.
- [ ] Avoid migrating right before a major send, launch, sale, or paid billing cycle.
- [ ] If you have paid subscribers, read [Migrating Paid Subscribers from Substack](guides/migrate-paid-subscribers.md) before scheduling anything.

## 2. Export your Substack data

Detailed guide: [How to Export Your Substack Data](guides/export-from-substack.md)

- [ ] Export your full publication data from Substack settings.
- [ ] Export your subscriber list as CSV.
- [ ] Export free subscribers.
- [ ] Export paid subscribers separately, if applicable.
- [ ] Export your post archive (usually included in the full publication export).
- [ ] Download all export files to your computer.
- [ ] Store one untouched backup of every file somewhere safe (cloud storage plus local copy).
- [ ] Create a working copy of the subscriber CSV for cleanup — never edit the original export.
- [ ] Open each file and verify it actually contains your data before moving on.

## 3. Review your subscriber list

Detailed guide: [Clean Your Subscriber List Before Import](guides/clean-your-subscriber-list.md)

- [ ] Check that the email column exists and every row has a valid-looking address.
- [ ] Separate free and paid subscribers (or verify the status column distinguishes them).
- [ ] Identify unsubscribed, bounced, comped, gifted, and long-inactive subscribers.
- [ ] Decide what to do with each of those groups — do **not** import unsubscribed or bounced contacts as active.
- [ ] Preserve status fields (free/paid, active/expired).
- [ ] Preserve signup dates.
- [ ] Preserve source and referral fields if present.
- [ ] Remove duplicate email addresses.
- [ ] Check GDPR / consent requirements for your audience — you can generally email people who subscribed to your newsletter, but keep the export as your consent record.
- [ ] Save a clean CSV formatted for import (see the [subscriber import template](templates/subscriber-import-template.csv)).

## 4. Prepare your new newsletter platform

- [ ] Set your publication name.
- [ ] Set your sender name (the "from" name readers will see).
- [ ] Set your reply-to address — use one you actually check.
- [ ] Apply your branding: colors, fonts, header.
- [ ] Upload your logo.
- [ ] Upload a favicon.
- [ ] Set up your homepage.
- [ ] Set up your signup page and any embedded signup forms.
- [ ] Enable your public archive if you want one.
- [ ] Configure your email footer.
- [ ] Add a physical mailing address if your platform or local law requires one (CAN-SPAM does).
- [ ] Configure unsubscribe settings and verify the unsubscribe link works.
- [ ] Set up analytics.
- [ ] Set up UTM tracking if you use it.
- [ ] Import your cleaned subscriber CSV.
- [ ] Recreate segments or tags (free, paid, source) if your platform supports them.
- [ ] Import your posts (see section 5).

## 5. Migrate your content archive

Detailed guide: [Migrate Your Substack Archive](guides/migrate-your-archive.md)

- [ ] Decide which posts to migrate — you may not need all of them.
- [ ] Prioritize posts with traffic, backlinks, conversions, evergreen value, or paid content.
- [ ] Import or recreate the selected posts on the new platform.
- [ ] Review titles and slugs on every migrated post.
- [ ] Check that images and media transferred (re-upload any that did not).
- [ ] Check embeds (tweets, videos, buttons) — these often break in transfer.
- [ ] Fix internal links so they point to the new domain, not substack.com.
- [ ] Re-apply paywalls on premium posts.
- [ ] Review canonical URLs, meta titles, descriptions, and OG images if your platform exposes them.
- [ ] Set up redirects from old URLs where possible.
- [ ] Test a sample of migrated posts on desktop and mobile.

## 6. Handle paid subscribers

Detailed guide: [Migrating Paid Subscribers from Substack](guides/migrate-paid-subscribers.md)

- [ ] Export complete paid subscriber data, including plan and billing details where available.
- [ ] Record each paid subscriber's renewal date.
- [ ] Record expiration dates for any non-renewing or comped subscriptions.
- [ ] Check how your Stripe account and customer records are set up, and what (if anything) can move with you.
- [ ] Decide whether readers must re-subscribe on the new platform or whether billing can transfer.
- [ ] Plan the transition so nobody gets double billed.
- [ ] Plan the transition so nobody loses access before their paid period ends.
- [ ] Prepare a dedicated email for paid subscribers (see the [paid subscriber announcement template](templates/migration-announcement-paid-subscribers.md)).
- [ ] Offer a grace period or comped access during the switchover if needed.
- [ ] Keep a manual record (spreadsheet) of every paid subscriber, their status, and their renewal date during the transition.
- [ ] Test premium content access on the new platform with a test account.

## 7. Move your custom domain

Detailed guide: [Move Your Custom Domain from Substack](guides/move-your-custom-domain.md) · Template: [Domain switch checklist](templates/domain-switch-checklist.md)

- [ ] Confirm your current custom domain setup on Substack (which subdomain or root domain points where).
- [ ] Lower your DNS TTL a day or two in advance, if your DNS provider allows it.
- [ ] Add the domain to your new platform first.
- [ ] Prepare the DNS records the new platform requires (usually a CNAME, sometimes A records).
- [ ] Do not delete old DNS records before the new setup is verified.
- [ ] Update the CNAME (or other records) only when the new platform is ready to receive traffic.
- [ ] Verify SSL is issued and working on the new platform.
- [ ] Test the homepage on the custom domain.
- [ ] Test individual post URLs.
- [ ] Test the signup page.
- [ ] Test redirects from old URL patterns.
- [ ] Monitor DNS propagation for 24–48 hours.

## 8. Test before launch

- [ ] Send a test email to a Gmail account.
- [ ] Send a test email to an Outlook account.
- [ ] Send a test email to Apple Mail.
- [ ] Check mobile rendering in at least one mail app.
- [ ] Click every link in the test email.
- [ ] Test the unsubscribe link end to end.
- [ ] Test the signup flow as a new reader.
- [ ] Verify the confirmation / welcome email arrives and reads correctly.
- [ ] Test the paid subscription flow end to end, if applicable (use a real or test payment).
- [ ] Verify analytics are recording opens, clicks, and site visits.
- [ ] Review the public archive as a logged-out visitor.
- [ ] Verify everything works on the custom domain, not just the platform subdomain.
- [ ] Ask two or three trusted readers to sign up, receive a test send, and report anything odd.
- [ ] Run the [deliverability checklist](guides/deliverability-checklist.md).

## 9. Announce the migration

Templates: [free subscribers](templates/migration-announcement-free-subscribers.md) · [paid subscribers](templates/migration-announcement-paid-subscribers.md)

- [ ] Send the announcement to free subscribers (from Substack, before the switch, or from the new platform as the first send — pick one and be consistent).
- [ ] Send the dedicated announcement to paid subscribers with clear instructions about billing and access.
- [ ] Ask readers to reply to the first email from the new platform, or to move it to their primary inbox — this helps deliverability.
- [ ] Update your website, social bios, email signature, and link-in-bio pages with the new signup URL.
- [ ] Post the announcement publicly if you have a public archive or social audience.
- [ ] Leave a final pinned post on Substack pointing readers to the new home, if you keep the Substack page up.

## 10. Post-migration audit

Template: [Post-migration audit](templates/post-migration-audit.md)

- [ ] Compare subscriber count before and after the import.
- [ ] Compare paid subscriber count before and after.
- [ ] Review your first real send from the new platform.
- [ ] Check open rate against your Substack baseline.
- [ ] Check click rate against your Substack baseline.
- [ ] Check unsubscribe rate (a small spike is normal; a large one is not).
- [ ] Check bounce rate.
- [ ] Check spam complaints.
- [ ] Check which pages are indexed by Google (use Search Console if you have it).
- [ ] Crawl or spot-check for broken links.
- [ ] Verify redirects still work.
- [ ] Verify analytics are complete and consistent.
- [ ] Do a structured review 7 days after migration.
- [ ] Do a final review 30 days after migration — only then consider winding down the old Substack publication.

---

## Need help migrating?

This checklist is maintained by [LetterBucket](https://letterbucket.com), a simple newsletter platform for creators. If you want help moving your subscribers, archive, and newsletter website from Substack, [contact us](https://letterbucket.com/contact).

The checklist itself is platform-neutral — use it wherever you are headed.
