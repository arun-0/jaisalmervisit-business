# Source, hosting and recovery

Updated 21 November 2026. Both custom domains are active on Cloudflare Pages. The newest worklog entry records the deployed Git commit and final checks.

## Ownership and release

| Asset | Current arrangement |
|---|---|
| Website source | Private [arun-0/jaisalmervisit-site](https://github.com/arun-0/jaisalmervisit-site). Baseline `65451b9` imports the engineer’s November 5 snapshot. No earlier Git history was supplied. |
| Business materials | Private [arun-0/jaisalmervisit-business](https://github.com/arun-0/jaisalmervisit-business). Baseline `f68e2a5` imports the November 20 plan and drafts. Private transcripts, personal memory and exports stay local. |
| Static frontend | Cloudflare Pages project `jaisalmervisit`, production branch `main`. Direct Upload publishes the tracked public directory with its Git commit. [Pages production](https://jaisalmervisit.pages.dev) |
| Backend | Firebase project `visitjaisalmer-e3085` serves published visitor data, receives provider enquiries and reviews, authenticates admins, and stores uploaded photos and audio. The owner confirmed billing is handled on 21 November 2026. Backend access can be checked when a selected revenue action requires it. |
| Recovery origin | Original Firebase Hosting deployment, checked for HTTP 200 on 21 November. Keep it available at least through the initial monitoring period. [Firebase fallback](https://visitjaisalmer-e3085.web.app) |

The site’s first release was reviewed, checked and merged in [site PR 1](https://github.com/arun-0/jaisalmervisit-site/pull/1). The checked-out GitHub identity is the owner’s named account. The two checkouts use its GitHub no-reply address because GitHub rejected the first push under the global private-email setting.

The Cloudflare GitHub app installation could see the private repository, but branch lookup failed in the dashboard and the Pages API returned 8000011. Direct Upload provided a verified deployment. GitHub Actions performs the release checks on pushes and pull requests. Publishing is an explicit, separate step. The site release script supports both previews and production. The latter requires a clean checkout at the current GitHub main commit. [Release instructions](https://github.com/arun-0/jaisalmervisit-site/blob/main/README.md)

If automatic publication becomes worthwhile, reuse the release checks and add an owner-approved deployment job with a dedicated Pages-only credential and controlled production environment. The project can use CI-based Direct Upload. Switching to native Git integration would require a new Pages project and a tested domain transfer. [Cloudflare Direct Upload](https://developers.cloudflare.com/pages/get-started/direct-upload/)

## Cutover and rollback

The original authoritative nameservers were `hugh.ns.cloudflare.com` and `stella.ns.cloudflare.com`. On 21 November, before cutover, public DNS and response headers confirmed the two Firebase web targets below.

| Name | Firebase rollback value | Pages target |
|---|---|---|
| Apex `@` | A, `199.36.158.100`, DNS only. Observed answer TTL 300 seconds. | Proxied CNAME to `jaisalmervisit.pages.dev`, Auto TTL |
| `www` | CNAME, `visitjaisalmer-e3085.web.app`, DNS only. Observed answer TTL 300 seconds. | Proxied CNAME to `jaisalmervisit.pages.dev`, Auto TTL. A zone Single Redirect sends www to the same path on the apex with HTTP 301 and preserves the query string. |

The DNS change applies to those two web records. The domain also has mail, verification and other infrastructure that must be managed on its own terms. A proxied apex usually resolves to Cloudflare IPs because Cloudflare flattens the CNAME. Validate the hostname in Pages and fetch a guide over HTTPS.

The enabled zone rule is named `Canonical www to jaisalmervisit.com`, rule ID `1523b6041b544e42b2e1d735996cac00`. Its configuration is tracked in the site repository at `deploy/canonical-redirect.json`. Domain forwarding uses the zone rules engine because Pages `_redirects` supports path rules. HTTPS and the www redirect were checked with a guide path and campaign query parameters.

For a bad static release, use the previous known-good Pages production deployment. To return service to Firebase, confirm the old Firebase homepage is reachable, then restore the two DNS-only records above. Recheck the apex homepage, www redirect, `/admin/`, `/ads.txt`, `/sitemap.xml` and public Firestore reads. During propagation, different resolvers can briefly show different versions. [Cloudflare custom domains](https://developers.cloudflare.com/pages/configuration/custom-domains/)

## What was tested

- Six original endpoints matched byte-for-byte between Firebase and the Cloudflare parity preview, including the homepage, privacy, admin, robots, ads and sitemap.
- The guide release passed checks for 35 guide documents, 37 sitemap URLs, 14 referenced assets, a real 404, noindex on admin, a production canonical on each guide and page content without JavaScript. All 13 public attraction images returned HTTP 200.
- A local DOM test using published data exercised the two-day planner and Camel Safari deep links. Browser verification on a phone-sized viewport loaded 13 attraction photos, five eligible partner entries and eight transport services, selected the two-day itinerary, opened the fort map and displayed the provider form. An initial content request took about 2.5 seconds. The former 1.5-second startup limit was extended to eight seconds with request cancellation and regression checks for delayed, offline and stalled reads.
- Admin sign-in, private uploads, live form submissions, ad fill, GA4 collection, Search Console indexing and business revenue need separate owner evidence. SMS is disabled in the source. The release preserved the Firebase rules and data.

For the first two days, the owner can review sitemap processing, landing traffic, ad delivery, reported operator enquiries and actual admin sign-in. If a reader reports a problem, record the exact URL, time, device and symptom. Keep personal traveller details in the business inbox.
