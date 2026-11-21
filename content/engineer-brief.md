# Brief for the jaisalmervisit.com engineer — search (SEO) changes

The original brief below is retained for context. On 21 November the site release added 35 static guides, editable Markdown, homepage links, a generated 37-URL sitemap, accessible attraction photos and a partner list with one entry per eligible business. Manual article ad units are configurable but await confirmed unit IDs and publisher consent review. The current priorities and owner evidence are in strategy/roadmap.md and setup/owner-inputs.md. Full local fact checks and expanded guide copy remain editorial work.

*Prepared 14 Nov 2026. Goal: more Google search traffic, which drives AdSense revenue.*

## The problem
The site is a single-page app. Attractions, itineraries and activities exist only as sections / hash routes of the home page (`/#map/fort`, `/#plan`). `sitemap.xml` lists 2 URLs. Google indexes and ranks URLs, and ignores `#fragments`, so the site can rank for roughly one query set (the home page) instead of hundreds.

## What to build, in priority order

### 1. A real, crawlable URL for every place, itinerary and activity
- Examples: `/places/jaisalmer-fort`, `/places/kuldhara`, `/places/sam-sand-dunes`, `/itineraries/2-days`, `/itineraries/family`, `/things-to-do/camel-safari`.
- Each URL must return **full HTML from the server** (static generation / pre-rendering, e.g. Firebase Hosting + a static build step), not an empty shell filled by JavaScript.
- Each page gets its own `<title>`, meta description, canonical, one `<h1>`, Open Graph image and schema.org data (`TouristAttraction`, `TouristTrip`, `FAQPage` where relevant).
- Keep the current home page and app experience; the home page links to these pages with normal `<a href>` links.
- Old `#map/...` links should keep working (or redirect in JS to the new URL).

### 2. Sitemap and Search Console
- Generate `sitemap.xml` automatically from the same data that builds the pages.
- After launch, the owner submits it in Google Search Console.

### 3. A simple way to add content without code
Owner (with Claude's help) will write 40–60 long pages over 3 months. Preferred: pages come from Markdown files or Firestore documents, so new content doesn't need a developer each time. Fields per place: title, slug, short description, body (sections: history, what to see, timings, tickets, how to reach, time needed, tips, nearby), images with alt text, lat/long, FAQ list.

### 4. Ads on content pages
- 2–3 AdSense slots per long page (after intro, mid-content, before footer). Consider Auto ads on content pages only.
- Keep layout shift low (reserve ad space).

### 5. Quick fixes (small)
- Remove test listings ("Service provider ltd", "WorkNeed App") from public view.
- BEST CHOICE strip shows every listing twice. Check if this is a carousel loop or a bug; screen readers and crawlers see duplicates.
- Add `alt` text to all images (currently 15 of 15 have none).
- Hindi versions later: `/hi/...` URLs with `hreflang` tags.

## How we'll know it worked
Search Console → pages indexed rises from ~2 to 50+, and search impressions/clicks grow month over month.

## Questions for the engineer
1. What framework / build setup is the site on, and can it pre-render pages?
2. Where do the places and listings data live today (`site-data.js`, Firestore)?
3. Rough time estimate for items 1–3?
