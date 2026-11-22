# Revenue setup for review

Prepared 22 November 2026. Owner approved **Viator** and **personalised ads with appropriate consent** as directions and asked for a reviewable setup. This file owns the concrete setup/owner steps; [TODO T01–T05](../TODO.md) owns status, dependencies and approvals. [Concepts: affiliate](../explanations/affiliate-pilot-explanation.md) · [Concepts: ads/consent](../explanations/advertising-consent-explanation.md).

## India-first review gates

Use the [India-first audience plan and its limits](../strategy/roadmap.md#audience-and-market). The review gates below are implementation decisions for that market, not a second audience-data record.

- Before featuring Viator products, check INR price visibility, the actual total, domestic payment methods, pickup, cancellation and language/support fit. **UPI is unverified**; do not promise it. If that experience is poor for Indian travellers, compare a suitable India-friendly alternative before scaling the approved pilot.
- For India visitors, propose one concise privacy-choice experience with distinct optional advertising-personalisation and analytics choices, understandable refusal/manage controls and appropriate signals. Verify applicable requirements and the supported implementation; do not assume default grants or no obligations.
- Use the certified European message only for its relevant visitor regions, rather than a global Europe-centred flow. Validate region handling through supported CMP/provider APIs, not an invented client region guess. The actual Indian and overseas mobile flows must both be reviewed.

## Owner checklist

| Order | What the owner actually does | What to have ready | What to report here |
|---|---|---|---|
| 1 | Open [AdSense Verification check](https://adsense.google.com/adsense/u/0/pub-9028150722368329/payments/verification). First compare the cousin’s existing confirmation with this exact AdSense publisher/account; Google Ads or another profile is not proof this notice is resolved. If prior success matches, use Google’s in-account help/support for the contradiction. Complete a new private step only if the applicable current requirement is established. | Existing confirmation checked privately; correct actual payee/account. If a submission is genuinely required, follow the supported country/account documents shown by Google and [identity instructions](https://support.google.com/adsense/answer/7568896). | Service/account match and current status or non-sensitive error only. No documents, passwords, banking details or private confirmation transcripts. [Evidence](../reports/adsense-identity-check-2026-11-22.md); status/check condition only in T01. |
| 2 | Open [Viator signup](https://partners.viator.com/signup). Review the linked Tripadvisor/Viator terms and privacy notice, enter the owner-controlled business email, then personally choose **Create account** if agreed. | Control of the intended account email. Use a durable business-owned account; don't create another account if one already exists. | Whether an existing/new affiliate account is accessible and the next non-sensitive screen requirements. |
| 3 | Complete email verification, legal/business profile and any payment/tax setup requested by Viator, directly in that service. | Correct legal payee, country/account type, business contact/site; bank/PayPal/tax details only as actually requested and supported. Do not assume the domain name is the legal payee. | Account approval/eligibility status and genuine generated affiliate links, or non-sensitive blockers. Country-specific fields were not visible before signup and are not claimed as verified. |
| 4 | Review the proposed CMP/website batch below once its actual draft/preview and code are ready. | No extra documents needed for this review. | Approval or requested changes to that concrete batch; the high-level personalisation choice is already settled. |

The inspected Viator signup page has **Email → Create account**, and states that proceeding accepts its terms. No form was submitted. Legal acceptance and private onboarding stay with the owner; they are the remaining owner steps, not a request to choose Viator again.

## Viator application and link plan

Website: `https://jaisalmervisit.com/`. Public account contact may use the existing business email if the owner controls and chooses it. Do not invent legal name, address, country, registration or tax status.

Paste where a site/promotion description is requested:

> Jaisalmer Visit is an independent English-language destination guide and local provider directory. We publish practical place guides, itineraries and activity-planning information for Jaisalmer. We plan to place clearly disclosed contextual affiliate links in relevant safari and itinerary guides. Visitors would check live availability and complete reservations and payment on Viator. We do not operate booking checkout or collect traveller booking payments.

If asked for measured traffic, use the dated baseline and limitations in [the audit](../reports/revenue-audit-2026-11-21.md), not targets or invented monthly traffic. Signup eligibility and the actual agreement still need account confirmation.

| Placement | Proposed visitor action | Review before a real partner link is installed |
|---|---|---|
| Camel-safari guide; relevant Sam context | **Check sunset safari dates on Viator** | Candidate [178630P1](https://www.viator.com/tours/Jaisalmer/Half-Day-Sunset-Camel-Safari/d24761-178630P1): actual route, pickup, riding time, availability and cancellation. Do not promise Sam/Khuri service without product evidence. |
| Desert itinerary; relevant overnight context | **Check overnight safari dates on Viator** | Candidate [245696P1](https://www.viator.com/tours/Jaisalmer/An-Overnight-Non-touristic-Camel-Safari-2PM-to-11-30-AM-Next-Day/d24761-245696P1): open-air sleeping/no tents or washroom was material in the checked listing. Distinguish it from a camp with facilities. |

Candidates are for review, not endorsed/date-available inventory. Use generated account links with a supported campaign label per placement, such as `camel-guide-sunset`. Never fabricate an affiliate ID or treat an ordinary product URL as commissionable. Programme and inventory facts were checked from [Viator's resources](https://partnerresources.viator.com/travel-content/links/) and must be rechecked at integration.

Nearby disclosure proposed for the website:

> We may earn a commission if you book through these links. Check current prices, inclusions and cancellation terms on Viator.

Use `rel="sponsored noopener"` for new-tab affiliate links, clear destination labels and no static price/rating claims. Retain useful non-booking guide content. Test link destination, supported placement attribution and mobile usability; record clicks separately from completed experiences, cancellations, net commission and payouts. Do not make a paid/self-booking merely to test tracking.

## Personalised-ad/CMP proposal

This is a **specified proposal**, not a saved Google draft. Browser control ended before the AdSense preparation page could be reliably inspected. Available account options and actual previews must be verified before claiming readiness to activate.

| Control | Proposed choice / review condition |
|---|---|
| Site | `jaisalmervisit.com` only; existing publisher account. No other sites or permissions. |
| India / primary journey | Concise optional ad-personalisation and analytics choices, default-denied optional signals until the applicable choice; INR/domestic usability review. This custom/main-region implementation is not yet built or legally certified. |
| Tool / initial region | Google's certified European regulations message for EEA/UK/Switzerland; review other applicable regional requirements separately. |
| Language / identity | English; Jaisalmer Visit; privacy URL `https://jaisalmervisit.com/privacy`. No unverified business/legal details. |
| First-layer choices | **Consent**, **Do not consent**, **Manage options**. Keep refusal visible; never relabel consent as merely continuing to the guide. |
| Advertising | Allow personalised ads only from the appropriate valid consent. Honour refusal/withdrawal; eligible limited ads or no ads may result when other permissions are absent. |
| Partners / purposes | Inspect the actual vendor/purpose list; use what the site really deploys. No silent additions for unrelated marketing. Record choices in the reviewed draft. |
| Consent optimisation | Inspect the default before saving. Prefer a predictable first review with automatic message optimisation disabled if the interface permits; review the actual standard message and its content-blocking behaviour. Do not promise an always non-blocking banner. |
| Analytics | Preserve basic-mode opt-in: no GA4 download/event forwarding before analytics permission or after refusal/withdrawal. Do not silently reinterpret advertising acceptance as analytics consent. |
| Existing cookie notice | Remove the misleading blanket “Google ads (not personalised)” wording as part of the same reviewed activation batch. Avoid simultaneous overlapping CMP and analytics notices. Validate a supported regional callback/sequence before implementation; if necessary offer the separate analytics choice through Cookie settings after the ad choice. Do not invent a region lookup or consent signal. |
| Ad formats | Review existing overlay formats (previously 3/3) on mobile. Recommend keeping reading, maps, navigation and contacts clear; propose specific format changes after inspecting actual controls. |
| Guide coverage | Keep `auto_ads=false`/empty manual slots until the concrete account/content/placement rollout is reviewed. This high-level consent decision does not activate all articles. |

[Google message choices](https://support.google.com/adsense/answer/10961068?hl=en) · [Consent optimisation behaviour](https://support.google.com/adsense/answer/16878447?hl=en) · [Funding Choices API](https://developers.google.com/funding-choices/fc-api-docs).

### Proposed primary-journey notice copy (for review)

> Choose your privacy preferences. You can allow advertising based on your interests and separately allow analytics that helps us improve this guide. You can refuse optional uses or change your choices later.

Proposed controls: **Accept optional uses**, **Reject optional uses**, **Manage choices**; management separates advertising personalisation and analytics. These are a product proposal for the main India journey, not the text of Google's certified European message. Use only after the actual implementation, applicable requirements and signals have been verified. Old analytics acceptance must not be silently treated as new ad-personalisation consent.

### Website copy changes to review with the configuration

The current analytics notice says Google ads are not personalised; the privacy policy also describes that default and only says visitors “may” see a Google message. These need to match the actual activated CMP, regions and signals.

Proposed advertising-policy wording, subject to the implemented scope:

> We use Google AdSense. Where required, our consent message lets you consent, refuse or manage advertising data use. Personalised advertising uses information about your interests or activity only when the applicable consent has been obtained. Your choices may result in personalised, non-personalised, limited advertising or no advertising. These treatments do not all use the same data or storage. You can revisit your choices using the site's privacy controls.

The separate analytics choice should say what accepting it actually does, without implying it is also advertising consent. Link the actual deployed vendors/policies and working preference-reopening control. Affiliate links should disclose the commercial relationship and that Viator's privacy/checkout applies after leaving the guide. Do not describe these drafts as legal certification.

### Acceptance checks before activation/publication

1. T01 account status and any serving restrictions checked; correct publisher/ads.txt verified.
2. Real Google draft/preview records site, regions, choices, vendors, optimisation and consent-mode decisions. No unreviewed account-wide options.
3. Mobile accept/refuse/manage/withdrawal paths work; no overlapping notices, forced personalisation, broken maps or blocked contact actions.
4. Ad and analytics signals checked separately, including initial denied state and re-acceptance. A script request is not a filled impression.
5. Privacy/notice wording matches behaviour; guide eligibility and format settings reviewed. No live ad clicks or customer-data test submissions.
6. Normal site branch/build/preview checks pass; obtain the concrete final publication/account-setting approval if required, then verify release and account results and record the meaning in WORKLOG.

## Continue this preparation

Use the [six-part session setup and prompt](../NEXT-PROMPT.md). Status/next owner check lives in TODO; this pack contains the exact execution detail and does not maintain a second status table.
