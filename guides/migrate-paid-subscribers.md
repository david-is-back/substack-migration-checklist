# Migrating Paid Subscribers from Substack

Paid subscribers are the highest-stakes part of any Substack migration. These are the people who pay you, and the two worst outcomes of a migration — charging someone twice, or cutting off access they paid for — both happen here. Move slowly and deliberately through this part.

> Paid subscriber migration can be more complex than free subscriber migration because billing, access, renewal dates, and customer records may not transfer automatically between platforms.

## Understand what you actually have

Substack bills paid subscriptions through Stripe, using a Stripe account connected to your publication. Before planning anything:

- [ ] Export your paid subscriber list from Substack (see [How to Export Your Substack Data](export-from-substack.md)).
- [ ] Log in to Stripe and confirm you can see the customers and active subscriptions.
- [ ] Export your Stripe customer and subscription data as a second record.
- [ ] Record each subscriber's **renewal date** — the date they will next be charged.
- [ ] Record **expiration dates** for cancelled-but-still-active and comped/gifted subscriptions.
- [ ] Note plan types: monthly, annual, founding/supporter tiers, discounts.

## The core decision: transfer billing, or re-subscribe?

There are broadly two paths, and which is available depends on your destination platform and how your Stripe account is set up:

**1. Transfer the billing relationship.** Some platforms can connect to the same Stripe account (or accept a Stripe data migration) and continue charging existing subscriptions without interruption. When this works, readers do nothing and billing continues seamlessly. Whether it works depends on the platform, on how Substack created the subscriptions in Stripe, and sometimes on a support request to one or both platforms. Do not assume it is possible — confirm it explicitly with your new platform before promising continuity to your readers.

**2. Ask readers to re-subscribe.** The simpler, always-available path: cancel renewals on the old setup and ask paid subscribers to subscribe again on the new platform. It is operationally cleaner but you will lose some percentage of paid subscribers in the transition, so it needs careful communication and generous handling of the overlap period.

Many migrations end up as a hybrid: billing transfers for most subscribers, with a manual re-subscribe path for edge cases.

## Rules that apply on either path

- [ ] **Never double bill.** If a reader paid Substack through, say, September, they must not be charged on the new platform before September. Use comped access, trial periods, or delayed start dates to bridge the gap.
- [ ] **Never cut access early.** A reader who paid for 12 months gets 12 months, wherever the content lives. If the new platform can't honor remaining time automatically, comp them manually until their original expiration date.
- [ ] **Keep a manual record.** Maintain a spreadsheet of every paid subscriber, their plan, renewal date, and migration status. Update it as each one transitions. If anything goes wrong with either platform's data, this spreadsheet is your source of truth.
- [ ] **Offer a grace period.** Give readers overlap time where access works on both platforms (or generous comped access on the new one) rather than a hard cutover day.
- [ ] **Be reachable.** Billing questions will come. Make sure your reply-to address works and you answer quickly during the transition.

## Communicate separately with paid subscribers

Do not fold paid subscribers into your general migration announcement. They deserve a dedicated email that answers, explicitly:

- Will I be charged twice? (No — and say how you're ensuring it.)
- Will I lose access to anything? (No — and say for how long access is guaranteed.)
- Do I need to do anything? (Ideally nothing; if re-subscribing is needed, give exact steps and a deadline that is far away.)
- Who do I contact if billing looks wrong? (You, at a real address.)

A ready-to-adapt email is in the templates folder: [migration-announcement-paid-subscribers.md](../templates/migration-announcement-paid-subscribers.md).

## Test before you rely on it

- [ ] Create a test account and complete a real paid checkout on the new platform.
- [ ] Verify the test account can access premium posts and the paid archive.
- [ ] Verify a free account **cannot** access premium content.
- [ ] Verify the receipt/billing emails the new platform sends look right.
- [ ] If billing transferred: pick a handful of real subscribers and confirm their subscription, plan, and renewal date look correct on the new platform and in Stripe.

## Paid migration checklist

- [ ] Paid subscriber data exported from Substack and Stripe
- [ ] Renewal and expiration dates recorded for every paid subscriber
- [ ] Transfer-vs-resubscribe decision made and confirmed with the new platform
- [ ] Double-billing prevention plan in place
- [ ] Access continuity plan in place (no one loses paid time)
- [ ] Manual tracking spreadsheet created
- [ ] Dedicated paid-subscriber email drafted and scheduled
- [ ] Grace period decided
- [ ] Premium access tested end to end on the new platform

## Next steps

- [Move Your Custom Domain from Substack](move-your-custom-domain.md)
- Back to the full [Substack Migration Checklist](../checklist.md)

---

## Need help migrating?

This guide is maintained by [LetterBucket](https://letterbucket.com). If you are moving a paid newsletter from Substack and want help planning the billing transition, [contact us](https://letterbucket.com/contact).
