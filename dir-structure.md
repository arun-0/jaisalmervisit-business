# Business directory reference

Checked on 21 November 2026.

Local folder — `C:\dev\ai\ghanu-jaisalmer-visit\business`

Private repository — [arun-0/jaisalmervisit-business](https://github.com/arun-0/jaisalmervisit-business)

This folder contains 14 documents, including this reference, across the root and four subfolders. It holds the shared plans, instructions, drafts and handover records for the owner and brother.

## Directory tree

```text
business/
├── AGENTS.md
├── CLAUDE.md
├── HANDOFF.md
├── README.txt
├── WORKLOG.md
├── dir-structure.md
├── content/
│   └── engineer-brief.md
├── setup/
│   ├── chatgpt-workflows.md
│   ├── claude-account-setup.md
│   └── owner-inputs.md
├── social/
│   ├── calendar-2026-11-week1-2.md
│   └── social-media-plan.md
└── strategy/
    ├── git-and-hosting-plan.md
    └── roadmap.md
```

## Root files

| File | Function | Current role |
|---|---|---|
| [AGENTS.md](AGENTS.md) | Gives assistants the business context and working rules. Covers handovers, Git conventions, revenue priorities, owner review, existing authorisations, privacy, Windows Git Bash, uv and fnm. | The shared instructions for work inside this business checkout. It records that Firebase billing is handled and that effort estimates guide priorities without imposing arbitrary caps. |
| [CLAUDE.md](CLAUDE.md) | Imports `AGENTS.md` using Claude's `@AGENTS.md` syntax. Contains a comment explaining where shared rules live. | Lets Claude use the same business instructions. Shared changes belong in `AGENTS.md`. |
| [HANDOFF.md](HANDOFF.md) | Introduces the workspace, links both private repositories, gives their Windows paths and points to the current plan, owner inputs, working-session prompt and hosting notes. | Orientation for someone joining or resuming the project. |
| [README.txt](README.txt) | Provides a short entry point to `HANDOFF.md`, `WORKLOG.md` and the roadmap. Identifies the original handoff materials' location. | A brief introduction suitable for opening in a basic text editor. |
| [WORKLOG.md](WORKLOG.md) | Records completed work, verification, unresolved inputs and the next direction, newest entry first. Includes deployment commits, workflow runs and corrections to earlier decisions. | The handover history between the owner, brother and work sessions. Older entries describe the state at their date. Later entries record changes and supersede earlier assumptions. |
| [dir-structure.md](dir-structure.md) | Shows the directory tree and explains each current file and folder. | This inventory. Update it when files are added, removed or repurposed. |

## content/

This folder currently holds the technical content brief that informed the website changes.

| File | Function | Current role |
|---|---|---|
| [engineer-brief.md](content/engineer-brief.md) | Preserves the original SEO brief. It requests full HTML pages for places, itineraries and activities, unique metadata, structured data, ordinary links, an automatic sitemap, editable content, ad placements, partner cleanup and image descriptions. | Historical requirements with an updated status paragraph at the top. The 35 launch guides and technical foundations have shipped. Local fact checks, richer copy and the appropriate monetisation integration remain part of the evolving work. |

Published guide Markdown and generated website HTML are in the sibling `site` checkout. This business folder holds the brief and planning context.

## setup/

This folder describes how work is organised and what access or evidence a selected task may need.

| File | Function | Current role |
|---|---|---|
| [chatgpt-workflows.md](setup/chatgpt-workflows.md) | Contains the revenue-session setup, app and model recommendation, full project path, exact copy-paste prompt and approach to early review, continued work and handover. | The current reusable revenue prompt. It treats 80/20 as prioritisation, allows scope to evolve with owner feedback and makes automation a progressive objective. |
| [claude-account-setup.md](setup/claude-account-setup.md) | Preserves the initial Claude setup instructions, including profile text, project instructions, suggested connectors, draft/publish responsibilities and working habits. | Historical reference. Its original paths, product details and workflow assumptions may differ from the current setup. The opening note points to the current working-session document. |
| [owner-inputs.md](setup/owner-inputs.md) | Lists useful Search Console, GA4 and AdSense evidence, commercial partner or affiliate inputs, and local facts. Also covers optional Instagram, Facebook, YouTube, WhatsApp, Threads, X, Gmail, newsletter and Drive inputs. | A reference for requesting the access or evidence needed for the action being pursued. Available signed-in sessions and reports come first. The full list is not a prerequisite for starting useful work. |

## social/

This folder contains the original social strategy and reusable draft material.

| File | Function | Current role |
|---|---|---|
| [social-media-plan.md](social/social-media-plan.md) | Describes the initial channel priorities, content themes, production ideas and growth assumptions. Includes draft Instagram, Facebook and YouTube profile copy, plus WhatsApp greetings, away messages and quick replies. | A draft/reference bank. The roadmap governs current priorities. The November 14 audience counts, quotas and targets are historical planning assumptions. |
| [calendar-2026-11-week1-2.md](social/calendar-2026-11-week1-2.md) | Contains ten proposed posts dated November 16–29, including Reel concepts, carousel outlines, captions, calls to action and hashtags. Flags claims that need a local check. | Reusable editorial drafts. The file records proposed content, without establishing that it was published. Dates, factual claims, media rights and commercial references need review when a draft is used. |

## strategy/

This folder holds the current business priorities and technical operating record.

| File | Function | Current role |
|---|---|---|
| [roadmap.md](strategy/roadmap.md) | Sets revenue priorities and records what has shipped. Covers ad coverage, booking paths, commercial page improvements, evidence and revenue calculations, owner review, progression and automation. Includes a major/minor comparison with the original seed plan. | The master business plan. It prioritises expected return on effort while allowing the work to develop through feedback and results. |
| [git-and-hosting-plan.md](strategy/git-and-hosting-plan.md) | Records repository baselines, Cloudflare Pages, the Firebase backend and fallback, automatic deployment from site main, credential names and permissions, domain records, the www redirect, recovery procedures and completed checks. | The technical operating and recovery reference. It describes the approved deployment credential without storing its secret value. |

## Relationship to the rest of the project

The project root is `C:\dev\ai\ghanu-jaisalmer-visit`.

| Location | Purpose |
|---|---|
| `business\` | Shared business plans, instructions, drafts and handovers documented here. |
| `site\` | Website code, published guide source, generated HTML, assets, checks and deployment workflow. A successful push to that repository's main branch publishes the website through GitHub Actions. |
| `seed-resource\` | Original supplied website and business handoff snapshots, archives and private reference material. |

Documents mention future reporting and private-input locations such as `reports/`, `reports/raw/` and `private/`. These folders are absent from the current business inventory. They can be created when the work produces the relevant material.

The current business record is distributed by function. `AGENTS.md` holds working instructions, `roadmap.md` holds priorities, `WORKLOG.md` records events and decisions, and `chatgpt-workflows.md` supplies the reusable session setup. Historical briefs and drafts preserve their original context, with current directions supplied by those shared records.
