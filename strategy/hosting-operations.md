# Hosting and recovery reference

Checked operating arrangement: 21 November 2026. Current release history/evidence is in [WORKLOG](../WORKLOG.md); active problems are in [TODO](../TODO.md). Build/edit/preview/deployment commands have one home: [site/README.md](../../site/README.md).

## System map

| Asset | Role |
|---|---|
| Cloudflare Pages project `jaisalmervisit` | Static frontend at jaisalmervisit.com; checked main pushes upload the committed `public/` directory and verify the deployment/domain. Branch/PR checks do not publish production. |
| Firebase `visitjaisalmer-e3085` | Firestore visitor data/forms/reviews, authentication and uploaded media. Billing confirmed handled on 21 Nov. Backend rules/live records are separate from a static release. |
| [Firebase fallback](https://visitjaisalmer-e3085.web.app) | Original hosting origin, checked HTTP 200 on 21 Nov; verify again before using it for recovery. |
| Separate private repositories | [Site](https://github.com/arun-0/jaisalmervisit-site) contains public source; [business](https://github.com/arun-0/jaisalmervisit-business) contains shared plans/evidence. Seed imports: site `65451b9`, business `f68e2a5`. Earlier source history was not supplied. |

Cloudflare Git integration failed with error 8000011/branch retrieval; Direct Upload and then GitHub Actions provided the release path. This moved the frontend, not Firebase services. Exact delivery/runtime behaviour and test commands are maintained in the site README/code, rather than repeated here.

## Deployment authority and credentials

The dedicated account token is named `jaisalmervisit-site-github-deploy`: Pages Write, no expiry, account scope. Its **value** exists only in encrypted repository secret `CLOUDFLARE_API_TOKEN`; the account ID is variable `CLOUDFLARE_ACCOUNT_ID`. Never print either credential flow or commit secrets. Local authorised Wrangler state is under `%LOCALAPPDATA%/JaisalmerVisit/Cloudflare`; another machine uses its own authorised session.

Production jobs are serial and skip stale main revisions. The workflow also supports manual retry; local preview/production scripts enforce their own release conditions. A main push publishes, so apply the relevant named-domain approval before merging a release. Recovery is a real production/DNS action, not permission inferred from these notes.

## Domain and recovery

Only the apex/www web records were changed in the cutover; mail, verification and other infrastructure have their own purposes.

| Name | Current Pages route | Historical Firebase rollback value |
|---|---|---|
| `@` | Proxied CNAME → `jaisalmervisit.pages.dev`, Auto TTL | A → `199.36.158.100`, DNS only; observed TTL 300 seconds. |
| `www` | Proxied CNAME → same Pages host; zone redirect sends path/query to HTTPS apex | CNAME → `visitjaisalmer-e3085.web.app`, DNS only; observed TTL 300 seconds. |

Historical authoritative nameservers: `hugh.ns.cloudflare.com`, `stella.ns.cloudflare.com`. A proxied/flattened apex normally answers with Cloudflare IPs. The enabled zone Single Redirect `Canonical www to jaisalmervisit.com` has rule ID `1523b6041b544e42b2e1d735996cac00`; the site tracks its specification in `deploy/canonical-redirect.json`. It preserves path/query with HTTP 301. Domain forwarding belongs to zone rules, not Pages path `_redirects`.

For a bad static release, prefer the prior known-good Pages deployment. If Firebase recovery is necessary and authorised, first confirm its old origin is usable, then restore the two historical DNS-only web records. Recheck apex/www, a guide, `/admin/`, ads.txt, sitemap and public Firestore loading, allowing for DNS/cache propagation. Do not alter unrelated records. [Cloudflare custom domains](https://developers.cloudflare.com/pages/configuration/custom-domains/).

Keep `public/google10227309e0228ef3.html` in future site releases to retain Search Console ownership. The static site has a real 404, admin noindex and public canonical/sitemap checks. Private admin sign-in, uploads, live form submissions, ad fill, account collection and revenue are distinct operational checks; passing a static release does not establish them.

## Collaboration and main branch control

Apply to both `arun-0/jaisalmervisit-business` and `arun-0/jaisalmervisit-site`. The owner authorised `jaisalmer-visit` (cousin) as a write collaborator, with only `arun-0` able to update/merge `main`. Other collaborators push topic branches and submit pull requests. The assistant may use existing owner authorisation/credentials for normal owner operations; this is not a delegation to another collaborator.

Prepared enforcement sequence:

1. Confirm rulesets are available for these **private** personal repositories. [GitHub plan support](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets) requires a suitable paid plan for private-repository rulesets. Billing remains an owner action; do not change visibility to obtain a feature.
2. Confirm repository ownership/admin roles still make `arun-0` the only person with administrator bypass. For each repository create an **active branch ruleset**, name `Owner-controlled main`, target exactly `refs/heads/main`, with **Restrict updates** enabled. Give **repository administrator** bypass **Always allow**, only while that role corresponds exclusively to the owner. Do not give Write/Maintain or the cousin bypass. This permits owner direct updates and owner PR merges while preventing collaborator main updates/merges. Do not merely require a PR, which by itself would not reserve merges to the owner. Use a supported explicit owner actor if available instead, after validating its identity.
3. Read the saved ruleset and effective rules for main back through GitHub; verify active enforcement, branch condition and bypass scope. Preserve existing checks and automatic site deployment. No need to push test content to main or impersonate the cousin to test.
4. Only after protection is confirmed, invite `jaisalmer-visit` with `push`/write on both repositories. Recheck pending invitation permissions; after acceptance recheck effective collaborator permissions. Invitation sent is not invitation accepted. Share normal repository/invitation links; no tokens.

Rule/approval ownership is in [AGENTS](../AGENTS.md); live capability, invitation and acceptance state belongs only in [T09](../TODO.md). [Available rule semantics](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets).
