# How to Export Your Substack Data

Exporting your data is the first real step of any Substack migration, and the one you should do before anything else. Once you have a complete export — subscribers, posts, and paid subscriber records — everything else in the migration becomes reversible.

This guide covers:

- Exporting your full publication archive (posts and settings)
- Exporting your email list as a subscriber CSV
- Exporting paid subscriber data
- Storing backups properly
- Keeping the original export untouched
- Creating a working copy for cleanup and import

> Substack's interface may change over time, so use this guide as a practical reference and always verify the current export options in your own dashboard.

## What Substack lets you export

Substack provides a publication-level data export that typically includes your published posts (as HTML files), your subscriber list, and some publication metadata. Subscribers can also be exported separately as a CSV from the subscribers page. What is **not** included: your Substack recommendations, notes, and — importantly — the billing relationship with paid subscribers, which lives in Stripe (see [Migrating Paid Subscribers from Substack](migrate-paid-subscribers.md)).

## Export your full publication data

1. Open your Substack dashboard.
2. Go to your publication settings.
3. Look for the export, import/export, or data section.
4. Create a new export.
5. Wait until the export is ready.
6. Download the ZIP file.
7. Store a backup before editing anything.

The export ZIP usually contains a folder of post files and a CSV of your email list. Unzip it and open a few files to confirm the export is complete — a truncated or failed export is easier to fix now than after you have cancelled anything.

## Export your subscriber list (CSV)

Even if the full export includes subscribers, export the list separately too — the subscribers page export often includes more useful columns (status, signup date, paid status).

1. Open the Subscribers page.
2. Find your subscriber list.
3. Use the export option.
4. Download the CSV file.
5. Save an untouched backup.
6. Create a working copy for cleanup and import.

If you have paid subscribers, check whether the export distinguishes free from paid. If it does not, filter the subscriber list by paid status in the dashboard and export the paid group separately.

## Export paid subscriber data

Paid subscriptions on Substack are billed through Stripe. Your Substack export shows who is a paid subscriber, but the payment records live in your Stripe account:

- Log in to your Stripe dashboard and confirm you can see your customers and subscriptions.
- Export your Stripe customer list as well — it is your source of truth for billing during the transition.
- Note renewal dates and plan types for each paid subscriber.

Read the full [paid subscriber migration guide](migrate-paid-subscribers.md) before making any changes to billing.

## Store your backups properly

- [ ] Keep the original ZIP and CSV files exactly as downloaded — never edit them.
- [ ] Store one copy in cloud storage (Google Drive, Dropbox, iCloud) and one locally.
- [ ] Name files with the export date, e.g. `substack-export-2026-07-06.zip`.
- [ ] Make a **working copy** of the subscriber CSV for cleaning — all edits happen on the copy.
- [ ] Keep the backups until at least 30 days after the migration is complete and audited.

The untouched original matters more than it seems: if an import goes wrong, or a subscriber disputes their status, the original export is your record of exactly what Substack held on export day.

## Next steps

- Clean your working copy: [Clean Your Subscriber List Before Import](clean-your-subscriber-list.md)
- Plan your content migration: [Migrate Your Substack Archive](migrate-your-archive.md)
- Back to the full [Substack Migration Checklist](../checklist.md)

---

## Need help migrating?

This guide is maintained by [LetterBucket](https://letterbucket.com). If you are moving from Substack and want help importing your subscribers and archive, [contact us](https://letterbucket.com/contact).
