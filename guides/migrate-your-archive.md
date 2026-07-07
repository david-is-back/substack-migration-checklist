# Migrate Your Substack Archive

Your archive — the posts you have already published — is often the most time-consuming part of a Substack migration, and also the part where you have the most room to make judgment calls. This guide helps you decide what to move, how to move it, and how to keep old links working.

## You do not have to migrate everything

It is tempting to move every post you ever published. In practice, most newsletters have a long tail of posts that get no traffic and have no backlinks. Migrating them all is fine if your new platform imports them automatically; if you have to move posts by hand, prioritize instead.

Migrate first:

- **Posts with search traffic.** Check your analytics (or Substack stats) for posts that still get visits months after publishing.
- **Posts with backlinks.** If other sites link to a post, that URL has SEO value worth preserving with a redirect.
- **Posts that convert.** Anything you link to from social bios, ads, or other posts as an entry point.
- **Evergreen content.** Guides, resources, and reference posts readers keep returning to.
- **Premium content.** Paid subscribers expect their paid archive to remain available — treat this as non-optional.

Posts that are purely time-bound (old announcements, expired promotions) can often stay behind or be dropped.

## How posts move between platforms

Some platforms import a Substack export ZIP directly; others accept RSS import; others require copy-paste. Check what your destination supports before planning a manual migration — an automatic importer can turn days of work into minutes. Formatting fidelity varies by platform, so always review imported posts rather than assuming they transferred cleanly.

## Review every migrated post

For each post you migrate, check:

- [ ] **Title** — imported correctly, no encoding glitches.
- [ ] **Slug / URL** — keep the same slug as the Substack URL if your platform allows it; this makes redirects trivial.
- [ ] **Images** — actually re-hosted on the new platform, not still loading from Substack's CDN (those can break later).
- [ ] **Embeds** — tweets, YouTube videos, and Substack-specific embeds (subscribe buttons, other posts) often break; replace or remove them.
- [ ] **Internal links** — links to your other posts should point at the new domain, not `substack.com`.
- [ ] **Paywalls** — re-apply the free/paid split on premium posts; imports usually don't preserve it.
- [ ] **Canonical URL** — if the platform exposes it, make sure it points to the new URL.
- [ ] **Meta title and description** — review for your most-trafficked posts.
- [ ] **OG image** — check the social sharing preview.
- [ ] **Rendering** — open the post on desktop and on a phone.

## Redirects: keep old links alive

If you used a custom domain on Substack, this is the payoff: once the domain points at your new platform, old URLs can redirect to the new posts, and you keep your SEO and shared links intact.

- Keep slugs identical where possible so `yourdomain.com/p/post-name` maps cleanly.
- If your new platform uses a different URL pattern, set up redirects from the old pattern (`/p/slug` → `/slug`, or per-post redirects for your top posts).
- If your publication lived on `yourname.substack.com` (no custom domain), you cannot redirect those URLs — Substack controls that domain. In that case, keep the Substack publication up with a pinned post pointing to your new home, and update the most important external links pointing at it.

More on the domain move itself: [Move Your Custom Domain from Substack](move-your-custom-domain.md).

## Archive migration checklist

- [ ] Listed all published posts and marked which to migrate
- [ ] Checked whether the new platform imports the Substack export automatically
- [ ] Migrated priority posts (traffic, backlinks, conversions, evergreen, premium)
- [ ] Reviewed titles, slugs, images, embeds, and internal links on each
- [ ] Re-applied paywalls on premium posts
- [ ] Reviewed canonical URLs, meta titles, descriptions, and OG images on top posts
- [ ] Set up redirects (or a plan for the no-custom-domain case)
- [ ] Tested a sample of posts on desktop and mobile
- [ ] Verified the public archive page lists everything correctly

## Next steps

- [Move Your Custom Domain from Substack](move-your-custom-domain.md)
- Back to the full [Substack Migration Checklist](../checklist.md)

---

## Need help migrating?

This guide is maintained by [LetterBucket](https://letterbucket.com). If you want help moving your Substack archive and newsletter website, [start your migration here](https://letterbucket.com/migrate-from-substack).
