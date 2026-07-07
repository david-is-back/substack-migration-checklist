# Post-Migration Audit

Fill this in after your migration to confirm nothing was lost and your new setup performs at least as well as Substack did. Do a first pass after your first real send, a structured review at 7 days, and a final review at 30 days. Only after the 30-day review should you consider winding down the old Substack publication.

Related: [Deliverability checklist](../guides/deliverability-checklist.md) · [full checklist](../checklist.md#10-post-migration-audit)

## Subscriber counts

| Metric | Value |
|---|---|
| Subscriber count before migration (Substack) | |
| Subscriber count after import (new platform) | |
| Difference explained? (excluded unsubscribes/bounces) | |
| Paid subscribers before migration | |
| Paid subscribers after migration | |
| Every paid subscriber accounted for? | |

- [ ] Import difference matches the contacts you deliberately excluded during [list cleaning](../guides/clean-your-subscriber-list.md)
- [ ] Paid subscriber list cross-checked against your manual tracking spreadsheet

## First send from the new platform

| Metric | New platform | Substack baseline |
|---|---|---|
| First send date | | — |
| Open rate | | |
| Click rate | | |
| Bounce rate | | |
| Unsubscribe rate | | |
| Spam complaints | | |

- [ ] Open and click rates within a reasonable range of your Substack baseline (platforms measure differently — look for collapses, not small deltas)
- [ ] Bounce rate very low (a spike means bad addresses got imported)
- [ ] Spam complaint rate well under 0.1%

## Website, domain, and SEO

| Item | Status |
|---|---|
| Domain status (resolving to new platform) | |
| SSL status | |
| Indexed pages (Search Console or `site:` check) | |
| Top broken links found | |
| Top redirected pages verified | |

- [ ] Homepage, signup page, and archive all load on the custom domain
- [ ] Spot-checked your top posts for broken images, embeds, and internal links
- [ ] Redirects from old URLs verified
- [ ] Analytics recording site visits and email engagement

## 7-day review

Date: ______

Notes (deliverability trend, reader replies, billing questions, anything broken):

-
-
-

## 30-day review

Date: ______

Notes (subscriber trend vs pre-migration, paid churn, open-rate trend, remaining loose ends):

-
-
-

- [ ] All loose ends from the 7-day review resolved
- [ ] Decision made about the old Substack publication (keep as pointer / wind down)
- [ ] Backups of the original export still stored safely

---

Part of the [Substack Migration Checklist](../checklist.md), maintained by [LetterBucket](https://letterbucket.com). Need help migrating? [Contact us](https://letterbucket.com/contact).
