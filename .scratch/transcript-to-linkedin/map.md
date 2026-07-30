# Transcript → LinkedIn (wayfinder map)

Label: wayfinder:map

## Destination

A complete spec for a new, standalone app — "Transcript → LinkedIn" — where a user pastes/uploads a meeting transcript, the app extracts multiple distinct angles/ideas from it via an LLM, the user picks any angle to turn into a full LinkedIn post draft (as many, in any order, as they like), edits it, and publishes it immediately and directly to LinkedIn via their connected account. Accounts exist so users can log in and browse a history of past transcripts and generated/published posts. The spec is ready to hand off to `/to-spec` → `/to-tickets` → `/implement`.

## Notes

- Standing constraint: host free (Vercel-style), use free tiers everywhere except the LLM API, which is paid.
- LLM for generation: Claude API (already decided — see Decisions so far).
- Consult `/grilling` and `/domain-modeling` when resolving tickets.
- Consult `/research` for tickets marked `research`.

## Decisions so far

- [LinkedIn API/OAuth requirements](issues/01-linkedin-api-oauth-requirements.md) — Technically feasible, no hard blockers (no fee, no follower/partner gate), but LinkedIn's docs are inconsistent on whether the posting scope is self-serve or requires org-level review — needed a live portal test.
- [Verify LinkedIn Developer Portal access path](issues/06-verify-linkedin-portal-access-path.md) — Confirmed self-serve, instant, no review. Credentials obtained. Direct-publish destination confirmed buildable; unblocks tech stack.
- [Tech stack selection](issues/05-tech-stack-selection.md) — Next.js + Auth.js (LinkedIn OIDC provider) + Notion as the datastore via a custom Auth.js adapter (chosen deliberately despite rate-limit/secrets-storage trade-offs).
- [Prompt/tone strategy](issues/07-prompt-tone-strategy.md) — Two-stage flow: flexible-count angle extraction, then on-demand full post drafting from any chosen angle, immediate publish only (no scheduling — see Out of scope).
- [LLM provider: Claude](issues/02-llm-provider-choice.md) — Claude API generates the post variations.
- [Auth mechanism: LinkedIn OAuth only](issues/03-auth-mechanism.md) — "Sign in with LinkedIn" is the sole login method; the same connection doubles as the publishing permission.
- [Transcript input format](issues/04-transcript-input-format.md) — Plain text paste/upload only for v1; no hard length limit specified yet.

## Not yet specified

- UI/UX flow: pages, editing experience for a generated draft, design of the history view.
- Cost/rate-limiting for Claude API usage per user.
- Error handling for failed generations or failed LinkedIn publishes.
- Data retention/privacy handling for transcript content (meeting transcripts may contain sensitive business information).

## Out of scope

- Other social platforms (X/Twitter, Threads, blog posts) — ruled out for v1; LinkedIn only.
- Scheduled/future-dated publishing — v1 is immediate-publish only (see [prompt/tone strategy ticket](issues/07-prompt-tone-strategy.md)); scheduling would need a cron/scheduler decision revisited later.
