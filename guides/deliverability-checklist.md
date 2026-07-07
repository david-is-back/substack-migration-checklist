# Deliverability Checklist After Migrating from Substack

On Substack, deliverability was mostly handled for you. After migrating, some of it becomes your responsibility — and the first sends from a new platform are exactly when inbox providers are deciding how to treat your mail. This checklist covers what to verify before and after your first real send.

## Sender identity

- [ ] **Sender name** is set and matches what readers expect — if your emails always came from "Jane Doe" or your publication name, keep it. A changed sender name plus a new sending infrastructure is a recipe for "who is this?" spam reports.
- [ ] **Reply-to email** is a real address you monitor. Replies are both a reader-service and a deliverability signal.
- [ ] **From address** — if your new platform supports sending from your own domain (e.g. `hello@yourdomain.com`), use it. Mail from a domain you own, that readers recognize, builds durable reputation.

## Authentication: SPF, DKIM, DMARC

These are DNS records that prove your email is really from you. Your new platform will give you the exact records to add — this is standard setup, not optional.

- [ ] **SPF** — authorizes the platform's servers to send on behalf of your domain. Usually merged into an existing TXT record; note that a domain can only have one SPF record.
- [ ] **DKIM** — cryptographically signs your emails. Usually one or more CNAME or TXT records from the platform.
- [ ] **DMARC** — tells inbox providers what to do with mail that fails SPF/DKIM. Gmail and Yahoo require DMARC for bulk senders. A minimal starting record: `v=DMARC1; p=none; rua=mailto:you@yourdomain.com` — start with `p=none` and monitor before tightening.
- [ ] **Custom sending domain** — if the platform supports it, complete its verification flow so mail is sent and authenticated under your domain rather than a shared one.
- [ ] Verify all records with the platform's built-in checker (or a free DNS/DMARC checker) before sending anything.

## Test sends

- [ ] Send a test to a **Gmail** account — check the Primary/Promotions tab placement and open the "show original" view to confirm SPF, DKIM, and DMARC all show `PASS`.
- [ ] Send a test to an **Outlook / Hotmail** account.
- [ ] Send a test to **Apple Mail / iCloud**.
- [ ] Check the **spam folder** in each. A test landing in spam is a warning to fix authentication before the real send, not a fluke to ignore.
- [ ] Check rendering on mobile.

## Your first real sends

- [ ] In your announcement, ask readers to **reply** to the email or **move it to their primary inbox** — both are strong positive signals to inbox providers, and the migration announcement is the natural moment to ask.
- [ ] If you are sending from a brand-new domain or subdomain, **avoid blasting your full list at once**. New sending domains have no reputation; a sudden large volume looks like spam. Warm up: send to your most engaged segment first, then expand over a few sends. (If your platform sends from its own established infrastructure, this matters less — ask them.)
- [ ] Consider a small, low-stakes **warm-up announcement** before your first major issue, so the first send from the new setup isn't also your most important one.

## Monitor after each send

- [ ] **Bounce rate** — should be very low if you [cleaned your list](clean-your-subscriber-list.md). A spike means bad addresses got imported.
- [ ] **Unsubscribe rate** — a small bump after a migration is normal; a large one suggests readers don't recognize the new emails.
- [ ] **Spam complaints** — the metric to watch most closely. Keep it well under 0.1%. Gmail's Postmaster Tools is free and shows your domain's spam rate directly.
- [ ] **Open rate vs your Substack baseline** — expect some noise (different platforms measure opens differently), but a collapse means inbox placement problems.

Record all of this in the [post-migration audit template](../templates/post-migration-audit.md).

## Next steps

- [Post-migration audit template](../templates/post-migration-audit.md)
- Back to the full [Substack Migration Checklist](../checklist.md)

---

## Need help migrating?

This guide is maintained by [LetterBucket](https://letterbucket.com). If you want help getting authentication and deliverability right on your new setup, [start your migration here](https://letterbucket.com/migrate-from-substack).
