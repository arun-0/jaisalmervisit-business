# Ads, consent and visitor experience

This explains concepts, not live configuration. [Current status](../TODO.md) · [Review settings and owner steps](../setup/revenue-setup.md#personalised-adcmp-proposal).

## Personalised, non-personalised and limited ads

| Treatment | Plain meaning |
|---|---|
| Personalised | Previously collected interests or activity can influence ad selection. |
| Non-personalised | Uses current context such as page content/query/coarse location rather than past behaviour. |
| Limited | A separate restricted serving treatment with fewer data-dependent features. |

Non-personalised Google ads still use cookies for functions such as frequency capping and aggregate reporting, so applicable storage-consent requirements do not disappear. [Google definitions](https://support.google.com/adsense/answer/9007336). Limited ads are not a zero-data/storage guarantee: basic delivery and, where enabled, fraud-only storage still matter. Signals/settings determine whether an eligible limited ad or no ad can be shown. [Limited ads](https://support.google.com/adsense/answer/14210870).

## Will a consent prompt put people off?

It can add friction; we have not measured an abandonment percentage here. Confusing choices, repeated prompts, stacked notices and intrusive ads can hurt a mobile travel task. Those are design risks to review, not evidence that this site's visitors have already left.

My recommendation is appropriate consent before personalisation, clear refusal and preference changes, and eligible restricted ads or no ads otherwise. Don't imply agreeing to personalisation is necessary to book or use the guide. Review actual mobile behaviour; Google's standard message may require a decision before content access, while its limited-message option is non-blocking. [Message options](https://support.google.com/adsense/answer/16878447?hl=en).

## India-first, with regional handling

The selected [India-first market](../strategy/roadmap.md#audience-and-market) determines the main visitor journey. The owner’s physical UK location is not the visitor location.

Do **not** impose an EEA/UK-focused consent message globally merely because this work happens in the UK. Google's certified European message requirements apply to the relevant visitor regions; other applicable rules and Google's signals still need review for India and other traffic. This is regional design, not an assertion that India has no privacy/consent obligations. [Google regional requirement](https://support.google.com/adsense/answer/13554116?hl=en-GB).

Consent Mode signals and a custom “non-personalised” label are not, by themselves, a valid consent solution. Google CMP only updates its European-region choices for users shown that message; defaults and the main India flow must be deliberately handled. [Google consent mode](https://support.google.com/adsense/answer/16053245?hl=en). Keep analytics opt-in separate unless a concrete reviewed integration changes it; do not silently broaden data use.

## What “guide ads remain OFF” means

Guides are separate place, activity and itinerary articles, such as `/places/sam-sand-dunes`; the interactive homepage `/` is separate.

The guide builder's `site/content/advertising.toml` has `auto_ads=false` and `slots=[]`: generated guides omit the publisher loader/manual ad placements. Guide text, maps and operator links still work. This does not switch off the homepage's existing publisher script or prove anything about account fill/earnings.

The pending rollout is a content/account/consent/placement decision, not just flipping a technical switch. Review eligible guides, mobile formats and real serving before expanding. Do not pad articles for ads or click live ads as an income test. Current status and dependencies belong in T02/T05, while exact controls/copy/checks belong in the setup pack.
