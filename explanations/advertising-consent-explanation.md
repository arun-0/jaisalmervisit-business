# Personalised ads, non-personalised ads and visitor experience

Written for the owner on 21 November 2026. This is an explanation and recommendation, not approval to change advertising/privacy settings. See [the roadmap](../strategy/roadmap.md#current-priority-todo-list) for the next actions.

## The short answer

Yes, consent prompts can add friction and some visitors may leave. We have not measured that effect on jaisalmervisit.com, so there is no honest percentage to quote. A confusing prompt, repeated interruptions and intrusive ads can hurt the experience. The solution is a clear, usable choice and restrained advertising, with the actual supported consent interface reviewed on mobile.

My earlier question oversimplified the trade-off: choosing non-personalised Google ads does not automatically remove cookie-consent requirements. Consent for personalisation and consent for device storage are different things.

## Three different ad treatments

| Treatment | What influences the ad | Example / implication |
|---|---|---|
| Personalised ads | Previously collected information about a visitor's interests or activity can influence selection. | A visitor may see an ad related to an interest from earlier browsing. The data use goes beyond this guide's immediate topic. |
| Non-personalised ads | Context such as the current page, query or coarse location; past behaviour is not used for targeting. | A desert guide may attract contextual travel advertising. This is not a guarantee that every ad will concern Jaisalmer. |
| Limited ads | A separate restricted serving mode with fewer data-dependent features. | An eligible limited ad may be possible when the consent signals do not permit the other treatments. Fill and revenue are not guaranteed. |

The first two definitions follow [Google's explanation](https://support.google.com/adsense/answer/9007336). Non-personalised ads still use cookies for functions such as frequency capping and aggregate reporting, so permission for that storage can still be needed where applicable.

Limited ads are not simply another name for non-personalised ads, nor a promise of zero processing or zero storage. Basic delivery uses information such as IP addresses, and programmatic limited ads can use fraud-detection-only cookies/local storage. Eligibility depends on settings, transparency and signals. If suitable consent or a permitted serving route is absent, showing no ad is also an outcome. [Google's limited-ads guidance](https://support.google.com/adsense/answer/14210870)

## What visitors would actually experience

A consent-management platform (CMP) presents and records the choices and passes the appropriate signals to advertising systems. For personalised Google ads in the EEA, UK and Switzerland, Google requires a certified CMP integrated with the IAB framework. Where a visitor is located matters; our being an India-focused website does not mean all visitors are outside those regions. Other regional requirements must also be considered. [Google's publisher requirements](https://support.google.com/adsense/answer/13554116?hl=en-GB)

“The ads are non-personalised” and a simple custom cookie banner are not, by themselves, proof that the advertising consent setup is suitable. Consent Mode defaults are signals; they are not a replacement for gathering a valid choice.

The goal is a coherent experience with understandable accept, refuse and manage-options choices. Refusal must be honoured. Do not promise that declining personalisation always produces ordinary non-personalised ads: if storage permission was also refused, the eligible result could instead be limited ads or no ad.

Google's current CMP options are not all identical. A standard message can require a decision before content access; its limited-message option is non-blocking. Consent optimisation may choose between these treatments. We need to inspect the exact available configuration rather than promise a small banner or silently accept revenue-optimisation defaults. [Google's consent-message options](https://support.google.com/adsense/answer/16878447?hl=en)

## My recommendation for Jaisalmer Visit

Prepare and review a Google-certified consent setup that allows personalisation only with the appropriate consent, offers an easy refusal and uses an eligible restricted treatment or no ads otherwise. This preserves a potential revenue option without forcing every visitor to accept personalisation. If the owner prefers non-personalised-only ads, that is a valid product preference, but it does not eliminate the need to check storage consent.

For the mobile review, prioritise:

- Clear wording and visible refusal; no suggestion that a booking or guide requires agreeing to personalisation.
- One coherent consent experience rather than confusing stacked advertising and analytics prompts. Confirm whether the supported CMP integration can achieve this without silently broadening analytics consent.
- A remembered choice for the supported duration and a way to change it; do not nag after refusal.
- Usable maps, directions and reading flow. Preview the actual CMP's blocking behaviour and reject unsuitable layouts before publication.
- Restrained ad formats. The number, placement and size of ads can be a larger usability issue than whether their targeting is personalised; that is a design judgement, not a measured finding for this site.

Personalised demand may improve revenue, but the size of the improvement here is unknown. With only 403 recorded views in the previous 28-day GA4 window, avoid a long optimisation exercise before the account is active and there is enough genuine usage. Review earnings alongside consent choices, engagement and guide-to-booking actions. Do not infer a causal uplift from a few visits.

This recommendation remains pending the owner's decision and a concrete configuration/preview. No new message or advertising setting has been published.

## What “guide ads remain OFF” means

“Guides” are our separate article pages, for example `/places/sam-sand-dunes`, `/things-to-do/camel-safari` and the itinerary URLs. They are different from the interactive homepage at `/`.

The guide builder now has an `auto_ads` switch in `site/content/advertising.toml`, separate from manually placed ad units. It is currently `false`, and manual `slots` is empty. Therefore the generated guides do not load the AdSense publisher script or reserve manual ad slots. This does not mean their editorial content or operator links are disabled.

The homepage already includes Google's publisher script, and Auto ads is ON in the AdSense account. Our audit observed an unfilled slot and zero historical AdSense delivery. The guide switch does not switch homepage advertising off or resolve the account's identity, ads.txt or consent issues.

The guide-ad todo is therefore: settle account/consent handling, review eligible guide content and mobile placements, propose the concrete rollout, obtain any necessary approval and then verify actual serving. Do not enable all guides merely because a switch exists, add text just to meet ad thresholds, or treat a loaded script as earned revenue. No live ad should be clicked to test income.

## Follow-up setup

| Item | Use |
|---|---|
| Chat | Keep the consent decision, preview and rollout in this same revenue chat. |
| App | Local Codex for code/verification; the existing business AdSense account for the reviewed message. |
| Project | Jaisalmer Visit — C:\dev\ai\ghanu-jaisalmer-visit. |
| Model | GPT-6.2 Sol, Medium for preparation and verification; no claim of a measured cost optimum. |
| Exact prompt | “Prepare a mobile-reviewed consent proposal with easy refusal, appropriate regional signals and no silent analytics expansion. Keep guide ads off until the concrete account/content/consent rollout is reviewed.” |
| Follow-up / stop | State personalised-with-consent or non-personalised-only preference. Review the exact message, fallback and ad formats before activation; confirm account identity/serving status independently. |
