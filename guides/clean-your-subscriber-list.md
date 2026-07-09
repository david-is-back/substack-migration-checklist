# Clean Your Subscriber List Before Import

Importing your Substack subscriber CSV into a new platform without cleaning it first is one of the most common migration mistakes. A dirty import can hurt your deliverability from day one — bounced addresses and re-mailed unsubscribers are exactly what spam filters watch for.

Work on a **copy** of your export, never the original (see [How to Export Your Substack Data](export-from-substack.md)).

> **Tip:** the free [substack-migration-check](https://github.com/david-is-back/substack-migration-skill) skill for Claude Code runs every check on this page automatically and produces a cleaned, import-ready CSV — offline, without your subscriber data leaving your machine. The manual walkthrough below is still worth reading so you know what it did and why.

## What to check, column by column

### Missing email addresses

Sort by the email column and delete any rows with an empty or obviously malformed address (no `@`, trailing spaces, commas inside the address). One bad row can break an entire import on some platforms.

### Duplicate contacts

Remove duplicate email addresses. If duplicates differ (one free, one paid), keep the paid row. Most spreadsheet tools can highlight duplicates; in Google Sheets use `Data → Data cleanup → Remove duplicates`.

### Unsubscribed users

Do **not** import unsubscribed contacts as active subscribers. Emailing people who opted out damages your sender reputation and may violate anti-spam law. Either exclude them entirely or import them with an unsubscribed status if your new platform supports it (useful as a suppression list).

### Bounced users

Addresses that hard-bounced on Substack will bounce on your new platform too. Exclude them. A high bounce rate on your first send from a new platform is a strong negative deliverability signal.

### Paid vs free status

Verify the column that distinguishes paid from free subscribers survived the export and is accurate. Spot-check a few known paid subscribers. This column drives access to premium content, so mistakes here directly affect paying readers.

### Signup date

Keep the original signup date if your new platform can import it. It preserves your consent record and lets you segment by subscriber age later.

### Subscription expiration date

For paid subscribers, keep (or add) the date their current paid period ends. You will need it to avoid cutting access early — see [Migrating Paid Subscribers from Substack](migrate-paid-subscribers.md).

### Tags or segments

If you used Substack sections or maintained any grouping, translate it into a tags column so you can recreate segments after import.

### Referral source

If the export includes a source or referral column, keep it. Knowing which subscribers came from recommendations, imports, or organic signups is hard to reconstruct later.

### Country or timezone

If available, keep it — useful for send-time optimization and for knowing which privacy laws apply to parts of your list.

### Consent / GDPR notes

You can generally continue emailing people who subscribed to your newsletter — the subscription moves with the newsletter, not the platform. But keep your untouched export as the consent record, and if part of your audience is in the EU/UK, make sure your new platform's signup flow and privacy policy meet GDPR requirements going forward. When in doubt about a specific segment (e.g. an old list you once imported into Substack from elsewhere), err on the side of excluding it.

## Recommended columns for import

Most platforms accept a CSV with columns along these lines:

```csv
email,name,status,is_paid,subscription_status,subscription_expires_at,created_at,source,tags
```

A ready-to-use file with example rows is in the templates folder: [subscriber-import-template.csv](../templates/subscriber-import-template.csv). Map your Substack export columns onto this structure, then export the cleaned sheet as CSV (UTF-8).

## Final checks before import

- [ ] No empty or malformed email addresses
- [ ] No duplicates
- [ ] Unsubscribed and bounced contacts excluded (or marked as suppressed)
- [ ] Paid status verified against known paid subscribers
- [ ] Signup dates preserved
- [ ] Expiration dates present for paid subscribers
- [ ] File saved as CSV, UTF-8, with a header row
- [ ] Untouched original export still stored safely

## Next steps

- Continue with section 4 of the [Substack Migration Checklist](../checklist.md#4-prepare-your-new-newsletter-platform)
- If you have paid subscribers: [Migrating Paid Subscribers from Substack](migrate-paid-subscribers.md)

If you are migrating to LetterBucket, you can import your cleaned CSV from the Subscribers section.
