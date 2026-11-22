# Working from the cousin's Claude Code

The same [AGENTS rules](../AGENTS.md) apply to both contributors. [NEXT-PROMPT](../NEXT-PROMPT.md) owns the two six-part setups and exact prompts; [TODO](../TODO.md) owns current work and approvals. Do not maintain another task list in Claude's profile or memory.

## First-time checkout

Use **local Claude Code**, included with Claude Pro when signed in with that subscription. A plain Claude chat or a read-only GitHub connection is not this editing/push workflow. Browser sessions and private account access from the owner's computer do not transfer to the cousin's computer.

On his own Windows machine, the recommended layout is `C:\dev\ai\ghanu-jaisalmer-visit\business` and sibling `site`. If that location already has either checkout, inspect/reuse it rather than clone over it. If he uses a different OS/location, choose the actual full path and report it; the owner's Windows path does not prove a path exists elsewhere.

For a new Windows layout, run in **Git Bash**, one command per line:

```bash
mkdir -p /c/dev/ai/ghanu-jaisalmer-visit
cd /c/dev/ai/ghanu-jaisalmer-visit
git clone https://github.com/arun-0/jaisalmervisit-business.git business
git clone https://github.com/arun-0/jaisalmervisit-site.git site
cd business
claude --add-dir ../site
```

Install Claude Code from its [official setup](https://code.claude.com/docs/en/setup) if absent, then sign in with Claude Pro. Do not copy the other person's credentials or install an unrelated API key. If Claude Code is already using a separately billed API credential, deliberately select subscription login; Pro does not include separate API billing. Use the existing Git/uv/Node setup where available; only install dependencies actually needed for the chosen task.

The Desktop **Code** tab can also open this business folder locally with the sibling site allowed. `business/CLAUDE.md` imports `AGENTS.md`; the exact prompt explicitly reads the shared records and site rules. Don't assume opening the parent folder automatically discovers every nested instruction. [Claude memory/import behaviour](https://code.claude.com/docs/en/memory#import-additional-files).

Confirm `gh api user --jq .login` reports **jaisalmer-visit** before pushing/creating PRs. If gh is unavailable or unauthenticated, complete his normal GitHub login or use another authorised GitHub tool. Confirm the configured Git author is his human identity; do not substitute arun-0 or add AI trailers. Never paste tokens into chat. Repositories are public, so public cloning alone does not prove authenticated write access.

Select the model/effort and paste the contributor prompt in [NEXT-PROMPT](../NEXT-PROMPT.md#cousin--claude-code). Later short prompts rely on the [shared turn-taking contract](../AGENTS.md#taking-turns-across-two-repositories), not memory of this chat. [Owner-only branch configuration](../strategy/hosting-operations.md#collaboration-and-main-branch-control).

## Scope of portable guidance

The owner's global Codex instructions are local to that machine/tool, not global Claude settings. The shared project rules are portable because they are committed and explicitly loaded. For another tool without filesystem access, provide current entry/TODO/relevant details and their date; check its actual capabilities before expecting edits, tests or PRs. Keep private transcripts, IDs and payment details out of uploads and repositories.

The earlier Claude UI/profile tutorial remains historical in [Git at f03fe41](https://github.com/arun-0/jaisalmervisit-business/blob/f03fe41/setup/claude-account-setup.md); it is not the current workflow.
