# Substack Migration Checklist

A practical checklist for moving your newsletter from Substack to another platform without losing subscribers, breaking old links, or confusing your readers.

This guide is platform-agnostic. It works whether you are migrating from Substack to [LetterBucket](https://letterbucket.com), Ghost, Kit, Beehiiv, WordPress, or any other newsletter platform. The steps that matter — exporting your data, cleaning your subscriber list, protecting paid subscriptions, moving your custom domain, and testing deliverability — are the same everywhere.

## What this guide covers

- Exporting your Substack data (subscribers, posts, and settings)
- Backing up your published posts and archive
- Cleaning your subscriber list before importing it anywhere
- Preparing your new newsletter setup before you switch
- Handling paid subscribers carefully so nobody loses access or gets double billed
- Moving a custom domain away from Substack without downtime
- Testing email deliverability from your new platform
- Announcing the migration to free and paid subscribers
- Auditing everything after the move

## What you will migrate

When you move a newsletter off Substack, you are migrating more than an email list. Plan for all of it:

- Subscribers
- Free and paid member status
- Published posts
- Images and media
- Custom domain
- Signup forms
- Email sender settings
- Analytics and tracking
- Paid subscription flow
- Public archive links

## Quick warning

Do not cancel, delete, redirect, or change your Substack publication until you have exported your data, tested your new setup, and sent at least one successful test email from your new platform.

Your Substack publication is your safety net during the migration. Keep it intact until the new setup is fully verified.

## How to use this checklist

1. Read the full [migration checklist](checklist.md) once, end to end, before doing anything.
2. Work through the guides in order — they follow the same sequence as the checklist.
3. Use the [templates](templates/) for subscriber imports, announcement emails, and post-migration audits.
4. If you hit a problem, [open an issue](../../issues/new/choose) and describe where you got stuck.

## Run the checklist automatically with Claude Code

The automatable parts of this checklist — export integrity (section 2), subscriber list cleanup (section 3), and post archive dependencies (section 5) — are packaged as a free [Claude Code](https://claude.com/claude-code) skill: [substack-migration-check](https://github.com/david-is-back/substack-migration-skill).

Point it at your Substack export ZIP and it produces an audit report, a cleaned import-ready subscriber CSV, and a per-post dependency inventory. It runs fully offline — your subscriber data never leaves your machine.

Install it from Claude Code:

```
/plugin marketplace add david-is-back/substack-migration-skill
/plugin install substack-migration-check@substack-migration-check
```

Then ask: *"Check my Substack export at ~/Downloads/my-export.zip — I'm migrating."*

## Contents

### The checklist

- [Substack Migration Checklist](checklist.md) — the full step-by-step checklist with checkboxes

### Guides

- [How to Export Your Substack Data](guides/export-from-substack.md)
- [Clean Your Subscriber List Before Import](guides/clean-your-subscriber-list.md)
- [Migrate Your Substack Archive](guides/migrate-your-archive.md)
- [Migrating Paid Subscribers from Substack](guides/migrate-paid-subscribers.md)
- [Move Your Custom Domain from Substack](guides/move-your-custom-domain.md)
- [Deliverability Checklist After Migrating from Substack](guides/deliverability-checklist.md)

### Templates

- [Subscriber import CSV template](templates/subscriber-import-template.csv)
- [Migration announcement email — free subscribers](templates/migration-announcement-free-subscribers.md)
- [Migration announcement email — paid subscribers](templates/migration-announcement-paid-subscribers.md)
- [Domain switch checklist](templates/domain-switch-checklist.md)
- [Post-migration audit](templates/post-migration-audit.md)

## Who this is for

This checklist is written for creators, founders, consultants, writers, and newsletter operators who want to migrate from Substack without losing subscribers or revenue. It assumes no technical background beyond being able to download a CSV file and update a DNS record (and the domain guide walks you through that part).

## A note on caution

Every newsletter platform handles imports, paid subscriptions, and domains a little differently. Not all data transfers perfectly between platforms, and paid subscriber migration in particular is rarely fully automatic. Where something depends on your destination platform, this guide says so — always verify the specifics with the platform you are moving to.

## Related resources

Maintained alongside this checklist:

- [Substack Alternatives](https://github.com/david-is-back/substack-alternatives) — an honest comparison of newsletter platforms if you are still deciding where to move
- [Ghost Migration Checklist](https://github.com/david-is-back/ghost-migration-checklist) — the same playbook for leaving Ghost
- [beehiiv Migration Checklist](https://github.com/david-is-back/beehiiv-migration-checklist) — the same playbook for leaving beehiiv
- [Mailchimp Migration Checklist](https://github.com/david-is-back/mailchimp-migration-checklist) — the same playbook for leaving Mailchimp

## Contributing

Found something outdated, unclear, or missing? Open an issue or a pull request. Substack's interface and export options change over time, and this checklist stays useful because people report what changed.

## Migrating from Substack?

This checklist is maintained by LetterBucket, a simple newsletter platform for creators who want to write, send, and publish from one place.

If you are moving from Substack and want help migrating your subscribers, archive, and newsletter website, get in touch:

[Contact LetterBucket about your migration](https://letterbucket.com/contact)
