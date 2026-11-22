# Working from the cousin's Claude Code

The same [AGENTS rules](../AGENTS.md) apply to both contributors. [NEXT-PROMPT](../NEXT-PROMPT.md) owns the two six-part setups and exact prompts; [TODO](../TODO.md) owns current work and approvals. Do not maintain another task list in Claude's profile or memory.

## First-time checkout

Use **local Claude Code**, included with Claude Pro when signed in with that subscription. A plain Claude chat or a read-only GitHub connection is not this editing/push workflow. Browser sessions and private account access from the owner's computer do not transfer to the cousin's computer.

On his own Windows machine, the recommended layout is `C:\dev\ai\ghanu-jaisalmer-visit\business` and sibling `site`. If that location already has either checkout, inspect/reuse it rather than clone over it. If he uses a different OS/location, choose the actual full path and report it; the owner's Windows path does not prove a path exists elsewhere.

## Before cloning: tools and GitHub login

`gh` is **GitHub CLI**, a separate local program. Signing into GitHub in Chrome does not automatically authenticate it; Claude Pro does not install or log it in. On the cousin's machine, install [Git for Windows](https://git-scm.com/install/windows) if needed to obtain Git Bash, and open Git Bash. Check `git --version` and `gh --version` before installing anything.

If GitHub CLI is absent and WinGet is available, run this in Git Bash:

```bash
winget install --id GitHub.cli --exact --source winget
```

Alternatively use GitHub's [official installer](https://github.com/cli/cli/releases/latest). Close/reopen Git Bash after installation so PATH refreshes, then confirm `gh --version`. If the existing install isn't found, locate/fix PATH rather than reinstall blindly. Use equivalent official setup on another OS.

Authenticate independently of Chrome:

```bash
gh auth login --hostname github.com --git-protocol https --web
gh api user --jq .login
gh auth setup-git
```

Complete the browser/device flow privately as **jaisalmer-visit**. The identity command must print that login. If another account or an overriding environment credential is active, resolve the mismatch without printing credentials or reusing arun-0's session. Never send passwords, device codes, OTPs or tokens to an assistant. [Official login flow](https://cli.github.com/manual/gh_auth_login) · [Git credential helper](https://cli.github.com/manual/gh_auth_setup-git). Setup is not verified just because public cloning works.

Install Claude Code from its [official setup](https://code.claude.com/docs/en/setup) if absent, then sign in with Claude Pro. A missing Windows CLI can be installed through `winget install --id Anthropic.ClaudeCode --exact --source winget`; reopen the terminal and verify `claude --version`. Do not copy the other person's credentials or install an unrelated API key. If Claude Code is already using a separately billed API credential, deliberately select subscription login; Pro does not include separate API billing.

## Clone and start the project

For a **new** Windows layout, run in Git Bash one command per line. Clone each repository only if its target does not already contain a checkout; inspect existing directories rather than execute blindly:

```bash
mkdir -p /c/dev/ai/ghanu-jaisalmer-visit
cd /c/dev/ai/ghanu-jaisalmer-visit
gh repo clone arun-0/jaisalmervisit-business business
gh repo clone arun-0/jaisalmervisit-site site
cd business
claude --add-dir ../site
```

Alternatively, once **local Claude Code** is available, open the empty/existing parent folder and paste the [standalone bootstrap prompt](../NEXT-PROMPT.md#first-session--bootstrap). It checks/installs tools, guides private GitHub login and clones missing checkouts before reading project records. It stops at verified setup. Then say **Setup verified; start my contributor turn using NEXT-PROMPT.md**. This avoids the old circular assumption that the first prompt could read files before cloning them.

Use existing uv/Node installations where available and install only dependencies needed for the selected task. Do not change the configured human Git author; if absent, ask for the cousin's preferred author name/email and set it locally in each repository, not as arun-0 or an AI identity.

The Desktop **Code** tab can also open this business folder locally with the sibling site allowed. `business/CLAUDE.md` imports `AGENTS.md`; the exact prompt explicitly reads the shared records and site rules. Don't assume opening the parent folder automatically discovers every nested instruction. [Claude memory/import behaviour](https://code.claude.com/docs/en/memory#import-additional-files).

Confirm `gh api user --jq .login` reports **jaisalmer-visit** before pushing/creating PRs. If gh is unavailable or unauthenticated, complete his normal GitHub login or use another authorised GitHub tool. Confirm the configured Git author is his human identity; do not substitute arun-0 or add AI trailers. Never paste tokens into chat. Repositories are public, so public cloning alone does not prove authenticated write access.

Select the model/effort and paste the contributor prompt in [NEXT-PROMPT](../NEXT-PROMPT.md#cousin--claude-code). Later short prompts rely on the [shared turn-taking contract](../AGENTS.md#taking-turns-across-two-repositories), not memory of this chat. [Owner-only branch configuration](../strategy/hosting-operations.md#collaboration-and-main-branch-control).

## Scope of portable guidance

The owner's global Codex instructions are local to that machine/tool, not global Claude settings. The shared project rules are portable because they are committed and explicitly loaded. For another tool without filesystem access, provide current entry/TODO/relevant details and their date; check its actual capabilities before expecting edits, tests or PRs. Keep private transcripts, IDs and payment details out of uploads and repositories.

The earlier Claude UI/profile tutorial remains historical in [Git at f03fe41](https://github.com/arun-0/jaisalmervisit-business/blob/f03fe41/setup/claude-account-setup.md); it is not the current workflow.
