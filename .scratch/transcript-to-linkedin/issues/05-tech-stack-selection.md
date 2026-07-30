# Tech stack selection (framework, DB, LinkedIn token storage)

Type: grilling
Status: resolved
Blocked by: 06

## Question

Given the constraints — free hosting (Vercel-style), free tiers everywhere except the paid LLM API, and LinkedIn OAuth as the sole auth mechanism — what's the concrete stack for this app?

Needs to cover:
- Web framework (a Vercel-friendly choice, e.g. Next.js, is the default assumption but hasn't been confirmed)
- Database for storing accounts, transcripts, generated posts, and history (must have a workable free tier)
- Where/how LinkedIn OAuth tokens (and refresh tokens) get stored and refreshed

Blocked on verifying the LinkedIn Developer Portal access path (ticket 06): if `w_member_social` requires Community Management review and a registered legal organization, that may force a rethink of the destination's direct-publish feature before the stack itself can be chosen.

## Answer

- **Framework**: Next.js — Vercel-native, zero-config free deploy.
- **Auth**: Auth.js (NextAuth) with its LinkedIn OpenID Connect provider, handling the sign-in + `w_member_social` OAuth flow and session cookies.
- **Database**: Notion, accessed via the Notion API — used deliberately despite the trade-offs discussed (no native Auth.js adapter, ~3 req/s rate limit, not a secrets-grade store for OAuth tokens). This means:
  - A **custom Auth.js adapter** must be written to persist sessions/accounts/tokens into Notion databases (no off-the-shelf adapter exists).
  - LinkedIn OAuth tokens will be stored in Notion pages/properties rather than an encrypted DB column — accepted as a known trade-off, not a gap to silently fix later.
  - Notion's rate limit (~3 req/s average) should be kept in mind for any bulk operations (e.g. loading history).
